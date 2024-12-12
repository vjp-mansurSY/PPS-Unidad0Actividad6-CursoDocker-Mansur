# Sesión 4 - Redes

## Ejercicios para entregar

### Trabajar con redes docker 

Vamos a crear dos redes de ese tipo (BRIDGE) con los siguientes datos:

Red1
    * Nombre: red1
    * Dirección de red: 172.28.0.0
    * Máscara de red: 255.255.0.0
    * Gateway: 172.28.0.1

![](/imagenes/C34.png)

Red2
    * Nombre: red2    
    * El resto de los datos será proporcionados automáticamente por Docker.

![](/imagenes/C35.png)

Poner en ejecución un contenedor de la imagen ubuntu:20.04 que tenga como hostname host1, como IP 172.28.0.10 y que esté conectado a la red1. Lo llamaremos u1.

![](/imagenes/C36.png)

Entrar en ese contenedor e instalar la aplicación ping (apt update && apt install inetutils-ping).

![](/imagenes/C37.png)
    
Poner en ejecución un contenedor de la imagen ubuntu:20.04 que tenga como hostname host2 y que esté conectado a la red2. En este caso será docker el que le de una IP correspondiente a esa red. Lo llamaremos u2.

![](/imagenes/C38.png)
    
Entrar en ese contenedor e instalar la aplicación ping (apt update && apt install inetutils-ping).

![](/imagenes/C39.png)

Captura de pantalla donde se vea la configuración de red del contenedor u1.

![](/imagenes/C40.png)

Captura de pantalla donde se vea la configuración de red del contenedor u2.

![](/imagenes/C41.png)

Captura de pantalladonde desde cualquiera de los dos contenedores que se pueda ver que no podemos hacer ping al otro ni por ip ni por nombre.

![](/imagenes/C42.png)

Captura de pantalla donde se pueda comprobar que si conectamos el contenedor u1 a la red2 (con docker network connect), desde el contenedor u1, tenemos acceso al contenedor u2 mediante ping, tanto por nombre como por ip.

![](/imagenes/C43.png)

### Despliegue de Nextcloud + mariadb/postgreSQL

Vamos a desplegar la aplicación nextcloud con una base de datos (puedes elegir mariadb o PostgreSQL) (NOTA: Para que no te de errores utiiliza la imagen mariadb:10.5). Te puede servir el ejercicio que hemos realizado para desplegar Wordpress. 

Para ello sigue los siguientes pasos:

- Crea una red de tipo bridge.

![](/imagenes/C44.png)

Crea el contenedor de la base de datos conectado a la red que has creado. La base de datos se debe configurar para crear una base de dato y un usuario. 

Además el contenedor debe utilizar almacenamiento (volúmenes o bind mount) para guardar la información. 

Puedes seguir la documentación de mariadb o la de PostgreSQL.

![](/imagenes/C45.png)

![](/imagenes/C46.png)

A continuación, siguiendo la documentación de la imagen nextcloud, crea un contenedor conectado a la misma red, e indica las variables adecuadas para que se configure de forma adecuada y realice la conexión a la base de datos. 

El contenedor también debe ser persistente usando almacenamiento.

![](/imagenes/C47.png)

![](/imagenes/C48.png)

Accede a la aplicación usando un navegador web.

![](/imagenes/C49.png)

