# Etiquetas y atributos
En este apartado de teoría se tratarán los siguientes temas:

* [`DOCUMENTOS HTML`](#docs)
* [`ENCABEZADOS`](#hX)
* [`PÁRRAFOS`](#p)
* [`LINKS`](#links)
* [`LISTAS`](#lists)


<h2 id="docs">Documentos HTML</h2>
A la hora de crear un documento HTML deben tenerse en cuenta los siguientes puntos:

* Todos los documentos HTML deben comenzar con la declaración: `<!DOCTYPE html>`.
* El documento en sí comienza con una etiqueta de apertura `<html>` y finaliza con una de cierre `</html>`.
* La información del propio documento está definida entre la etiqueta de apertura `<head>` y la de cierre `</head>`.
* La parte visible de la página web, se verá reflejada dentro de las etiquetas `<body>` y `</body>`.


<h2 id="hX">Encabezados</h2>

Los encabezados están definidos por las etiquetas "hX", donde X es un índice del 1 al 6. Por ello, las etiquetas comienzan en `<h1>` y finalizan en `<h6>`. De esta manera, las etiquetas con un menor índice son las más importantes de todas, e irán perdiendo importancia a medida que su índice se vuelva mayor, he aquí un ejemplo:

```
<h1>Encabezado 1</h1>
<h2>Encabezado 2</h2>
<h3>Encabezado 3</h3>
<h4>Encabezado 4</h4>
<h5>Encabezado 5</h5>
<h6>Encabezado 6</h6>
```

La salida se ve así:

<img src="https://user-images.githubusercontent.com/110897750/195821658-5cfed9f8-01b5-445b-813e-3b933d99c754.jpg" alt="foto-encabezados">


<h2 id="p">Párrafos</h2>

Los párrafos en HTML están delimitados por las etiquetas `<p>` y `</p>`.

He aquí un ejemplo de la sintáxis:

```
<p>Esto es un párrafo</p>
<p>Esto es otro párrafo</p>
```


<h2 id="links">Links</h2>

Los links se crean con las etiquetas `<a>` y `</a>`. El texto o elemento contenido entre la etiqueta de apertura y de cierre, será aquello que el usuario deberá clicar para acceder al enlace definido.

Para añadir un link, se debe utilizar el atributo `href`, indicándole a qué enlace se quiere acceder tras clicar en él. Estas referencias pueden ser externas o internas, donde se puede acceder a elementos del propio documento haciendo referencia del id de un elemento, por ejemplo.

```
<a href="https://github.com/NLarrea">Esto es un link</a>
```

El link se vería de la siguiente manera:

<a href="https://github.com/NLarrea">Esto es un link</a>


<h2 id="lists">Listas</h2>

Existen dos tipos de listas:

* Listas no ordenadas (Unordered List): se definen entre las etiquetas de apertura `<ul>` y `</ul>`.
* Listas ordenadas (Ordered List): se definen entre las etiquetas de apertura `<ol>` y `</ol>`.

Las primeras crean listas con unos iconos delante, los cuales pueden ser modificados por el usuario aplicando estilos. Las segundas, sin embargo, se generan creando números o letras de tal forma que ordene los elementos de la lista.

Para crear dichos elementos (List Item), se utilizan las etiquetas `<li>` y `</li>`.

He aquí un ejemplo:

```
<ul>
	<li>Elemento 1</li>
	<li>Elemento 2</li>
	<li>Elemento 3</li>
</ul>
<ol>
	<li>Elemento 1</li>
	<li>Elemento 2</li>
	<li>Elemento 3</li>
</ol>
```

Este sería el resultado de dicho código:

![listas](https://user-images.githubusercontent.com/110897750/195825620-d0b8dd68-2f3c-4a30-a585-6a2655d4515e.jpg)


# Contacto
Si tienes alguna duda o sugerencia acerca del contenido de este documento o cualquier otro asunto, no dudes en contactar conmigo:

<div align="center">
&emsp;<a href="https://twitter.com/nloust_"><img width="16" alt="twitter_logo" src="https://user-images.githubusercontent.com/110897750/195668304-54d1fbb3-bea1-4f9d-9ee7-7e494bd79013.png"> @nloust_</a> <!-- twitter: -->
&emsp;<a href="https://www.instagram.com/n.loust/"><img width="16" alt="instagram_logo" src="https://seeklogo.com/images/I/instagram-new-2016-logo-4773FE3F99-seeklogo.com.png"> @n.loust</a> <!-- instagram: -->
&emsp;<a href="https://www.linkedin.com/in/naia-larrea/"><img width="16" alt="linkedin_logo" src="https://user-images.githubusercontent.com/110897750/195669519-30e44b5d-4bef-47d3-9e37-81cff0ee5e55.png"> Naia Larrea</a> <!-- linkedin: -->
</div>