# Creación y uso de volúmenes
1. Lo primero que tendremos que hacer es crear los volúmenes con **docker volume create volumen_datos docker volume create volumen_web** y comprobamos que se hayan creado
![](/img/almacenamiento/1.png)
2. Lo siguiente será arrancar los contenedores, para ello lo haremos de la siguiente forma
![](/img/almacenamiento/2.png)
* Comprobaremos que se han creado con **docker ps**
![](/img/almacenamiento/3.png)
3. Para borrar el volumen tendremos que parar el contenedor y después borrarlo
![](/img/almacenamiento/4.png)
* Ahora ya sí dejará borrar el volumen y lo comprobaremos
![](/img/almacenamiento/5.png)
4. Ahora lo que vamos a hacer será entrar al contenedor c1 y crear el archivo **index.html**
![](/img/almacenamiento/6.png)
* Ahora entramos al navegador por el **puerto 8080** y comprobamos que funcione
![](/img/almacenamiento/7.png)
5. Para este paso lo que vamos a hacer es parar y borrar el contenedor **c1**
![](/img/almacenamiento/8.png)
* Ahora vamos a crear el contenedor **c3** pero usando el volumen que teníamos para el **c1**
![](/img/almacenamiento/9.png)
* Por último comprobamos que se haya creado 
![](/img/almacenamiento/10.png)

# Bind mount para compartir datos
1. Lo primero será crear una carpeta con **mkdir** y después usando **echo** creamos el fichero y lo añadimos a la carpeta. Como paso opcional será ejecutar un **cat** para visualizar el fichero
![](/img/almacenamiento/11.png)
2. Para el siguiente paso tendremos que ejecutar los siguiente dos comandos para crear los contenedores
![](/img/almacenamiento/12.png)
* Como paso adicional usaremos **docker ps** para comprobar que se han creado
![](/img/almacenamiento/13.png)
* Ahora vamos al navegador y vemos si se visualiza bien
![](/img/almacenamiento/14.png)
![](/img/almacenamiento/15.png)
3. Vamos a modificar el **index.html**, para ello usamos **nano saludo/index.html**
![](/img/almacenamiento/16.png)
4. Sin reiniciar el servidor ni nada iremos al navegador y refrescando la pantalla veremos que siguen siendo accesible y además se han aplicado las modificaciones
![](/img/almacenamiento/17.png)
![](/img/almacenamiento/18.png)