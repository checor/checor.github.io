---
layout: post
title: 'Notas sobre mi-ubicacion, web para ubicarse en #CPMX8'
published: true
excerpt_separator: <!--more-->
---

![Campus Party México]({{site.baseurl}}/images/cpmx8.jpg)

[Código fuente](https://github.com/checor/mi-ubicacion)

Revisando mis repositorios en Github (y fotos antiguas), recordé que en 2017 escribí una pequeña web para ubicarnos entre los 25,000 asistentes del Campus Party México 2017, en su tiempo, el evento de tecnología mas grande del país.

En este post explicaré un poco acerca del funcionamiento y del problema a resolver.

<!--more-->

## Motivación

La primera vez que asistí al Campus Party México, en su quinta edición, quedé maravillado por ver a tantas personas con intereses parecidos a los míos, con tantas horas de contenido, y lo mejor, convivir con toda la comunidad campusera. Cualquiera que haya asistido puede dar fe de ello. 

Me llamó la atención de que se usaba mucho Twitter para comunicarse entre todos los asistentes, en ese tiempo los hashtags estaban en pleno apogeo, y Twitter no tenía copiadas tantas cosas de Facebook, lo que la hacía ideal para transmitir mensajes a la comunidad, sin tener que seguirse en redes sociales o siquiera conocerse.

Con Twitter, podrías anunciar trueques, dinámicas, dádivas, o invitar a retas de videojuegos. Pero, ¿cómo ubicarse en el recinto? había cientos, si no es que miles, de personas instaladas en las larguísimas mesas de la arena. Era complicado decir: "**_estoy en la quinta mesa atrás del escenario X, estoy usando playera roja..._", así que me di a la tarea de escribir la página para ubicarnos por coordenadas. ¡Tweetea un link y comparte tu ubicación con todo el campus!

## Librerías utilizadas

Cabe resaltar que por ese entonces, aunque conocía un poco de desarrollo web, mi experiencia principal era como programador de embebidos, así que no tenía mucha idea de que tecnologías utilizar. Tras investigar un poco, me fui por las siguientes tecnologías:

* JS Vanilla: No conocía ninguna otra librería que jquery, y la tachaban de obsoleta.
* [Github Pages](https://pages.github.com/): ¿Publicar una página sin tener que pagar hosting, y desde Github? ¿Dónde firmo?
* [Skeleton](http://getskeleton.com/): No conocía de librerías CSS, y esta prometía ser simple y minimalista. Me flechó.

Después de elegir las herramientas a trabajar, tenía una incógnita, ¿cómo colocarle un marcador a un mapa? Después de googlear y parar en Stack Overflow varias veces, encontré que una opción era usar [Canvas](https://developer.mozilla.org/es/docs/Web/HTML/Canvas), ya que funcionaba con JS y con los últimos navegadores. Quería algo minimalista y que funcionara en la mayoría de equipos.

## Manos a la obra

Sobra decir que tenía el tiempo contado. Esta idea se me ocurrió el primer día del evento, y aunque encontré que tiempo atrás alguien había hecho una herramienta [similar](https://www.facebook.com/cpmx.michoacan/posts/291636991006950/), estaba caida y era para una edición anterior, por lo tanto tomé mis habilidades casi nulas de diseño y empecé a bocetar el mapa del campus. Una vez con el mapa hecho, lo coloqué en el canvas.

Una vez con el mapa hecho, empecé a escribir el código en Javascript, para que cada vez que alguien presionara la imagen, se mostrara el marcador en ese punto, así como la URL. Curiosamente, programar esta lógica se me hizo mas sencillo que la configuración inicial del canvas.

La última parte era la de twittear la ubicación. Si bien al día de hoy Twitter cambió o eliminó esta opción, tiempo atrás podrías crear un tweet agregando un parámetro _status=_ a la URL de Twitter. Seguro que existen mejores formas, pero esa me pareció sencilla.

Una vez hecho, tocaba anunciar su existencia. Y eso lo hice con mi primer [tweet](https://twitter.com/checor/status/883162559603331072) al respecto.

## Conclusiones

Una vez creada la herramienta, pudo servirle a decenas de campuseros para ubicarse entre ellos de forma mas rápida. Fue gratificante ver que la herramienta pasó en manos de varias personas, e incluso un par me agradecieron.

Aunque el código no es el mejor, me gustó el enfoque simple que le dí y como pude realizar este pequeño proyecto en una laptop viejita y Notepad++. Nada de Node, nada de frameworks de front end, usar sass, o minificar js... cosas que en su momento eran extrañas para mi, y seamos sinceros, por mas que uno avance en esto del desarrollo, puede que no las abarquemos por completo.

Y por supuesto, una vez que atravesemos la pandemia, me gustaría actualizar esta herramienta, para Campus Party o Talent Land.

¿Qué debería mejorar para que la herramienta sea mas moderna?
