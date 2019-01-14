# Objetivos cubiertos en la decimotercera semana

## Entender el papel de los contenedores en la infraestructura virtual
Los contenedores aportan las siguientes ventajas ([según el tema correspondiente](http://jj.github.io/CC/documentos/temas/Contenedores)):
* Permite la _virtualización ligera_ sin necesidad de hipervisor ni de mecanismos hardware para funcionar. Su única limitación es que la
máquina invitada debe tener el mismo kernel y CPU que la máquina anfitriona.
* Permite aislar los recuros y manejarlos, algo muy conveniente en infraestructuras virtuales ya que mejora las prestaciones de estos.
* Permite trabajar con multitud de servicios y su despliegue en diferentes servicios en la nube.
* Permite el almacenamiento de datos para que sean fácilmente transferibles a otros entornos.

## Comprender los procesos de definición de contenedores
Se va a explicar la definición de contenedores en Docker:
En primer lugar hay que descargar la imagen que se va a utilizar para el contenedor. En este caso se utilizará Ubuntu:
```shell
$ sudo docker pull ubuntu
```
Además de descargar la imagen este comando la instalará. Para poder acceder al contenedor y provisionarlo ejecutaremos el siguiente
comando
```shell
$ sudo docker run -it ubuntu /bin/bash
```
que indica que se está ejecutando un comando interactivamente para crear un pseudo-terminal. Desde ahí se pueden ejecutar los comandos
necesarios para provisionar el contenedor. Por ejemplo:
```shell
$ sudo apt-get update
$ sudo apt-get install git
```
Una vez terminado de provisionar el contenedor basta con ejecutar el siguiente comando:
```shell
$ sudo docker stop ubuntu
```
Para realizar un contenedor de datos es necesario de un `Dockerfile`. Este fichero consta de las instrucciones necesarias para crear un
contenedor y realizar su provisionamiento. Un ejemplo de `Dockerfile` es el siguiente:
```
FROM busybox

WORKDIR /data
VOLUME /data
COPY ejemplo.json .
```
Este fichero básicamente crea un contenedor que empaqueta un archivo. Para lanzar este `Dockerfile` primero hay que crear el contenedor y luego ejecutarlo:
```shell
$ sudo docker build --tag=friendlyhello .
$ sudo docker run -p 4000:80 friendlyhello
```
Mediante `--tag` se le puede asignar un nombre al contenedor. La etiqueta `-p` sirve para redirigir un puerto del contenedor a la máquina anfitriona. Tras haberlo ejecutado este estará disponible en el puerto 4000.

## Análisis post-mortem del último hito
En el último hito se ha creado una segunda máquina virtual donde almacenar la base de datos que utiliza el servicio. Esta se ha provisionado con un `Vagrantfile` distinto al de la primera máquina virtual y se ha realizado una red privada entre ellas para su
conexión. Para más información se puede visitar [su página correspondiente](https://github.com/fpeiro/CC-proyecto/blob/gh-pages/hito5.md#entorno-multim%C3%A1quina).

## Alta en Docker Hub si no se ha hecho ya, así como instalación de las herramientas de Docker
Se ha creado una cuenta en Docker Hub tal y como se muestra en
[esta captura de pantalla](https://github.com/fpeiro/CC-ejercicios/blob/master/images/dockerhub.png). Además
[se ha instalado Docker CE](https://github.com/fpeiro/CC-ejercicios/blob/master/images/dockerce.png) para poder crear contenedores desde
el sistema operativo.
