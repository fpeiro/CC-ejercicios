# Objetivos cubiertos en la cuarta semana

## Entender las arquitecturas de software en la nube de uso en la actualidad
Se ha leído el [primer tema](http://jj.github.io/CC/documentos/temas/Arquitecturas_para_la_nube) de teoría de la asignatura donde se
especifican distintas arquitecturas para el desarrollo de software en la nube.
* Arquitectura en capas, desarrollo natural de la arquitectura cliente-servidor, creando 3 o más capas entre las que se suele incluir la
capa de presentación, la de aplicación, la de lógica de negocio y la de acceso a datos.
* Arquitectura dirigida por eventos que dispone de una cola de eventos, que se originan en el usuario, pero también de una parte a otra de
la arquitectura en la cual diferentes procesadores de eventos van extrayendo eventos de la cola y procesándolos de forma asíncrona.
* Arquitectura microkernel. Es más o menos monolítica, con un núcleo central al que se pueden añadir funcionalidades mediante plugins.
* Arquitectura basada en microservicios. Se trata de unidades que se van a desplegar de forma independiente, diferentes servicios que
trabajarán de forma totalmente independiente unos de otros.
* Arquitectura basada en espacios. En esta, un espacio es compartido por una serie de unidades de procesamiento, que se comunican entre sí
principalmente a través de ese espacio.

## Comprender el paper fundamental de la infraestructura virtual en este proceso
En la página de [Infraestructura como servicio (IaaS)](https://es.wikipedia.org/wiki/Infraestructura_como_servicio_(IaaS)) de la Wikipedia
podemos sacar la conclusión de que la infraestructura virtual permite que el desarrollador no necesite de ningún hardware para alojar la
aplicación y, debido a eso, no debe preocuparse del mantenimiento ni suministro de este.

De esta manera la IaaS permitiría aprovisionar el procesamiento, almacenamiento, redes y otros recursos informáticos fundamentales donde el
consumidor puede implementar y ejecutar software arbitrario, que puede incluir sistemas operativos y aplicaciones. Ahí, el consumidor no
administra ni controla la infraestructura de la nube subyacente, pero tiene control sobre los sistemas operativos, el almacenamiento y las
aplicaciones implementadas; y posiblemente control limitado de componentes de red seleccionados (por ejemplo, firewalls de host).

## Entender en qué consiste los servicios web y cómo desplegarlos en la nube
Según la página de la Wikipedia [Computación en la nube](https://es.wikipedia.org/wiki/Computaci%C3%B3n_en_la_nube) un servicio web es
aquel que se encuentra en Internet y que atiende peticiones en cualquier momento desde un servidor. Se puede tener acceso a su
información desde cualquier dispositivo ubicado en cualquier lugar. Sirven a sus usuarios desde varios proveedores de alojamiento
repartidos frecuentemente por todo el mundo. Gracias a esto se reduce costes, se garantiza un mejor tiempo de actividad y una menor
vulnerabilidad a ataques.

## Tener manejo básico de los lenguajes usados en herramientas de provisionamiento, Python y Ruby
En la asignatura impartida en el Grado de Ingeniería Informática de la Universidad de Jaén llamada
[Procesamieno del Lenguaje Natural](https://github.com/fpeiro/CC-ejercicios/blob/master/docs/2017-18-13313010_es.pdf) aprendí cómo a
utilizar el lenguaje de programacion Python. Entre otras cosas aprendí a leer y escribir ficheros, tratar y clasificar textos, así como
extraer información de ellos.

En Ruby en cambio, no tengo experiencia previa aunque hay
[distintos manuales](http://es.tldp.org/Manuales-LuCAS/doc-guia-usuario-ruby/guia-usuario-ruby.pdf) para aprender.

## Darse de alta en servicios PaaS como zeit.co y Heroku
Se ha dado de alta tanto en [zeit.co](https://github.com/fpeiro/CC-ejercicios/blob/master/images/zeit-co.png) como en
[Heroku](https://github.com/fpeiro/CC-ejercicios/blob/master/images/heroku.png) para la realización de las prácticas.

## Entender por qué no se hace git pull sino git pull --rebase y como arreglarlo en ese caso usando un squash commits con git rebase -i
La primera de ellas necesita de un commit para descargar los cambios mientras que en la segunda no. Esto es problemático cuando se está
trabajando con un fork pues al hacer pull request se realizarán commits que no provocan ningún cambio.

## Proponer temas para el siguiente seminario/recuperación
Podría realizarse un seminario sobre Travis para la realización de tests en GitHub.
