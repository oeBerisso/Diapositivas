
<img src="static/Flask.png">

----
## Flask

Flask es un Framework minimalista que permite crear aplicaciones web rápidamente, sin ninguna estructura fija, y la capacidad de escalarlo tanto como sea necesario

----
### Patron MVC (MODELO-VISTA-CONTROLADOR)

- Modelo: Se encarga de los datos, generalmente (pero no obligatoriamente) consultando la base de datos. Actualizaciones, consultas, búsquedas, etc. todo eso va aquí, en el modelo.
- El Controlador: Responde a eventos (usualmente acciones del usuario) e invoca peticiones al 'modelo' cuando se hace alguna solicitud sobre la información (por ejemplo, mostrar los datos de un usuario o editarlos).
- La Vista: Son la representación visual de los datos, todo lo que tenga que ver con la interfaz gráfica va aquí.

----

### Estructura interna del proyecto

```
.
├── config                    # Configuraciones para el despliegue del entorno productivo y entorno de pruebas
├── helpers                   # Archivos con funciones útiles que son utilizadas en varios lugares
├── models                    # Modelos
├── resources                 # Controladores
├── static                    # Archivos tales como estilos, JavaScript, imágenes
├── templates                 # Vistas
├── validations               # Reglas para validar los formularios
|   db.py                     # Funciones para la conexión con la base de datos
|   __init__.py               # Inicializa el proyecto y contiene todas las rutas que entiende el sistema
```

----

### Switch con la logica de las validaciones

CODE: validator.py python

----

### Funciones para validar

CODE: field.py python

----

### Ejemplo de reglas para el registrar

```py
rules = {
    "username": {"presence": True, "unique_user": True, "name": "usuario"},
    "last_name": {"presence": True, "name": "apellido"},
    "first_name": {"presence": True, "name": "nombre"},
    "email": {"presence": True, "email": True, "unique_mail": True, "name": "email"},
    "password": {
        "presence": True,
        "min_length": 6,
        "compare_fields": "confirm_password",
        "name": "contraseña",
    },
    "confirm_password": {
        "presence": True,
        "min_length": 6,
        "name": "confirmar contraseña",
    },
}
```
