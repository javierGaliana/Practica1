Práctica 1 de la asignatura Infraestructura Virtual
===================================================
- Autor: Javier Galiana Romero
- correo: jagaro@correo.ugr.es
- Licencia: GPLv3

Aplicación realizada
--------------------
La aplicación usada sobre esta aplicación ha sido la página web que se creo en el curso 2012/2013 para la asignatura TW. Dicha aplicación se ha montado en el PAAS Pagoda Box(<a>www.pagodabox.com</a>)
Para crear una aplicación se podía hacer directamente sobre un repositorio de github.

Realización
-----------
Para la realización de la práctica se ha usado un módulo de web, un módulo de base de datos y otro módulo de caché.

Para poder establecer las preferencias de estos módulos cuando se montan se debe de crear un archivo llamado Boxfile en el directorio raíz. Esta información serían los metadatos. El formato seguido sería yumla(<a>yaml.org/start.html</a>) Las opciones necesarias a incluir son las extensiones php que son las librerías que se instalan con el módulo de web( plataforma PHP) y además indicar cual es el archivo index de nuestra web.

Para crear la base de datos hay que seguir un tutorial que te explica como acceder remotamente a tu base de datos mediante un túnel(<a>help.pagodabox.com/customer/portal/articles/175427</a>).

En cambio realizar el módulo de caché es sencillo y necesario, ya que una vez montada la aplicación sus directorios se vuelven de sólo lectura excepto que crees un módulo de caché que es donde se guardará toda la información dinámica. En este caso también es interesante indicar en la etiqueta web1 las carpetas que serán compartidas y con derecho de escritura que tendrán en común todas las instancias de nuestra aplicación.

Interacción con los repositorios
--------------------------------
En esta ocasión tenemos la posibilidad de ligar nuestro directorio al repositorio de la aplicación en pagoda. Haciendo esto cuando hacemos un push se hace directamente sobre dicho repositorio y lo monta para poder ejecutarlo.

Para configurar el repositorio sería:

git remote add pagoda git@git.pagodabox.com:periodico

Haciendo ahora <i>push pagoda master</i> actualizamos los archivos y montamos nuestra aplicación. 

Conclusiones
------------
El Paas es intuitivo pero complejo en algunos conceptos. También existe poca documentación y es difícil encontrar ejemplos lo cual dificulta el aprendizaje. En cambio, es intuitivo a nivel de configuración básica y permite una vez aprendido gestionar los cambios rápidamente.
