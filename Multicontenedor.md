# Despliegue de Nextcloud
1. Lo primero será descargar el docker-compose, para ello ejecutaremos el comando **sudo curl -L "https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose** y le concederemos permisos
![](/img/multicontenedor/1.png)
2. Después crearemos el archivo **docker-compose.yaml**
![](/img/multicontenedor/2.png)
3. Una vez creado iniciamos los servicios
![](/img/multicontenedor/3.png)
4. Para mostrar los contenedores será con **docker-compose ps**
![](/img/multicontenedor/4.png)
5. Para poder comprobar que nos funciona correctamente buscaremos en el navegador el puerto 8082
![](/img/multicontenedor/5.png)
6. Podemos comprobar que se ha creado una red de tipo *bridge* con **docker network ls**
![](/img/multicontenedor/6.png)
7. Para borrar el escenario será con **docker-compose down**
![](/img/multicontenedor/7.png)