# Redes docker
1. Lo primero que tendremos que hacer para la creación de la red1 y red2 será escribir los siguientes comandos para poder crearlas con los requisitos especificados 
![](/img/redes/t1.png)
![](/img/redes/1.png)
2. El siguiente paso para poner en ejecución un contenedor será escribir el siguiente comando para poder crearlo con las especificaciones correctas
![](/img/redes/t2.png)
![](/img/redes/2.png)
3. Para entrar al contenedor deberíamos ejecutar el comando **docker exec -it u1 bash** lanzando un bash para poder ejecutar comandos dentro de él e instalar ping
![](/img/redes/3.png)
* Después haremos un **update** y la propia instalación de **ping**
![](/img/redes/4.png)
4. Para crear el contenedor u2 lo haremos de la misma manera que en el paso 2 con la diferencia de que no escribiremos la ip y lo conectaremos a la red2
![](/img/redes/t3.png)
![](/img/redes/5.png)
5. Para entrar al contenedor deberíamos ejecutar el comando **docker exec -it u2 bash** lanzando un bash para poder ejecutar comandos dentro de él e instalar ping
![](/img/redes/6.png)
* Después haremos un **update** y la propia instalación de **ping**
![](/img/redes/7.png)
* Ahora vamos a comprobar que desde u1 no somos capaces de hacer ping ni con el nombre ni con la ip, para ello primero vamos a ver la ip que le asignó docker a u2 con el comando **docker inspect u2**
![](/img/redes/8.png)
* Una vez lo tengamos vamos a volver a conectarnos a u1 con **docker exec -it u1 bash** y ejecutar tanto **ping 172.19.0.2** como **ping host2**
![](/img/redes/9.png)
* Para el siguiente ejemplo tendremos que conectar u1 a la red2, para ello ejecutamos el comando **docker network connect red2 u1**
![](/img/redes/10.png)
* Una vez conectado volvemos a ejecutar **ping 172.19.0.2** como **ping host2** y vemos que ahora si se encuentran
![](/img/redes/11.png)

# Despliegue de Nextcloud + mariadb/postgreSQL
1. Lo primero será crear la red bridge con el comando **docker network create --driver bridge red_nextcloud**
![](/img/redes/12.png)
2. Lo siguiente será crear un volumen con **docker volume create mariadb_data**
![](/img/redes/13.png)
* Después vamos a crear un contenedor para la base de datos
![](/img/redes/t4.png)
![](/img/redes/14.png)
3. Para la creación del contenedor de nextcloud será de la misma forma que el punto anterior, primeramente con **docker volume create nextcloud_data** el volumen
![](/img/redes/15.png)
* Y para el contenedor sería con el siguiente
![](/img/redes/t5.png)
![](/img/redes/16.png)
4. Por último desde el navegador entramos al puerto **8081** y podemos apreciar que nos carga la página de **nextcloud**
![](/img/redes/17.png)