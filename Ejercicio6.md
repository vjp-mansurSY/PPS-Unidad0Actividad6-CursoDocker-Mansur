# Sesión 6 - Creación de Imágenes

Para la realización de estos ejercicios es necesario tener una cuenta en Docker Hub.

## Creación de una imagen a partir de un contenedor

Arranca un contenedor desde una imagen base debian o ubuntu.

![](/imagenes/C63.png)

Instala los paquetes inetutils-ping, iproute2 y dnsutils con distintas herramientas de redes.

![](/imagenes/C64.png)

Crea una imagen a partir de este contenedor (recuerda que tienes que utilizar el nombre de tu usuario Docker Hub). La imagen se debe llamar <tu_usuario_docker_hub>/comandos_redes.

![](/imagenes/C65.png)

Sube la imagen a Docker Hub.

![](/imagenes/C66.png)

![](/imagenes/C67.png)



Descarga la imagen en otro ordenador donde tengas docker instalado, y crea un contenedor a partir de ella. (Si no tienes otro ordenador con docker instalado, borra la imagen en tu ordenador y bájala de Docker Hub).

![](/imagenes/C68.png)

![](/imagenes/C69.png)

## Creación de una imagen a partir de un Dockerfile
Crea una página web estática (por ejemplo busca una plantilla HTML5). O simplemente crea un index.html.

### Mi Página Web

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mi Página Web</title>
</head>
<body>
    <h1>Bienvenido a mi página web estática</h1>
    <p>Esta es una página servida por un contenedor Docker.</p>
</body>
</html>
```

Crea un fichero Dockerfile que permita crear una imagen con un servidor web sirviendo la página. Puedes usar una imagen base debian o ubuntu, o una imagen que tenga ya un servicio web, como hemos visto en el apartado Ejemplo 1: Construcción de imágenes con una página estática.

![](/imagenes/C70.png)

### Usa la imagen base de nginx
FROM nginx:alpine

### Copia el archivo HTML a la carpeta del servidor web de Nginx
COPY index.html /usr/share/nginx/html/

### Exponer el puerto 80 para acceder a la página web
EXPOSE 80

![](/imagenes/C71.png)

Ejecuta el comando docker que crea la nueva imagen. La imagen se debe llamar <tu_usuario_docker_hub>/mi_servidor_web.

![](/imagenes/C72.png)


Conéctate a Docker Hub y sube la imagen que acabas de crear.

![](/imagenes/C73.png)

![](/imagenes/C74.png)

Descarga la imagen en otro ordenador donde tengas docker instalado, y crea un contenedor a partir de ella. (Si no tienes otro ordenador con docker instalado, borra la imagen en tu ordenador y bájala de Docker Hub).

![](/imagenes/C75.png)

![](/imagenes/C76.png)
