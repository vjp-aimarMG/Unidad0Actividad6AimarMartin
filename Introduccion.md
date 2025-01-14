1. Para crear el contenedor tendremos que utilizar el comando **docker run -d -p 8181:80 --name servidor_web nginx**.
![](/img/introduccion/1.png)
* Después para comprobar que está corriendo ejecutaremos el comando **docker ps** y en la columna ***STATUS*** veremos que está como ***“Up”***
![](/img/introduccion/2.png)
2. Para acceder al servidor será tan sencillo como entrar a un navegador y escribir en el navegador el puerto que le hemos especificado al crearlo, que sería lo siguiente **localhost:8181**
![](/img/introduccion/3.png)
3. Con el comando **docker images** podremos listar todas las imágenes que tengamos cargadas
![](/img/introduccion/4.png)
4. Lo último que tendremos que hacer es borrar el contenedor, pero para ello antes tendremos que pararlo ya que lo tenemos corriendo. Para ello primero ejecutamos el comando **docker stop servidor_web** y después ya lo podremos borrar con el comando **docker rm servidor_web**
![](/img/introduccion/5.png)