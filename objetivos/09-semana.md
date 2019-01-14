# Objetivos cubiertos en la novena semana

## Tener listos diferentes sistemas cloud donde se puedan desplegar máquinas virtuales
En Azure poseo una cuenta personal donde poder desplegar las máquinas virtuales necesarias para la asignatura. Se posee además una
[suscripción](https://github.com/fpeiro/CC-ejercicios/blob/master/images/azure.png) para poder hacer uso de estas.

## Conocer diferentes lugares donde haya imágenes de sistemas operativos listas para usar
En [FreeOS](http://www.freeos.com) podemos encontrar multitud de enlaces a sistemas operativos gratuitos para descargar.

## Instalar y configurar diferentes sistemas de provisionamiento
Se ha instalado [Ansible en Windows 10](https://github.com/fpeiro/CC-ejercicios/blob/master/images/ansible.PNG) a través del subsistema
de Linux. Para ello se han ejecutado los siguientes comandos:
```console
$ sudo apt-add-repository ppa:ansible/ansible
$ sudo apt-get install ansible
```
Preparamos además una configuración básica para él.
```console
[defaults]
host_key_checking = False
inventory = ./ansible_hosts
```

## Entender los conceptos de los sistemas de máquinas virtuales y cómo configurarlos desde línea de órdenes
En la página [Máquina virtual de la Wikipedia](https://es.wikipedia.org/wiki/M%C3%A1quina_virtual#M%C3%A1quinas_virtuales_de_sistema) se
explica que las máquinas virtuales de sistema son sistemas hardware que pueden crear múltiples instancias de máquinas virtuales. Esta costa
de una capa software llamada monitor de máquina virtual o hipervisor.

Para configurarlos desde la línea de órdenes podemos utilizar Ansible. Gracias a Ansible se pueden desplegar servicios sobre ellos. La
instalación y configuración básica de este se puede encontrar en el punto anterior. Con Vagrant además podemos automatizar la creación de
estas máquinas virtuales. Para instalar Vagrant se necesitan de los siguientes comandos:
```console
$ sudo apt-get install vagrant
```
Preparamos además una configuración básica para él.
```console
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
    config.vm.box = "hashicorp/precise32"
end
```

## Entender las nociones básicas de seguridad
Para crear sistemas cloud hay que tener en cuenta las siguientes consideraciones:
* Actualizar el sistema para aplicar los parches de seguridad.
* Realizar siempre conexiones a través de SSH cifrado con clave.
* No almacenar nunca la clave privada en el sistema.

## Instalarse los diferentes clientes de líneas de órdenes de los sistemas en la nube a los que se tenga acceso
Se ha instalado la interfaz de línea de comandos de Azure para la realización de las prácticas. La captura de pantalla que lo prueba se puede ver [aquí](https://github.com/fpeiro/CC-ejercicios/blob/master/images/azurecli.png).

## En la sesión del jueves, comentar los fallos más habituales en el hito
En clase expliqué los problemas que tenía con el almacenamiento de variables en Heroku y Azure que me impedía conectarme a la base
de datos sin almacenar la contraseña.
