# Contenido multimedia

Es muy común ver contenido de multimedia (como imágenes, videos, etc.) en páginas web. En este apartado se hablará de dichos elementos, de cómo introducirlos a la página y de algunas opciones de personalización a través de HTML.

<p id="indice">He aquí un pequeño índice del contenido a mostrar en este apartado:</p>

* [IMÁGENES](#imagenes)
  * [Formatos de imagen permitidos](#img-format)
  * [Sintaxis](#sintaxis)
  * [Formas de introducir una imagen](#formas)
  * [Definir el tamaño de una imagen](#size)
  * [Float](#float)
* [VÍDEOS](#videos)
* [AUDIOS](#audios)

<br>

<sub>* [Ver código](./multimedia.html)</sub>

[<< TEMA 2](../02-Formularios_y_tablas/README.md#formularios-y-tablas) | [INICIO](../../README.md#temario-del-curso---teoria) | [TEMA 4 >>](../04-Hojas_de_estilo/README.md#introducción-a-css)


<br><hr>
<hr><br>


<h2 id="imagenes">Imágenes</h2>

Las imágenes son elementos muy útiles y súper utilizados a la hora de crear y diseñar una página web. Ayudan mucho tanto para explicar diferente contenido como para simplemente decorar la página.

A continuación, se hablará de diferentes posibilidades a la hora de introducirlas a la web, la sintaxis necesaria y algunos atributos que nos permitirán darles el formato deseado.


<br><hr>


<h3 id="img-format">Formatos de imagen permitidos</h3>

En primer lugar, hay que tener en cuenta que no todos los formatos de imagen son permitidos en todos los buscadores. He aquí una lista de los formatos más utilizados que sí se pueden utilizar en todos ellos:

* APNG (.apng)
* GIF (.gif)
* ICO (.ico, .cur)
* JPEG (.jpg, .jpeg, .jfif, .pjpeg, .pjp)
* PNG (.png)
* SVG (.svg)

<br>

<sub>[Volver al índice](#indice) | [Vídeos](#videos)</sub>


<br><hr>


<h3 id="sintaxis">Sintaxis</h3>

Para "introducir" una imagen se utiliza la etiqueta `<img>`, la cual crea un espacio para la imagen a la que hace referencia.

Esta etiqueta no tiene otra etiqueta de cierre, en su interior contiene los atributos necesarios para referenciar la imagen. Estos son los **atributos obligatorios**:

* `src`: especifica la dirección de la imagen.
* `alt`: contiene un texto alternativo por si la imagen no es cargada o el usuario contiene un lector de páginas web.

<br>

He aquí un ejemplo simple:

```HTML
<img src="myDog-img.pnj" alt="foto de mi perro">
```

<br>

El primero de ellos, es evidentemente obligatorio debido a que es el *lugar en el que se indica qué imagen se quiere introducir* en la web. El segundo, sin embargo, se utiliza debido a dos posibles motivos:

* En caso de que ocurra algún tipo de error al cargar la imagen, la web mostrará el texto definido en el atributo `alt`.
* En el caso de que el usuario utilice un lector de páginas web, debido a visión reducida o cualquier otro motivo, el lector leerá el contenido de dicho atributo.

<br>

Es por ello que **es importante definir bien el contenido de ambos**. Aquí se muestra cómo se vería la imagen si ocurriera alguno de los casos anteriores:

![1-alt](https://user-images.githubusercontent.com/110897750/197421627-e50b5a67-17f1-41a0-9108-f7feb8fcce6a.jpg)

<br>

<sub>[Volver al índice](#indice) | [Vídeos](#videos)</sub>


<br><hr>


<h3 id=formas>Formas de introducir una imagen</h3>

1. **Introducir imágenes locales escribiendo la dirección "completa"**

```HTML
<img src="C:\Users\larre\Documentslogo_NL.png" alt="Logo NL" style="width:300px; height:100%;"/>
```

<br>

Para demostrar que funciona:

![2-logo](https://user-images.githubusercontent.com/110897750/197421990-49013091-43d8-4983-afd0-317e576723a0.jpg)

<br>

2. **Introducir imágenes con una dirección relativa**

```HTML
<img src="img/skyrim.jpg" alt="foto de skyrim" style="width:300px; height:100%;">
```

<br>

Para demostrar que funciona:

![3-skyrim](https://user-images.githubusercontent.com/110897750/197421991-c7b6f25a-1d8a-45c4-bcd3-d88719d20fb5.jpg)

<br>

3. **Introducir imágenes de internet**

```HTML
<img src="https://github.githubassets.com/images/modules/site/social-cards/github-social.png" alt="imagen de GitHub" style="width:500px; height:100%;">
```

<br>

Para demostrar que funciona:

![4-github](https://user-images.githubusercontent.com/110897750/197421992-d1bb1bfd-64f3-4cf9-92e8-d51250f9642d.jpg)

<br>

<sub>[Volver al índice](#indice) | [Vídeos](#videos)</sub>


<br><hr>


<h3 id="size">Definir el tamaño de una imagen</h3>

Ya se ha hablado de los atributos obligarotios. Sin embargo, existen otros atributos que **no son obligatorios**, pero son muy utilizados para, por ejemplo, definir el tamaño de la imagen.

Existen dos formas de definir dicho tamaño desde HTML:

* **Atributo `style`**

Este atributo permite introducir estilos a la imagen. Sabiendo esto, se puede utilizar para definir una anchura (*width*) y altura (*height*):

```HTML
<img src="img/skyrim.jpg" alt="foto de skyrim" style="width:300px; height:100%;">
```

<br>

Este sería el resultado:

![3-skyrim](https://user-images.githubusercontent.com/110897750/197421991-c7b6f25a-1d8a-45c4-bcd3-d88719d20fb5.jpg)

<br>

* **Atributos `width` y `height`**

Se pueden utilizar estos dos atributos independientes sin la necesidad de usar estilos propios:

```HTML
<img src="img/skyrim.jpg" alt="foto de skyrim" width="300" height="100%">
```

<br>

![3-skyrim](https://user-images.githubusercontent.com/110897750/197421991-c7b6f25a-1d8a-45c4-bcd3-d88719d20fb5.jpg)

<br>

En ambos casos se ha obtenido el mismo resultado. Sin embargo, **¿cuál es la mejor de las dos opciones?** Personalmente, creo que es mejor la primera opción, porque permite realizar lo mismo que la segunda, asegurando que no se pueda modificar sin querer su tamaño desde CSS.

<sub>[Volver al índice](#indice) | [Vídeos](#videos)</sub>


<br><hr>


<h3 id="float">Float</h3>

Este no es un atributo como tal, sino que es una propiedad que se puede implementar **utilizando CSS**, y se caracteriza porque permite a una imagen *"flotar"* a la derecha o a la izquierda de un texto.

Para ello, como ya se ha visto anteriormente, se hará uso del atributo `style`.

```HTML
<img src="../img/people/chef.jpg" alt="foto de un chef" style="float:left;">
<p>Mucho texto<p>
<p>Mucho texto<p>
```

<br>

Este sería el resultado:

![5-float](https://user-images.githubusercontent.com/110897750/197422054-8bda77c0-6568-429c-8612-7f5209ffbbb4.jpg)

<br>

<sub>[Volver al índice](#indice) | [Vídeos](#videos)</sub>


<br><hr>
<hr><br>


<h2 id="videos">Vídeos</h2>

En las webs es común ver vídeos de vez en cuando. No son elementos tan típicos como una imagen, sin embargo, también conviene saber cómo poder añadirlos y configurarlos a nuestro gusto en nuestra web.

En primer lugar, para poder insertar una imagen en HTML, se necesita hacer uso de las etiquetas `<video>` y `</video>`. Dentro de ellas, se especificarán atributos tales como el ancho (*width*) y alto (*height*) del vídeo, y también se añadirán otros **atributos importantes**:

* `controls`: este atributo añade los controles básicos necesarios en cualquier vídeo. Permite pausar o poner en marcha el vídeo, verlo en pantalla completa, cambiar la velocidad o modificar el volumen.
* `autoplay`: es opcional, este atributo hace que el vídeo comience a reproducirse automáticamente tras ser cargado.
* `muted`: personalmente lo considero un atributo obligatorio, en especial si se ha introducido también el atributo `autoplay`.
* `loop`: este atributo opcional permite que el vídeo se vuelva a reproducir automáticamente tras finalizar.

<br>

Dentro de las etiquetas de vídeo mencionadas, se debe introducir la etiqueta de `<source>`, la cual no tiene una etiqueta de cierre, al igual que las etiquetas utilizadas para las imágenes. En éstas se debe especificar la dirección de referencia del vídeo a introducir, así como el tipo de formato que es.

No todos los navegadores soportan todos los formatos de vídeo, pero estos son los más utilizados y el atributo y valor necesarios para introducirlos:

* **MP4:** `type="video/mp4"`
* **WebM:** `type="video/webm"`
* **Ogg:** `type="video/ogg"`

<br>

He aquí un pequeño ejemplo con los atributos más básicos:

```HTML
<video width="600" height="auto" controls autoplay muted>
    <source src="img/Arde Bogotá - Big Bang.mp4" type="video/mp4">
</video>
```

<br>

Este sería el resultado de dicho código:

![2-video](https://user-images.githubusercontent.com/110897750/197422083-f8c6a635-bb51-4e28-ab79-2265456e2083.jpg)

<br>

<sub>[Volver al índice](#indice) | [Audios](#audios)</sub>


<br><hr>
<hr><br>


<h2 id="audios">Audios</h2>

Para poder añadir audios en una web se deben utilizar las etiquetas de `<audio>` de apertura y `</audio>` de cierre.

A pesar de estar divididas en dos puntos diferentes, éstas funcionan igual que las ya vistas en el apartado anterior, los *vídeos*. Para los audios no se deben definir ni la anchura (*width*) ni el alto (*height*), sin embargo, los atributos marcados como **importantes** en el apartado anterior, coinciden en este también:

* `controls`
* `autoplay`
* `muted`
* `loop`

<br>

De nuevo, dentro de esas etiquetas de audio, se deberá añadir la etiqueta `<source>`, donde especificar la dirección de referencia al audio, y el tipo, mediante el atributo **type** siendo los siguientes casos posibles:

* **MP3:** `type="audio/mp3"`
* **Ogg:** `type="audio/ogg"`
* **WAV:** `type="audio/wav"`

<br>

Aquí se muestra otro ejemplo básico:

```HTML
<audio controls>
    <source src="img/The Lord of the Rings - Soundtrack - Main theme.mp3" type="audio/mp3">
</audio>
```

<br>

Esto es lo que se podría ver en la página:

![3-audio](https://user-images.githubusercontent.com/110897750/197422085-b9287cce-7767-4f47-b5ed-3a680c8a5bc8.jpg)

<br>

<sub>[Volver al índice](#indice)</sub>


<br><hr>
<hr><br>


[<< TEMA 2](../02-Formularios_y_tablas/README.md#formularios-y-tablas) | [INICIO](../../README.md#temario-del-curso---teoria) | [TEMA 4 >>](../04-Hojas_de_estilo/README.md#introducción-a-css)
