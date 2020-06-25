## Virtualización
----

## Virtualización
En la cátedra se promueve virtualizar el código python con virtual env, pero no se decía nada sobre la base de datos

----

Para evitar problemas de compatibilidad entre miembros del grupo utilizamos docker para virtualizar la base de datos y usamos docker-compose para también tener un phpmyadmin.

----

¿Que pasa cuando se quiere programar en un dispositivo nuevo?

----

Terminamos armando un docker para python y lo agregamos al docker-compose

----

### Concluisión

* Para proyectos simples es una buena opción virtual env ya que es más liviano
* Para proyectos que usen más servicios como una base de datos, resulta más cómodo usar Docker para el desarrollo 