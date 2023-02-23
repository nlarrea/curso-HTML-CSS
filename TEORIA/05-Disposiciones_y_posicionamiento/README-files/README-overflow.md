# OVERFLOW

En esta parte de la guía se va a hablar de cómo permitir o no que los elementos en nuestra página web se vean si éstos ocupan más que el contenedor en el que se encuentran, por ejemplo.

<p id="indice">He aquí un pequeño índice donde se muestra el temario a tratar:</p>

* [Valores para overflow](#valores-para-overflow)
  * [visible](#visible)
  * [hidden](#hidden)
  * [scroll](#scroll)
  * [auto](#auto)
* [overflow en un eje](#overflow-en-un-eje)
* [overflow-wrap](#overflow-wrap)
* [text-overflow](#text-overflow)

<br>

[Disposición, Posicionamiento y Overflow](../README.md#disposición-posicionamiento-y-overflow)


<br><hr><br>


## Valores para overflow

Los valores permitidos en esta propiedad son los mostrados en el [indice](#indice).

El código HTML utilizado en este apartado será el siguiente:

```html
<div class="container">
    <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Vel velit, esse molestiae suscipit at dolorum asperiores 
        expedita, neque porro placeat ipsum unde sed veritatis nisi? Delectus accusamus consequuntur iure a sed eum ex tenetur 
        magnam velit unde voluptatem aliquid minus et debitis officiis, nesciunt in eligendi voluptatum nisi nam? Expedita 
        itaque ab deserunt ad blanditiis nemo molestias soluta id, non amet fugit similique nostrum nulla ipsum ipsam eaque. 
        Ducimus unde labore magnam ipsam veritatis amet, corrupti officia libero enim quaerat officiis, accusantium hic rerum 
        animi. Nam qui possimus nisi suscipit quas neque maxime ab error. Officiis debitis placeat ad repellat!
    </p>
</div>
```

<br>

Acompañado de los siguientes estilos base de CSS:

```css
.container {
    width: 300px;
    height: 200px;
    margin: 20px;
    padding: 10px;
    border: 1px solid black;
    background-color: rgba(111, 212, 212, 0.466);
}
```


<br><hr>


### visible

Este es el valor *por efecto* para la propiedad `overflow`. Lo que se consigue con ello es **permitir ver el contenido a pesar de que sobrepase los límites del contenedor**.

He aquí un ejemplo:

```css
.container {
    overflow: visible; /* no necesario */
}
```

<br>

Este es el resultado:

![1-overflow_visible](https://user-images.githubusercontent.com/110897750/202437173-ac36bced-360f-4eb1-9a24-2c7d50a00ddc.jpg)

<sub>[Disposición, Posicionamiento y Overflow](../README.md#disposición-posicionamiento-y-overflow) | [Volver al índice](#indice)</sub>


<br><hr>


### hidden

Como su propio nombre indica, si se utiliza este valor, aquel contenido que *"sobre"* no será visible.

Continuando con el ejemplo anterior:

```css
.container {
    overflow: hidden;
}
```

<br>

Este es el resultado:

![2-overflow_hidden](https://user-images.githubusercontent.com/110897750/202437176-0d1fcd06-6886-4e66-a6c3-543429629c68.jpg)

<sub>[Disposición, Posicionamiento y Overflow](../README.md#disposición-posicionamiento-y-overflow) | [Volver al índice](#indice)</sub>


<br><hr>


### scroll

Este valor añade barras de scroll tanto verticales como horizontales. Si una de las dos barras no es necesaria, también será añadida, repito: **¡se añaden las dos!**

Continuando con el ejempli anterior:

```css
.container {
    overflow: scroll;
}
```

<br>

Este es el resultado:

![3-overflow_scroll](https://user-images.githubusercontent.com/110897750/202437178-835d0e9a-f2fd-4957-8dea-0b582b5a8cd2.jpg)

<sub>[Disposición, Posicionamiento y Overflow](../README.md#disposición-posicionamiento-y-overflow) | [Volver al índice](#indice)</sub>


<br><hr>


### auto

Este valor funciona igual que el `scroll`, sin embargo, **añade únicamente aquella barra de scroll que sí sea necsaria**, lo cual estéticamente hablando, queda mucho mejor.

Siguendo el mismo ejemplo que antes:

```css
.container {
    overflow: auto;
}
```

<br>

Este es el resultado:

![4-overflow_auto](https://user-images.githubusercontent.com/110897750/202437180-100203b8-3042-4702-90da-1e5db2c791c9.jpg)

<sub>[Disposición, Posicionamiento y Overflow](../README.md#disposición-posicionamiento-y-overflow) | [Volver al índice](#indice)</sub>


<br><hr>


## overflow en un eje

Se puede definir el valor de la propiedad `overflow` en una sola dirección utilizando las siguientes propiedades:

* overflow-x
* overflow-y

<br>

Esto permite definir diferentes valores de overflow para cada uno de los ejes, siendo estas opciones las mismas que las vistas en el [apartado anterior](#valores-para-overflow):

* visible
* hidden
* scroll
* auto

<br>

En este caso, la **diferencia entre *scroll* y *auto*** consiste en que `scroll` siempre mostrará la barra (horizontal o vertical) y auto la mostrará solo cuando sea necesaria.

<sub>[Disposición, Posicionamiento y Overflow](../README.md#disposición-posicionamiento-y-overflow) | [Volver al índice](#indice)</sub>


<br><hr>


## overflow-wrap

Esta propiedad permite especificar si un texto *largo* debe *"partirse"* y saltar a la siguiente línea, o debe mantenerse y permitir que sobresalga del bloque al que pertenece.

Su valor *por defecto* es `normal`.

He aquí un ejemplo modificando el código HTML y CSS:

```html
<div class="container">
    <p>
        Loremipsumdolorsitametconsecteturadipisicingelit.
    </p>
</div>
```

<br>

Con el valor por defecto:

```css
.container {
    /* no sería necesario añadirlo */
    overflow-wrap: normal;
}
```

<br>

Este sería el resultado:

![5-overflow-wrap_normal](https://user-images.githubusercontent.com/110897750/202437181-07aef347-b361-4637-b5d4-1c420f052d00.jpg)

<br>

Sin embargo, al modificar el valor de esta propiedad al siguiente:

```css
.container {
    overflow-wrap: break-word;
}
```

<br>

Se consigue que la palabra se *"rompa"* y salte a la siguiente línea:

![6-overflow-wrap_break-word](https://user-images.githubusercontent.com/110897750/202437184-ee93e6ff-3fc4-4357-b57a-3c54d09b89ca.jpg)

<sub>[Disposición, Posicionamiento y Overflow](../README.md#disposición-posicionamiento-y-overflow) | [Volver al índice](#indice)</sub>


<br><hr>


## text-overflow

Siguiendo más o menos el ejemplo anterior, cuando se encierra un texto dentro de un contenedor y éste es más pequeño de lo que ocupa el texto, cuando no se desea mostrar dicho texto sobrante, se puede utilizar `hidden`.

Sin embargo, en osaciones se deseará dar formato a dicho texto, como indicar que hay más texto haciendo uso de "...".

Para que esto sea posible, el elemento que contenga el texto **debe** tener los siguientes valores para estas propiedades:

* `overflow: hidden;`
* `white-space: nowrap;`

<br>

El valor por defecto de esta propiedad es `clip`.

He aquí un ejemplo con el siguiente código HTML:

```html
<div class="container">
    <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Eaque, rem?</p>
</div>
```

<br>

Y el siguiente estilo:

```css
p {
    overflow: hidden;
    white-space: nowrap;
    text-overflow: ellipsis;
}
```

<br>

Esto es lo que se consigue:

![7-text-overflow](https://user-images.githubusercontent.com/110897750/202437185-dd2ebfde-cb1d-48d6-baed-3de414619224.jpg)

<sub>[Disposición, Posicionamiento y Overflow](../README.md#disposición-posicionamiento-y-overflow) | [Volver al índice](#indice)</sub>