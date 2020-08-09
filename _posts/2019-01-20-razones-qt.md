---
layout: post
published: true
title: 10 razones para utilizar Qt
excerpt_separator: <!--more-->
---
![Qt Framework]({{site.baseurl}}/images/qt.png)

Qt no es sólamente un framework, si estás trabajando en C++ y deseas tener una vida más fácil, Qt es El framework.

<!--more-->

Mi primer conocimiento del framework fue cercano al 2006, cuando el debate entre GNOME 2 y KDE estaban en pleno apogeo, sobre cual de los 2 era el mejor. Sin embargo, los toolkits con los que están creados, GTK+ y Qt, persiguen objetivos diferentes.

A continuación, listo algunas de mis razones favoritas por las cuales me gusta Qt y lo considero una opción fuerte viable para ciertos proyectos de software (y hardware).

# 1. Multiplataforma

Cuando utilizamos Qt, nuestro código correrá sin problemas en Windows, Linux y Mac OS; incluso sin problemas en Android, iOS y Windows Phone. Su soporte de plataformas es bastante similar a algunos lenguajes con máquina virtual.

# 2. Mas que sólo interfaz gráfica

La primera vez que escuché de Qt, siendo linuxero de la década pasada, me imaginaba que Qt era sólo una libería para interfaces gráfica, como lo es GTK. Para mi sorpresa, después de utilizarlo pro primera vez, Qt contiene una infinidad de elementos más, que envuelven a casi todo el lenguaje, como lo son:

- _Signals_ y _slots_ para comunicación entre objetos e hilos.
- Clases para leer, escribir y manejar JSON y XML
- Clases para hilos y concurrencia.
- Creación de DLL's y sistema de plugins.
- Herramientas para internacionalización.
- Suite para pruebas, destacando unitarias y de interfaz gráfica.
- Herramientas para empaquetar e instalar el nuestras aplicaciones.
- Librerías para comunicación en red.
- Creador de imágenes linux personalizadas con Yocto.

En fin, que Qt contiene casi todo lo que uno puede esperar de algún lenguaje, sin tener que recurrir a módulos o librerías de terceras personas. De las pocas herramientas que podría echar de menos, son, alguna herramienta para _coverage_ (cobertura), y quizá un algún protocolo más para comunicación de redes industriales.

# 3. Qt Creator

**Qt Creator** es el IDE que te incluye Qt para realizar tus desarrollos. Al principio, por su apariencia me pareció un editor muy sencillo, pero luego de poder probarlo más a fondo, descrubrí que no tiene nada que envidiarle a cualquier otro IDE o editor de texto actual.

Aunque algunas de sus funcionalidades están pensadas para Qt, en realidad se puede utilizar como cualquier otro editor de C++. Yo lo he utilizado sin problemas para aplicaciones de OpenCV que no necesito de Qt.

# 4. Múltiples kits para interfaces de usuario

Qt tiene una ración de librerías para crear interfaces gráficas. Desde la inicial, **Qt Widgets**, que nos permite crear una aplicación de escritorio "clásica"; **Qt Quick**, que nos permite crear interfaces mas modernas y personalizables utilizando un dialecto de JavaScript (!).

Incluso tiene algunas maravillas, las cuales no he utilizado a fondo, como **Qt WebEngine**, que nos muestra una interfaz web como cualquier navegador; **Qt WebChannel**, que permite comunicar código C++ en _back-end_ con JS en el _front_, y actualmente tienen en pruebas **Qt for WebAssembly**, que como su nombre indica, permitirá cargar nuestra aplicación Qt completamente en un navegador web. 

Esto permite que incluso desarrolladores que no trabajan en C++ y se dediquen más a la parte del frente de una aplicación, realizarlo sin problemas.

# 5. Bindings para diferentes lenguajes

Ya vimos que en la interfaz gráfica, se puede utilizar Qt sin utilizar C++, pero gracias a sus _bindigs_, también se pueden utilizar otros lenguajes sin mayor problemas.

Uno de los más utilizados es Qt para **Python**, (PyQt o Pyside), que agregan la mayoría de la funcionalidad de interfaces y objetos a este lenguaje. Cabe señalar que en algún momento estos bindings tienen algunas licencias las cuales pueden no ser compatibles con nuestro desarrolllo.

