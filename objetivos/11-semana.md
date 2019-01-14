# Objetivos cubiertos en la undécima semana

## Entender los recursos para automatización de actividades en la nube
Para automatizar actividades en la nube podemos realizar alguna de las siguientes alternativas:
* Acceder a los servicios en la nube desde su interfaz gráfica y realizar las operaciones de manera manual.
* Instalar las interfaces de línea de comandos de los servicios y ejecutar los comandos necesarios para su automatización. Se pueden crear
_scripts_ para programar secuencias de comandos que realicen tareas más complejas.
* Instalar herramientas de creación y configuración de entornos de desarrollo virtualizados como Vagrant para realizar estas tareas a más
alto nivel y haciendo uso de comandos más básicos.

Como complemento se puede utilizar software de provisionamiento de máquinas virtuales como Ansible para desplegar servicios en estas
máquinas.

## Entender el concepto de infraestructura definida por software

Según [la Hewlett Packard Enterprise](https://www.hpe.com/es/es/what-is/software-defined-infrastructure.html) la infraestructura definida
por software es aquella cuyos recursos informáticos, de red y almacenamiento se agrupan de manera lógica y pueden gestionarse como si de
software se tratase permitiendo el provisionamiento de infraestructura basado en políticas y que permite la automatización de tecnologías
de la información.

La infraestructura definida por software proporciona unos modelos de consumo de tecnologías de la información simplificados y
estandarizados, un sistema de configuración, copia de seguridad y recuperación de datos automática, una gestión sencilla y una gestión
híbrida de la nube completamente integrada.

## Probar diferentes proveedores de nube y ver las posibilidades que ofrecen
Por ahora se ha utilizado únicamente Azure para la automatización de máquinas virtuales. Utilizar Azure tiene 
[las siguientes ventajas](https://azure.microsoft.com/es-es/overview/azure-vs-aws/):
* Incluye Windows Server y SQL Server de manera gratuita.
* Permite la utilización de todos los sistemas operativos, lenguajes y herramientas de código abierto necesarias. Es además la única nube
con soporte integrado para RedHat.
* Dispone de más regiones globales que cualquier otro proveedor de servicios en la nube.
