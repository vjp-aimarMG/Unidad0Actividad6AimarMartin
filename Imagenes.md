1.   Primeramente tenemos que ejecutar el comando **docker run --name web -p 8000:80 -d php:7.4-apache** para levantar el contenedor
![](/img/imagenes/1.png)
![](/img/imagenes/2.png)
2. Ahora tendremos que crear el archivo **index.html** de la siguiente forma 
![](/img/imagenes/3.png)
* Una vez creado lo copiamos en la ruta **/var/www/html**
![](/img/imagenes/4.png)
* Para comprobarlo iremos al navegador y refrescamos la página
![](/img/imagenes/5.png)
3. Para el siguiente paso tendremos que hacer lo mismo que arriba, primero creamos el archivo con el contenido de la siguiente forma
![](/img/imagenes/6.png)
* Ahora lo pasaremos a la ruta raiz
![](/img/imagenes/7.png)
* Por último nos dirigimos al navegador y refrescamos la página
![](/img/imagenes/8.png)
4. Para crear el contenedor de base de datos tenemos que escribir el siguiente comando
![](/img/imagenes/9.png)
* Ejecutaremos **docker ps** para ver los contenedores que tenemos 
![](/img/imagenes/10.png)
* Por último entraremos en la base de datos con el usuario para ver que efectivamente nos podemos conectar, para ello usaremos el comando **mysql -h 127.0.0.1 -P 3336 -u invitado -p**
![](/img/imagenes/11.png)
* Ahora para visualizar será con **SHOW DATABASE**
![](/img/imagenes/12.png)
5. Lo último que haremos será intentar borrar el contenedor mariadb con el contenedor bbdd creado y veremos que nos da un error
![](/img/imagenes/13.png)