También existen para Rust, Mono, Node.js, Go, entre otros.

# 6. Soporte para embebidos

En sistemas embebidos, (sistemas autónomos que normalmente tienen poca potencia, como puede ser un kiosko, un verificador de precios, un autoestéreo, un punto de venta...), es uno de los aspectos en los cuales Qt en los últimos años se ha ido puliendo.

Dadas las bondades del lenguaje y de Qt, con el se puede realizar una aplicación con una interfaz agradable, y con pocos requerimientos de CPU y memoria. Afortunadamente, en el desarrollo de un par de aplicaciones para embebidos, que he trabajado,  el cliente ha quedado maravillado de como el costo del hardware se reduce.

Uno podría estar tentado a utilizar herramientas más de "moda" como alguna webapp con **HTML5** para estos sistemas, pero aquí el buen uso de los recursos limitados pasa factura.

# 7. Soporte industrial

Este es otro aspecto importante de Qt. Al momento de estar trabajando con Qt por el 2016, hubo una librería que me cayó como maná del cielo. Modbus para Qt.

Quizá algunos desarrolladores que no interactúan con el área industrial y de manufactura les suene el protocolo anterior. Pues bien, este permite comunicarse sin dolor con una buena cantidad de PLC's, esos cachivaches que uno encuentra en una planta que hacen que alguna maquinaria funcione, como puede ser una máquina de galletas o embotelladora. Tiene 2 sabores TCP y Serial, dependiendo su conexión.

También cuenta con el protocolo CANBus, utilizado fuertemente en el área automotriz. Por eso no es de sorprendernos que encontremos Qt en algunos autoestéreos.

Y por último, el viejo protocolo Serial RS232, que se resiste a morir y que uno lo encuentra más de lo que uno desearía en plantas. Tiene varios elementos de configuración, así que alguna vez tuviste algún dispositivo o cable RS232 que no funcionaba bien, te invito a que pruebes tratando de utilizarlo con Qt. Puede que te encuentres con alguna sorpresa.

# 8. Multilenguaje sin dolor.

Qt, cuenta con clases para poder definir que un texto podrá o deberá mostrarse en otro idioma, en caso de ser necesario. Esto es algo común en muchos lenguajes y frameworks.

Lo interesante de esto, es que Qt cuenta con una herramienta llamada Qt Linguist, la cual permite tomar uin diccionario con frases, y traducirlas al lenguaje deseado. Esto, con interfaz sencilla, para que pueda hacerlo alguien sin necesidad de conocer como programar o que es Qt. Incluso permite agregar comentarios a cada frase, para que sean de apoyo al traductor.

# 9. Sintaxis moderna

Qt permite utilizarle con compiladores que soporten C++11, C++14, e incluso C++17. En mi caso, antes de conocer C++11, para mi este lenguaje no me era muy atractivo, exisitiendo tanta oferta con diferentes características, pero al conocer algunas de las bondades de C++11, como el uso de funciones _lambda_, _smart pointers_, y la detección de tipo de dato mediante _auto_, me dejó claro que includo un "dinosaurio" como C++ se puede actualizar, y darnos elementos que pueden darnos un desarrollo mas placentero, comparado con C++98.

Todos estos cambios, entran sin que afecte el desarrollo con Qt.

# 10. Documentación de calidad

Por último, y no por eso menos importante, la documentación es un elemento clave para comprender un framework y poder utilizarlo sin problemas.

La documentación tiene una infinidad de ejemplos y páginas, donde se puede ir explorando las cualidades sin perderse tanto, como me ha pasado con algunos otros frameworks. Así también, cuando uno descarga Qt, tiene una copia de toda la documentación en el IDE, que me ha salvado más de una vez que me encontré sin wifi.

# Comentarios finales

Para mi, Qt es una herramienta no muy conocida, que me ha funcionado de maravilla en más de una ocasión. C++ no es un lenguaje que actualmente esté bajo los reflectores, pero tiene un gran área de utilidad que no se debe ignorar. Como los sabiduría popular pregona, una herramienta no es la ideal para todas las soluciones. ¿Has utilizado Qt en algún desarrollo o lo planeas utilizar? ¡Cuéntame!
