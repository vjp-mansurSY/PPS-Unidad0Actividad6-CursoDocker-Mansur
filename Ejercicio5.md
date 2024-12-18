# Sesión 5 - Escenarios multicontenedor

## Despliegue de prestashop

Es esta tarea vamos a desplegar una tienda virtual construída con prestashop. Utilizaremos el fichero docker-compose.yml de Bitnami que podemos encontrar en la siguiente [URL](https://hub.docker.com/r/bitnami/prestashop).

Para obtener la imagen Docker de Bitnami PrestaShop lo haremos a través del siguiente comando:

![](/imagenes/C50.png)

![](/imagenes/C51.png)

![](/imagenes/C52.png)

![](/imagenes/C53.png)

Una vez hemos descargado el fichero docker-compose.yml asociado deberemos modificarlo de la siguiente manera:

Modificar los valores de las variables de entorno para conseguir lo siguiente:

* El usuario de prestashop para conectarse a la base de datos deberá ser pepe y su contraseña pepe. Investigar en la página de Dockerhub cuál es el nombre de las variables de entorno que debo modificar y/o añadir.
  
* Modificar el nombre de la base de datos de prestashop para que se llame mitienda. Debéis de modificar esos valores en los dos servicios. Investigar en la página de Dockerhub cuál es el nombre de las variables de entorno que debo modificar.
  
* Ten en cuenta que si tienes instalado docker en una máquina virtual y tienes que poner la IP de la máquina para acceder a los contenedores, debes modificar la variable de entorno PRESTASHOP_HOST para poner esa dirección ip.
  
* Por último, si tienes que repetir el ejercicio, borra el escenario con docker-compose down -v, para eliminar los volúmenes y que la modificación de la configuración se tenga en cuenta.

![](/imagenes/C54.png)


Levantar los contenedores:

![](/imagenes/C55.png)

Acceso desde el navegador a la aplicación.

![](/imagenes/C56.png)


## Despliegue de Nextcloud

Vamos a desplegar la aplicación nextcloud con una base de datos (puedes elegir mariadb o PostgreSQL) utilizando la aplicación docker-compose. Puedes coger cómo modelo el fichero docker-compose.yml el que hemos estudiado para desplegar WordPress.
  
* Dentro de un directorio crea un fichero docker-compose.yml para realizar el despliegue de nextcloud con una base de datos. Recuerda las variables de entorno y la persistencia de información.

![](/imagenes/C57.png)

* Levanta el escenario con docker-compose.

![](/imagenes/C58.png)

* Muestra los contenedores con docker-compose.

![](/imagenes/C59.png)

* Accede a la aplicación y comprueba que funciona.

![](/imagenes/C60.png)

* Comprueba el almacenamiento que has definido y que se ha creado una nueva red de tipo bridge.

![](/imagenes/C61.png)


* Borra el escenario con docker-compose.

![](/imagenes/C62.png)
