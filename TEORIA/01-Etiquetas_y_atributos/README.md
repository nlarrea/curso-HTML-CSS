# Etiquetas y atributos

En este apartado de teoría se tratarán los siguientes temas:

* [DOCUMENTOS HTML](#documentos-html)
* [ENCABEZADOS](#encabezados)
* [PÁRRAFOS](#párrafos)
* [LINKS](#links)
* [LISTAS](#listas)

<br>

<sub>* [Ver código](mi-primera-pagina-web.html)</sub>

[EJERCICIOS](../../EJERCICIOS/) | [INICIO](../../README.md#temario-del-curso---teoria) | [TEMA 2 >>](../02-Formularios_y_tablas/README.md#formularios-y-tablas)


<br><hr>
<hr><br>


## Documentos HTML

A la hora de crear un documento HTML deben tenerse en cuenta los siguientes puntos:

* Todos los documentos HTML deben comenzar con la declaración: `<!DOCTYPE html>`.
* El documento en sí comienza con una etiqueta de apertura `<html>` y finaliza con una de cierre `</html>`.
* La información del propio documento está definida entre la etiqueta de apertura `<head>` y la de cierre `</head>`.
* La parte visible de la página web, se verá reflejada dentro de las etiquetas `<body>` y `</body>`.


<br><hr>
<hr><br>


## Encabezados

Los encabezados están definidos por las etiquetas "hX", donde X es un índice del 1 al 6. Por ello, las etiquetas comienzan en `<h1>` y finalizan en `<h6>`. De esta manera, las etiquetas con un menor índice son las más importantes de todas, e irán perdiendo importancia a medida que su índice se vuelva mayor, he aquí un ejemplo:

```HTML
<h1>Encabezado 1</h1>
<h2>Encabezado 2</h2>
<h3>Encabezado 3</h3>
<h4>Encabezado 4</h4>
<h5>Encabezado 5</h5>
<h6>Encabezado 6</h6>
```

<br>

La salida se ve así:

<img src="https://user-images.githubusercontent.com/110897750/195821658-5cfed9f8-01b5-445b-813e-3b933d99c754.jpg" alt="foto-encabezados">


<br><hr>
<hr><br>


## Párrafos

Los párrafos en HTML están delimitados por las etiquetas `<p>` y `</p>`.

He aquí un ejemplo de la sintáxis:

```HTML
<p>Esto es un párrafo</p>
<p>Esto es otro párrafo</p>
```


<br><hr>
<hr><br>


## Links

Los links se crean con las etiquetas `<a>` y `</a>`. El texto o elemento contenido entre la etiqueta de apertura y de cierre, será aquello que el usuario deberá clicar para acceder al enlace definido.

Para añadir un link, se debe utilizar el atributo `href`, indicándole a qué enlace se quiere acceder tras clicar en él. Estas referencias pueden ser externas o internas, donde se puede acceder a elementos del propio documento haciendo referencia del id de un elemento, por ejemplo.

```HTML
<a href="https://nlarrea-links.vercel.app/">Esto es un link</a>
```

<br>

El link se vería de la siguiente manera:

<a href="https://nlarrea-links.vercel.app/">Esto es un link</a>


<br><hr>
<hr><br>


## Listas

Existen dos tipos de listas:

* Listas no ordenadas (Unordered List): se definen entre las etiquetas de apertura `<ul>` y `</ul>`.
* Listas ordenadas (Ordered List): se definen entre las etiquetas de apertura `<ol>` y `</ol>`.

Las primeras crean listas con unos iconos delante, los cuales pueden ser modificados por el usuario aplicando estilos. Las segundas, sin embargo, se generan creando números o letras de tal forma que ordene los elementos de la lista.

Para crear dichos elementos (List Item), se utilizan las etiquetas `<li>` y `</li>`.

He aquí un ejemplo:

```HTML
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

<br>

Este sería el resultado de dicho código:

![listas](https://user-images.githubusercontent.com/110897750/195825620-d0b8dd68-2f3c-4a30-a585-6a2655d4515e.jpg)

<br><hr>
<hr><br>

[EJERCICIOS](../../EJERCICIOS/) | [INICIO](../../README.md#temario-del-curso---teoria) | [TEMA 2 >>](../02-Formularios_y_tablas/README.md#formularios-y-tablas)
