# Selectores

Como ya se ha mencionado en el apartado anterior, en este archivo se hablará únicamente de los selectores. Los selectores son los encargados de seleccionar los elementos del documento HTML a los que se van a aplicar los estilos CSS.

<p id="indice">Esta va a ser la guía de este archivo:</p>

* [Selectores básicos](#selectores-básicos)
  * [Selector de tipo](#selector-de-tipo)
  * [Selector de clase](#selector-de-clase)
  * [Selector de ID](#selector-de-id)
  * [Selector de atributo](#selector-de-atributo)
  * [Selector universal](#selector-universal)
* [Combinadores](#combinadores)
  * [Combinador de hermanos adyacentes](#combinador-de-hermanos-adyacentes)
  * [Combinador de hermanos generales](#combinador-de-hermanos-generales)
  * [Combinador de descendencia](#combinador-de-descendencia)
  * [Combinador de hijo](#combinador-de-hijo)

<br>

[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos)


<br><hr><br>


## Selectores básicos

Los selectores básicos son los que se utilizan para seleccionar elementos HTML por su tipo, clase, ID o atributo. A continuación se explicarán cada uno de ellos.

El código HTML utilizado será el mostrado a continuación:

```html
<h1>Esto es un encabezado</h1><br>
<p>Esto es un párrafo</p><br>
<p class="parrafo">Esto es un párrafo con clase</p><br>
<p id="parrafo">Esto es un párrafo con id</p><br>
<a href="https://github.com/nlarrea">
    <i class="bi bi-github"></i>
    nlarrea
</a><br>
<a href="https://twitter.com/nloust_">
    <i class="bi bi-twitter"></i>
    @nloust_
</a><br>
<a href="https://www.instagram.com/n.loust/">
    <i class="bi bi-instagram"></i>
    @n.loust
</a>
```

<br>

Como se puede observar, en el código HTML se han utilizado tres tipos de selectores: el selector de tipo, el selector de clase y el selector de ID. A continuación se explicarán cada uno de ellos.


<br><hr>


### Selector de tipo

El selector de tipo es el más sencillo de todos los selectores. Se utiliza para seleccionar elementos HTML por su tipo.

En el ejemplo a continuación, se ha utilizado el selector de tipo para seleccionar los elementos `<h1>`, `<p>` y `<a>`:

```css
h1 {
    color: red;
}

p {
    color: blue;
}

a {
    color: green;
}
```

<br>

Como se puede observar, el selector de tipo se utiliza de la siguiente manera:

```css
selector {
    propiedad: valor;
}
```

<br>

Como ya se ha mencionado, el selector de tipo se utiliza para seleccionar todos los elementos HTML que tengan el mismo tipo que el selector. En el ejemplo anterior, cuando el selector de tipo es `p`, se seleccionan todos los elementos `<p>` del documento HTML. Por ello se verán afectados todos los elementos `<p>` del documento HTML, independientemente de si tienen o no una clase o ID.

Este sería el resultado del código CSS anterior:

![1-selector-de-tipo](https://user-images.githubusercontent.com/110897750/203103615-f252a86c-8dd6-4871-9f62-34debc58b70a.jpg)

<br>

El selector de tipo es el más sencillo de todos los selectores, pero también es el menos eficiente. Por ello, se recomienda utilizar los selectores de clase y de ID en lugar del selector de tipo.

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>


<br><hr>


### Selector de clase

El selector de clase es el selector más utilizado de todos los selectores. Se utiliza para seleccionar elementos HTML por su clase.

En el ejemplo anterior, se ha utilizado el selector de clase para seleccionar los elementos la clase `parrafo`:

```css
.parrafo {
    color: darkgoldenrod;
}
```

<br>

Como se puede observar, el selector de clase se utiliza de la siguiente manera:

```css
.selector {
    propiedad: valor;
}
```

<br>

Como ya se ha mencionado, el selector de clase se utiliza para seleccionar todos los elementos HTML que tengan la misma clase que el selector. En el ejemplo anterior, cuando el selector de clase es `.parrafo`, se seleccionan todos los elementos HTML que tengan la clase `parrafo`.

Este sería el resultado del código CSS anterior:

![2-selector-de-clase](https://user-images.githubusercontent.com/110897750/203103619-1b5493a9-680f-4b03-a7e9-b46efd8a9483.jpg)

<br>

El selector de clase es el selector más utilizado de todos los selectores. Permite especificar a qué elemento se desea aplicar el formato indicado, por ello, se recomienda utilizar el selector de clase en lugar del selector de tipo.

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>


<br><hr>


### Selector de ID

El selector de ID es el selector menos utilizado de todos los selectores. Se utiliza para seleccionar elementos HTML por su ID. Se usa para seleccionar un elemento HTML en específico.

En el ejemplo anterior, se ha utilizado el selector de ID para seleccionar el elemento con ID `parrafo`:

```css
#parrafo {
    color: darkred;
}
```

<br>

Como se puede observar, el selector de ID se utiliza de la siguiente manera:

```css
#selector {
    propiedad: valor;
}
```

<br>

Como ya se ha mencionado, el selector de ID se utiliza para seleccionar el elemento HTML que tenga el mismo ID que el selector. En el ejemplo anterior, cuando el selector de ID es `#parrafo`, se selecciona el elemento HTML que tenga el ID `parrafo`.

Este sería el resultado del código CSS anterior:

![3-selector-de-id](https://user-images.githubusercontent.com/110897750/203103621-539f36d5-e3cb-4e3c-afa0-cae2e6f1805e.jpg)

<br>

El selector de ID es el selector menos utilizado de todos los selectores. Se utiliza el selector de clase en las ocasiones donde se quiera aplicar un estilo a elementos concretos. El selector de ID se utiliza para seleccionar un elemento HTML en específico ya que no se puede utilizar el mismo ID para dos elementos HTML diferentes.

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>


<br><hr>


### Selector de atributo

El selector de atributo es un selector que se utiliza para seleccionar elementos HTML por su atributo, es decir, para seleccionar elementos HTML que tengan un atributo concreto.

En el ejemplo a continuación, se ha utilizado el selector de atributo para seleccionar los elementos HTML que tengan *"loust"* en algún lugar del atributo href:

```css
a[href*="loust"] {
    color: darkorange;
}
```

<br>

Como se puede observar, el selector de atributo se utiliza de la siguiente manera:

```css
selector[atributo] {
    propiedad: valor;
}
```

<br>

Como ya se ha mencionado, el selector de atributo se utiliza para seleccionar todos los elementos HTML que tengan el mismo atributo que el selector. En el ejemplo anterior, cuando el selector de atributo es `a[href*="loust"]`, se seleccionan todos los elementos HTML que tengan escrito *"loust"* en parte del atributo `href`.

Este sería el resultado del código CSS anterior:

![4-selector-de-atributo](https://user-images.githubusercontent.com/110897750/203103625-c09c821a-4598-4273-9442-a1c298cc89cf.jpg)

<br>

Existen varias opciones para los selectores de atributo. A continuación, se muestran las más utilizadas:

* `selector[atributo]` - Selecciona todos los elementos HTML que **tengan el atributo** indicado.
* `selector[atributo="valor"]` - Selecciona todos los elementos HTML en los que el valor de dicho atributo **sea** el valor indicado.
* `selector[atributo~="valor"]` - Selecciona todos los elementos HTML en los que el valor de dicho atributo **sea o contenga** el valor indicado.
* `selector[atributo|="valor"]` - Selecciona todos los elementos HTML en los que el valor de dicho atributo **sea o empiece por** el valor indicado.
* `selector[atributo^="valor"]` - Selecciona todos los elementos HTML en los que el valor de dicho atributo **empiece por** el valor indicado.
* `selector[atributo$="valor"]` - Selecciona todos los elementos HTML en los que el valor de dicho atributo **termine por** el valor indicado.
* `selector[atributo*="valor"]` - Selecciona todos los elementos HTML en los que el valor de dicho atributo **contenga** el valor indicado.

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>


<br><hr>


### Selector universal

El selector universal es un selector que se utiliza para seleccionar todos los elementos HTML de la página. Se utiliza para aplicar un estilo común a todos los elementos HTML.

En el ejemplo a continuación, se ha utilizado el selector universal para seleccionar todos los elementos HTML y modificar el `margin`, `padding` y `box-sizing`:

```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
```

<br>

Como se puede observar, el selector universal se utiliza de la siguiente manera:

```css
* {
    propiedad: valor;
}
```

<br>

Este sería el resultado del código CSS anterior:

![5-selector-universal](https://user-images.githubusercontent.com/110897750/203103626-114b5a5e-a526-43bb-95b3-dd1db0591d5c.jpg)

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>


<br><hr>
<hr><br>


## Combinadores

Los combinadores son selectores que se utilizan para seleccionar elementos HTML que cumplan una serie de condiciones. Los combinadores se utilizan para seleccionar elementos HTML que no se pueden seleccionar con un solo selector.

El código HTML que se utilizará en este apartado es el siguiente:

```html
<div class="some-text">
    <h1>Esto es un encabezado</h1>
    <p>Esto es un párrafo después de un h1</p>
    <span>Esto es un span en medio de los p</span>
    <p>Esto es un párrafo hermano de h1 y otros p</p>
</div>
<p>Esto es un párrafo suelto</p>
<a href="https://github.com/nlarrea">
    <span>
        <i class="bi bi-github"></i>
        nlarrea
    </span>
</a>
<a href="https://twitter.com/nloust_">
    <span>
        <i class="bi bi-twitter"></i>
        @nloust_
    </span>
</a>
<a href="https://www.instagram.com/n.loust/">
    <span>
        <i class="bi bi-instagram"></i>
        @n.loust
    </span>
</a>
```


<br><hr>


### Combinador de hermanos adyacentes

El combinador de hermanos adyacentes es un combinador que se utiliza para seleccionar elementos HTML que sean hermanos adyacentes. Un elemento HTML es hermano adyacente de otro si se encuentran uno al lado del otro y tienen el mismo padre.

En el ejemplo a continuación, se ha utilizado el combinador de hermanos adyacentes para seleccionar todos los `<p>` que van después de un `<h1>`:

```css
h1 + p {
    color: red;
}
```

<br>

Como se puede observar, el combinador de hermanos adyacentes se utiliza de la siguiente manera:

```css
selector1 + selector2 {
    propiedad: valor;
}
```

<br>

El elemento que se ve afectado por el código CSS es el selector2, que es el elemento que va después del selector1. En el ejemplo anterior, el selector1 es el `<h1>` y el selector2 es el `<p>`.

Este sería el resultado del código CSS anterior:

![7-combinador-de-hermanos-adyacentes](https://user-images.githubusercontent.com/110897750/203103628-07ea30fb-07ca-4dc2-8c91-379d066716de.jpg)

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>


<br><hr>


### Combinador de hermanos generales

El combinador de hermanos generales es un combinador que se utiliza para seleccionar elementos HTML que sean hermanos generales. Un elemento HTML es hermano general de otro si uno sigue al otro (no necesariamente de forma inmediata) y tienen el mismo padre.

En el ejemplo a continuación, se ha utilizado el combinador de hermanos generales para seleccionar todos los `<p>` que van después de un `<span>`:

```css
span ~ p {
    color: blue;
}
```

<br>

Como se puede observar, el combinador de hermanos generales se utiliza de la siguiente manera:

```css
selector1 ~ selector2 {
    propiedad: valor;
}
```

<br>

El elemento que se ve afectado por el código CSS es el selector2, que es el elemento que va después del selector1. En el ejemplo anterior, el selector1 es el `<span>` y el selector2 es el `<p>`. Por lo que, en este caso, se verá modificado el color del segundo **párrafo**.

Este sería el resultado del código CSS anterior:

![8-combinador-de-hermanos-generales](https://user-images.githubusercontent.com/110897750/203103631-d9a670ae-4f58-4995-ade9-98b23cc94c66.jpg)

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>


<br><hr>


### Combinador de descendencia

El combinador de descendencia es un combinador que se utiliza para seleccionar elementos HTML que sean descendientes. Un elemento HTML es descendiente de otro si se encuentra dentro de él.

En el ejemplo a continuación, se ha utilizado el combinador de descendencia para seleccionar todos los `<i>` que están dentro de un `<a>`, no necesariamente de forma inmediata:

```css
a i {
    color: orange;
}
```

<br>

Como se puede observar, el combinador de descendencia se utiliza de la siguiente manera:

```css
selector1 selector2 {
    propiedad: valor;
}
```

<br>

El elemento que se ve afectado por el código CSS es el selector2, que es el elemento que está dentro del selector1. En el ejemplo anterior, el selector1 es el `<a>` y el selector2 es el `<i>`. Por lo que, en este caso, se verá modificado el color de los textos dentro de los links.

Este sería el resultado del código CSS anterior:

![9-combinador-de-descendencia](https://user-images.githubusercontent.com/110897750/203103637-2776128e-3462-42ba-9a03-0c1d2d7ee800.jpg)

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>


<br><hr>


### Combinador de hijo

El combinador de hijo, o de *descendencia directa*, es un combinador que se utiliza para seleccionar elementos HTML que sean hijos. Un elemento HTML es hijo de otro si se encuentra dentro de él y es el primer elemento.

En el ejemplo a continuación, se ha utilizado el combinador de hijo para seleccionar todos los `<span>` que están dentro de un `<a>`:

```css
a > span {
    color: lightseagreen;
}
```

<br>

Como se puede observar, el combinador de hijo se utiliza de la siguiente manera:

```css
selector1 > selector2 {
    propiedad: valor;
}
```

<br>

El elemento que se ve afectado por el código CSS es el selector2, que es el elemento que está dentro del selector1. En el ejemplo anterior, el selector1 es el `<a>` y el selector2 es el `<span>`. Por lo que, en este caso, se verá modificado el color de los span dentro de los links.

A los iconos también se les aplica este color, aunque como los iconos tenían ya un color asignado, en la imagen a continuación no se reflejará.

Este sería el resultado del código CSS anterior:

![10-combinador-de-hijo](https://user-images.githubusercontent.com/110897750/203103640-f0a8226e-74af-4a4b-b3c7-81ab3e7d568a.jpg)

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>