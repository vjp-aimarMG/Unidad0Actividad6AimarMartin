# Creación de una imagen a partir de un contenedor
1. Lo primero que haremos será arrancar un contenedor con el comando **docker run -it --name contenedor_redes debian bash**
![](/img/creacion_imagenes/1.png)
2. Una vez dentro actualizaremos el repositorio e instalaremos los paquetes necesarios
![](/img/creacion_imagenes/2.png)
* De manera opcional podemos comprobar que se ha instalado correctamente
![](/img/creacion_imagenes/3.png)
3. Ahora crearemos la imagen con el comando **docker commit contenedor_redes vjp-aimarMG/comandos_redes**
![](/img/creacion_imagenes/4.png)
4. Iniciaremos sesión en DockerHub con el comando **docker login**
![](/img/creacion_imagenes/5.png)
5. Una vez tengamos iniciada la sesión subiremos la imagen con el comando **docker push vjp-aimarMG/comandos_redes**
![](/img/creacion_imagenes/6.png)
6. Como no tengo otra máquina borraré la imagen y me la volveré a bajar de DockerHub
#### Borrado:
![](/img/creacion_imagenes/7.png)
#### Descarga:
![](/img/creacion_imagenes/8.png)
7. Por último crearemos un contenedor a partir de la imagen descargada
![](/img/creacion_imagenes/9.png)