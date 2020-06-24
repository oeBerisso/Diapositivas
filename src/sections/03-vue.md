
<img src="static/vue.png">

----
## VueJS

- A diferencia de otros frameworks monolíticos, Vue está diseñado desde el inicio para ser adoptado incrementalmenteLa biblioteca principal se enfoca solo en la capa de la vista, y es muy simple de utilizar e integrar con otros proyectos o bibliotecas existentes.
- Es un framework "reactivo" que implementa "two way data-binding": enlace de datos en dos direcciones (entre la vista y el modelo) de una manera muy eficiente y rápida.
- Posee una gran facilidad de aprendizaje y uso con respecto a otros frameworks como ReactJS.
- utiliza el patron MVVM

----

### Estructura del cliente vue

```
.
├── assets                    # Configuraciones para el despliegue del entorno productivo y entorno de pruebas
├── components                # Componentes reutilizables (vistas)
├── helpers                   # Archivos con funciones útiles que son utilizadas en varios lugares
├── routes                    # Declaracion de rutas
├── models                    # Modelos
|    App.vue                   # Layout de las vistas
|    main.js                   # Inicializa el componente raiz de proyecto y configura los pluggins de terceros a utilizar
```

----
### Vue CLI (COMMAND LINE INTERFACE)

- El `vue-cli` (es decir, la “interfaz de línea de comandos Vue”) es una herramienta creada por el equipo Vue.js para ayudar a facilitar el rápido desarrollo de las aplicaciones Vue.
- vue create <nombre-del-proyecto> te permite generar un proyecto de manera rapida con configuraciones tales como babel, vuex, router, linter, entre otros.

----

### Integracion con flask

En el package.json (archivo principal que contiene la configuracion del proyecto), agregamos un script que utiliza
vue cli para convertir los archivos .vue, en estaticos que flask puede utilizar, para esto es necesario brindar una configuracion en un archivo vue.config.js

----

### Configuracion


CODE: vue.config.js javascript