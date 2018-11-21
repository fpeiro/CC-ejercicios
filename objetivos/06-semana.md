# Objetivos cubiertos en la sexta semana

## Aprender a usar diferentes sistemas de provisionamiento de máquinas virtuales en la nube
Gracias al [seminario realizado de Ansible](https://youtu.be/gFd9aj78_SM) se ha conocido la configuración de este sistema de
provisionamiento, así como la importancia del inventariado y la instalación de gemas en él.

## Entender los diferentes conceptos subyacentes: servicio, estado
Se ha leído el artículo
[Definición de servicios web de estado frente a sin estado](https://nordicapis.com/defining-stateful-vs-stateless-web-services/) donde
se definen dichos conceptos como comparación de los servicios web que utilizan servicios frente a aquellos que utilizan estados como
almacenamiento de datos de los usuarios. Estos difieren en que:
* Los servicios web que hacen uso de estados almacenan en el servidor un estado del usuario conectado que realiza un seguimiento de la
sesión del usuario hasta su desconexión.
* Los que no hacen uso de estos almacenan una cookie en el navegador que permite registrar en todo momento que las acciones que la
contiene las realiza el mismo usuario.

## Entender el concepto de servicio web
En el [sitio web de IBM](https://www.ibm.com/support/knowledgecenter/es/SSMKHH_9.0.0/com.ibm.etools.mft.doc/ac55710_.htm) podemos
encontrar la definición de servicio web de la W3C. La W3C define un servicio web como un sistema de software designado para dar soporte
a la interacción de máquina a máquina interoperativa a través de una red. Este realiza una tarea específica o un conjunto, y se describe
mediante el estánda Web Services Description Language. Estos sistemas pueden hacer uso de mensajes SOAP para interactuar con el servicio
web, normalmente utilizando HTTP.

## Entender qué es lo que se requiere en el hito 2 y las diferentes capas
La realización del hito 2 de mi proyecto puede encontrarse en [este enlace](https://github.com/fpeiro/CC-proyecto). Para su realización
se han abordado los siguientes temas:
* Clase/Módulo + Test: Se definen pruebas sobre las diferentes funcionalidades del microservicio para comprobar que los resultados que
devuelve son los esperados.
* Servicio web + Test: Se definen pruebas sobre las diferentes rutas presentes en el microservicio con el fin de verificar que estas se
han implementado correctamente.
* Travis (para ejecutar los tests): El objetivo de Travis es corroborar que los test se han resuelto correctamente cuando el código del
microservicio ha cambiado.
* Descripción de la infraestructura virtual: Han de describirse los servicios de los que consta el microservicio así como la
comunicación y almacenamiento de los datos que van a utilizarse.

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

## Aprender lo suficiente de los lenguajes de programación usados por los sistemas de aprovisionamiento para entender el Domain Specific Language usado por los mismos
Ansible permite el uso de múltiples lenguajes de programación como Ruby o Python. De estos lenguajes
[ya se ha detallado](https://github.com/fpeiro/CC-ejercicios/blob/master/objetivos/04-semana.md#tener-manejo-b%C3%A1sico-de-los-lenguajes-usados-en-herramientas-de-provisionamiento-python-y-ruby)
el dominio que se tiene sobre ellos.

## Decidir sobre el próximo seminario (19 de noviembre)
En clase se decidió que el seminario del 19 de noviembre iba a estar destinado a la explicación del software de negociación de mensajes
(broker) RabbitMQ.
