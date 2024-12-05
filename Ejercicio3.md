# Sesión 3 - Almacenamiento

## Ejercicios para entregar

Crear los siguientes volúmenes con la orden docker volume: volumen_datos y volumen_web.

![](/imagenes/C15.png)

Una vez creados estos contenedores:

- Arrancar un contenedor llamado c1 sobre la imagen php:7.4-apache que monte el volumen_web en la ruta /var/www/html y que sea accesible en el puerto 8080.

![](/imagenes/C16.png)

- Arrancar un contenedor llamado c2 sobre la imagen mariadb que monte el volumen_datos en la ruta /var/lib/mysql y cuya contraseña de root sea admin.

![](/imagenes/C17.png)


Intenta borrar el volumen volumen_datos, para ello tendrás que parar y borrar el contenedor c2 y tras ello borrar el volumen.

![](/imagenes/C18.png)

Copia o crea un fichero index.html al contenedor c1, accede al contenedor y comprueba que se está visualizando.

![](/imagenes/C19.png)

Borra el contenedor c1 y crea un contenedor c3 con las mismas características que c1 pero sirviendo en el puerto 8081.

![](/imagenes/C20.png)


Captura de pantalla donde se puedan ver los dos volúmenes creados.

![](/imagenes/C21.png)

Captura de pantalla con la orden correspondiente para arrancar el contenedor c1 usando el volumen_web.

![](/imagenes/C22.png)

Captura de pantalla con la orden correspondiente para arrancar el contenedor c2 usando el volumen_datos.

![](/imagenes/C23.png)

Captura de pantalla donde se vea el proceso para poder borrar el volumen_datos.

![](/imagenes/C24.png)

Captura de pantalla donde se vea el borrado de c1 y la creación de c3.

![](/imagenes/C25.png)

Captura de pantalla donde se vea el acceso al contenedor c3.

![](/imagenes/C26.png)


## Bind mount para compartir datos

Crea una carpeta llamada saludo y dentro de ella crea un fichero llamado index.html con el siguiente contenido (Deberás sustituir ese XXXXXx por tu nombre.):

![](/imagenes/C27.png)

Una vez hecho esto arrancar dos contenedores basados en la imagen php:7.4-apache que hagan un bind mount de la carpeta saludo en la carpeta /var/www/html del contenedor. Uno de ellos vamos a acceder con el puerto 8181 y el otro con el 8282. Y su nombres serán c1 y c2.

![](/imagenes/C28.png)

![](/imagenes/C29.png)

![](/imagenes/C30.png)

Modifica el contenido del fichero ~/saludo/index.html.

![](/imagenes/C31.png)

Comprueba que puedes seguir accediendo a los contenedores, sin necesidad de reiniciarlos.

![](/imagenes/C32.png)

![](/imagenes/C33.png)

