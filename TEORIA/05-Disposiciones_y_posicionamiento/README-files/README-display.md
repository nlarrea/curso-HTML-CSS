# DISPOSICIONES

En este apartado se hablará de la propiedad `display` de CSS.

<p id="indice">He aquí un pequeño índice indicando los temas a tratar:</p>

* [none](#none)
* [inline](#inline)
* [block](#block)
* [inline-block](#inline-block)
* [table](#table)
* [table-cell](#table-cell)
* [table-row](#table-row)
* [flex](#flex)
* [inline-flex](#inline-flex)
* [grid](#grid)
* [inline-grid](#inline-grid)

<br>

[<< Disposición, Posicionamiento y Overflow](../README.md#disposición-posicionamiento-y-overflow)


<br><hr>


## none

Haciendo uso de este valor, el elemento será *"borrado"* totalmente de la página, se actuará como si éste no existiera (a pesar de estar completamente definido en el archivo HTML).

He aquí un pequeño ejemplo:

Este es el código HTML creado, donde hay un párrafo que contiene un `<span>` con un mensaje *"Hello World!"*. Todo ello está dentro de un `<div>`, para mostrar mejor el contenido.

```html
<div class="container">
    <p>
        Lorem ipsum dolor sit amet
        <span class="displayMe">Hello World!</span>
        consectetur adipisicing elit. Tempora 
        suscipit quaerat adipisci provident, sit 
        error libero hic temporibus sed molestiae.
    </p>
</div>
```

<br>

El mensaje *"Hello World!"* no será visto, como si no existiera, debido a que tiene un `display: none;`, tal y como se puede ver en el código de CSS mostrado:

```css
.displayMe {
    display: none;
}
```

<br>

He aquí el resultado de dicho código:

![1-none](https://user-images.githubusercontent.com/110897750/202165823-927079f9-11e1-4a39-993f-465daf73e3d4.jpg)

<sub>[Disposición, Posicionamiento y Overflow](../README.md#disposición-posicionamiento-y-overflow) | [Volver al índice](#indice)</sub>


<br><hr>


## inline

Utilizando `inline`, el elemento se comporta como si fuera parte de un texto, como si formara parte de él.

A continuación, se mostrará un ejemplo para entender mejor este valor de la propiedad. Se sigue manteniendo el mismo concepto con el código HTML:

```html
<div class="container">
    <p>
        Lorem ipsum dolor sit amet
        <strong class="displayMe">Hello World!</strong>
        consectetur adipisicing elit. Tempora 
        suscipit quaerat adipisci provident, sit 
        error libero hic temporibus sed molestiae.
    </p>
</div>
```

<br>

Sin embargo, este es el código CSS:

```css
.displayMe {
    display: inline;
    background-color: aquamarine; /* para que se vea mejor */
}
```

<br>

En esta ocasión sí se puede ver el contenido del `<span>`:

![2-inline](https://user-images.githubusercontent.com/110897750/202165826-70c7b4a6-6c1f-41b7-82c7-c963a78199ed.jpg)

<sub>[Disposición, Posicionamiento y Overflow](../README.md#disposición-posicionamiento-y-overflow) | [Volver al índice](#indice)</sub>


<br><hr>


## block

Con este tipo de disposición, se debe imaginar un bloque que ocupa todo el ancho posible. Así, es más sencillo entender que lo que permite `display: block;` es hacer que el elemento se traslade a **una nueva línea**, y ocupe todo el ancho posible de la misma.

Ahora se mostrará el mismo ejemplo:

```html
<div class="container">
    <p>
        Lorem ipsum dolor sit amet
        <span class="displayMe">Hello World!</span>
        consectetur adipisicing elit. Tempora 
        suscipit quaerat adipisci provident, sit 
        error libero hic temporibus sed molestiae.
    </p>
</div>
```

<br>

Se modifica el display en el código CSS:

```css
.displayMe {
    display: block;
}
```

<br>

Sin haber modificado el código del archivo HTML, pero cambiando la disposición en el CSS, se obtiene lo siguiente:

![3-block](https://user-images.githubusercontent.com/110897750/202165829-b98134f3-9cd5-4197-b853-46f660033805.jpg)

<sub>[Disposición, Posicionamiento y Overflow](../README.md#disposición-posicionamiento-y-overflow) | [Volver al índice](#indice)</sub>


<br><hr>


## inline-block

En ocasiones, se deseará utilizar los dos últimos valores vistos anteriormente. Para ello existe esta opción llamada `inline-block`:

* **inline:** debido a que se ajusta a los elementos igual que los elementos `inline`, como si se tratara de una parte más del texto.
* **block:** porque como a cualquier elemento de tipo bloque, a este también se le pueden aplicar estilos de `height` y `width`.

He aquí un ejemplo:

Se mantiene el código HTML (adjunto para que se pueda leer mejor el código al completo):

```html
<div class="container">
    <p>
        Lorem ipsum dolor sit amet
        <span class="displayMe">Hello World!</span>
        consectetur adipisicing elit. Tempora 
        suscipit quaerat adipisci provident, sit 
        error libero hic temporibus sed molestiae.
    </p>
</div>
```

<br>

Y este sería el nuevo código CSS:

```css
.displayMe {
    display: inline-block;
    height: 50px;
    width: 60px;
}
```

<br>

Este es el resultado:

![4-inline-block](https://user-images.githubusercontent.com/110897750/202165833-01962d0e-2ae4-45e6-aff3-0af8883fa35b.jpg)

Como se puede observar, el texto resaltado tiene una altura mayor a la que ocupa una línea, por lo que la primera línea del párrafo, a la que pertenece dicho *"Hello World"*, tiene una nueva altura y empuja a las demás hacia abajo.

<sub>[Disposición, Posicionamiento y Overflow](../README.md#disposición-posicionamiento-y-overflow) | [Volver al índice](#indice)</sub>


<br><hr>


## table

Con este valor de la propiedad, se consigue que el elemento al que se hace referencia y todos sus *"hijos"* actúen como si fueran elementos de una tabla, igual que si se usara la etiqueta `<table>` vista en el [segundo tema](../../02-Formularios_y_tablas/README.md) de este repositorio.

He aquí un ejemplo:

Se mpdifica ligeramente el contenido del archivo HTML:

```html
<div class="container">
    <p>
        Lorem ipsum dolor sit amet
        <div class="displayMe">
            Hello World!
            <span>Elemento 1</span>
            <span>Elemento 2</span>
        </div>
        consectetur adipisicing elit. Tempora suscipit 
        quaerat adipisci provident, sit error libero hic 
        temporibus sed molestiae.
    </p>
</div>
```

<br>

Se han sustituido las etiquetas `<strong>` del texto *"Hello World!"* por `<div>`, y se han añadido dos `<span>` dentro del mismo.

En el código CSS se ha escrito lo siguiente:

```css
.displayMe {
    display: table;
    height: 40px;
    background-color: aquamarine;
}

.displayMe > span:nth-child(1) {
    background-color: lightcoral;
}

.displayMe > span:nth-child(2) {
    background-color: lightgreen;
}
```

<br>

Se les ha puesto color de fondo a ambos `<span>` para poder diferenciarlos mejor.

Este es el resultado de dicho código:

![5-table](https://user-images.githubusercontent.com/110897750/202165834-54944b8e-dedf-4770-a516-d146696dcbde.jpg)

<sub>[Disposición, Posicionamiento y Overflow](../README.md#disposición-posicionamiento-y-overflow) | [Volver al índice](#indice)</sub>


<br><hr>


## table-cell

Ya se ha visto el valor `table`, sin embargo, también se puede especificar que se desea que dicho contenido actúe como celdas de una tabla.

Con este valor se consigue que los elementos actúen igual que si se utilizaran etiquetas `<td>` o `<th>`.

He aquí un ejemplo:

Se mantiene el código HTML visto en el [apartado anterior](#table):

```html
<div class="container">
    <p>
        Lorem ipsum dolor sit amet
        <div class="displayMe">
            Hello World!
            <span>Elemento 1</span>
            <span>Elemento 2</span>
        </div>
        consectetur adipisicing elit. Tempora suscipit 
        quaerat adipisci provident, sit error libero hic 
        temporibus sed molestiae.
    </p>
</div>
```

<br>

El contenido del archivo CSS apenas ha sido modificado:

```css
.displayMe {
    display: table-cell;
    height: 40px;
    background-color: aquamarine;
}

.displayMe > span:nth-child(1) {
    background-color: lightcoral;
}

.displayMe > span:nth-child(2) {
    background-color: lightgreen;
}
```

<br>

A pesar del pequeño cambio, se puede apreciar cómo los dos `span` se han desplazado ligeramente hacia la derecha, dejando una especie de pequeño *gap* entre los elementos:

![6-table-cell](https://user-images.githubusercontent.com/110897750/202165836-b29d55a5-a852-4acf-9211-093d226ec4ae.jpg)

<sub>[Disposición, Posicionamiento y Overflow](../README.md#disposición-posicionamiento-y-overflow) | [Volver al índice](#indice)</sub>


<br><hr>


## table-row

Este valor permite a los elementos comportarse de la misma manera que si se utilizaran las etiquetas `<tr>`.

A continuación, se muestra un breve ejemplo:

Se vuelve a utilizar el mismo código que el visto anteriormente:

```html
<div class="container">
    <p>
        Lorem ipsum dolor sit amet
        <div class="displayMe">
            Hello World!
            <span>Elemento 1</span>
            <span>Elemento 2</span>
        </div>
        consectetur adipisicing elit. Tempora suscipit 
        quaerat adipisci provident, sit error libero hic 
        temporibus sed molestiae.
    </p>
</div>
```

<br>

Y de nuevo, se hace un pequeño cambio en el archivo CSS:

```css
.displayMe {
    display: table-row;
    height: 40px;
    background-color: aquamarine;
}

.displayMe > span:nth-child(1) {
    background-color: lightcoral;
}

.displayMe > span:nth-child(2) {
    background-color: lightgreen;
}
```

<br>

En esta ocasión, el contenido vuelve a juntarse. Esto se debe a que se concentra todo en una misma línea, ya que se le ha indicado que actúe como la línea de una tabla:

![7-table-row](https://user-images.githubusercontent.com/110897750/202165839-93af48be-9b46-4ada-9fbc-f67a30244558.jpg)

<sub>[Disposición, Posicionamiento y Overflow](../README.md#disposición-posicionamiento-y-overflow) | [Volver al índice](#indice)</sub>


<br><hr>


## flex

* **Cada una de las PROPIEDADES DEL FLEXBOX se explican [AQUÍ](flexbox.md#flexbox) en un archivo a parte, para no hacer este apartado más extenso.**

Si se utiliza este valor para un único elemento, parece que tiene las mismas propiedades que un elemento con `display: block;`. Sin embargo, cuando se utiliza `display: flex;` en un elemento *"padre"*, dicho elemento se convierte en un **contenedor Flexbox**, y los *"hijos"* se convierten en **elementos Flexbox**.

En esta ocasión, se modifica el ejemplo de la siguiente manera:

En el código HTML se añade un nuevo elemento y se elimina el texto *"Hello World!"*:

```html
<div class="container">
    <p>
        Lorem ipsum dolor sit amet
        <div class="displayMe">
            <span>Elemento 1</span>
            <span>Elemento 2</span>
            <span>Elemento 3</span>
        </div>
        consectetur adipisicing elit. Tempora suscipit 
        quaerat adipisci provident, sit error libero 
        hic temporibus sed molestiae.
    </p>
</div>
```

<br>

Este es el código CSS:

```css
.displayMe {
    display: flex;
    justify-content: space-evenly;
    background-color: aquamarine;
}

.displayMe > span:nth-child(1) {
    background-color: lightcoral;
}

.displayMe > span:nth-child(2) {
    background-color: lightgreen;
}

.displayMe > span:nth-child(3) {
    background-color: lightpink;
}
```

<br>

En este ejemplo, se puede ver uno de los usos más simples de Flexbox. Se utiliza el `<div>` con la clase `displayMe` como contenedor de los otros tres elementos. A dicho contenedor se le especifica el tipo de *display* y se utiliza `justify-content: space-evenly;` para distribuir uniformemente los elementos *"hijos"* del contenedor.

Este es el resultado del código:

![8-flex](https://user-images.githubusercontent.com/110897750/202165845-41b08e0b-c873-44ba-9bf2-86372fb2b74a.jpg)

<sub>[Disposición, Posicionamiento y Overflow](../README.md#disposición-posicionamiento-y-overflow) | [Volver al índice](#indice)</sub>


<br><hr>


## inline-flex

Tal y como se ha visto al principio del contenido de este tema, al igual que ha pasado con `inline` y `block`, también se puede utilizar esta mezcla entre `inline` y `flex`.

* **inline:** porque inserta el bloque como si fuera texto.
* **Flexbox:** porque sus elementos *"hijos"* actúan como elementos Flexbox.

He aquí un ejemplo:

El código HTML se mantiene casi intacto desde el apartado anterior, únicamente se ha modificado el contenido de los `<span>` para reducir el espacio que ocupan:

```html
<div class="container">
    <p>
        Lorem ipsum dolor sit amet
        <div class="displayMe">
            <span>E1</span>
            <span>E2</span>
            <span>E3</span>
        </div>
        consectetur adipisicing elit. Tempora suscipit 
        quaerat adipisci provident, sit error libero 
        hic temporibus sed molestiae.
    </p>
</div>
```

<br>

En el CSS se realizan pequeños cambios que se explicarán a continuación:

```css
.displayMe {
    display: inline-flex;
    width: 100px;
    justify-content: space-evenly;
    background-color: aquamarine;
}

.displayMe > span:nth-child(1) {
    background-color: lightcoral;
}

.displayMe > span:nth-child(2) {
    background-color: lightgreen;
}

.displayMe > span:nth-child(3) {
    background-color: lightpink;
}
```

<br>

En este caso, el contenedor y los tres elemendos se encuentran insertados en el texto, debido al valor `inline`, sin embargo, se pueden aplicar las opciones de alineamiento como `justify-content` propias del Flexbox:

![9-inline-flex](https://user-images.githubusercontent.com/110897750/202165846-2323140c-5741-4f15-9572-bb93634024b7.jpg)

<sub>[Disposición, Posicionamiento y Overflow](../README.md#disposición-posicionamiento-y-overflow) | [Volver al índice](#indice)</sub>


<br><hr>


## grid

* **Cada una de las PROPIEDADES DEL CSS GRID se explican [AQUÍ](grid.md#grid) en un archivo a parte, para no hacer este apartado más extenso.**

Con este valor, se utiliza un tipo de display de *"rejilla"*, donde se define el tamaño de cada fila y/o columna del elemento *contenedor*.

Por sí mismo, este tipo de display funciona como `block`.

He aquí un ejemplo:

Se vuelve a utilizar el mismo código HTML que en el apartado anterior:

```html
<div class="container">
    <p>
        Lorem ipsum dolor sit amet
        <div class="displayMe">
            <span>E1</span>
            <span>E2</span>
            <span>E3</span>
        </div>
        consectetur adipisicing elit. Tempora suscipit 
        quaerat adipisci provident, sit error libero 
        hic temporibus sed molestiae.
    </p>
</div>
```

<br>

Esta vez, se modifica el `display` y se añade una propiedad típica de este tipo de display: `grid-template-columns`, con la que se define el tamaño de cada una de las columnas:

```css
.displayMe {
    display: grid;
    grid-template-columns: 3fr 1fr 2fr;
    background-color: aquamarine;
}

.displayMe > span:nth-child(1) {
    background-color: lightcoral;
}

.displayMe > span:nth-child(2) {
    background-color: lightgreen;
}

.displayMe > span:nth-child(3) {
    background-color: lightpink;
}
```

<br>

En este ejemplo se está definiendo el tipo de display a `grid`, y se indica que hay 3 columnas, definiendo también sus tamaños en fracciones (`3fr 1fr 2fr`).

Este es el resultado:

![10-grid](https://user-images.githubusercontent.com/110897750/202165848-d4725bd8-2895-4eca-852b-e4672147aeeb.jpg)

<sub>[Disposición, Posicionamiento y Overflow](../README.md#disposición-posicionamiento-y-overflow) | [Volver al índice](#indice)</sub>


<br><hr>


## inline-grid

De nuevo, el display de tipo `grid` también puede ser utilizado junto al valor `inline`, creando un valor con propiedades de ambos:

* **inline:** porque inserta el elemento como si se tratara de texto.
* **grid:** porque sus elementos *"hijos"* actúan como elementos de grid.

He aquí un ejemplo:

De nuevo, el código HTML se mantiene:

```html
<div class="container">
    <p>
        Lorem ipsum dolor sit amet
        <div class="displayMe">
            <span>E1</span>
            <span>E2</span>
            <span>E3</span>
        </div>
        consectetur adipisicing elit. Tempora suscipit 
        quaerat adipisci provident, sit error libero 
        hic temporibus sed molestiae.
    </p>
</div>
```

<br>

En este caso se modifica el tipo de display en el archivo CSS y además, se le indica un tamaño concreto al contenedor:

```css
.displayMe {
    display: inline-grid;
    grid-template-columns: 3fr 1fr 2fr;
    height: 50px;
    width: 200px;
    background-color: aquamarine;
}

.displayMe > span:nth-child(1) {
    background-color: lightcoral;
}

.displayMe > span:nth-child(2) {
    background-color: lightgreen;
}

.displayMe > span:nth-child(3) {
    background-color: lightpink;
}
```

<br>

Este es el resultado:

![11-inline-grid](https://user-images.githubusercontent.com/110897750/202165851-6b8c1e3e-b932-49dc-89c0-423ae5ccb9f4.jpg)

<sub>[Disposición, Posicionamiento y Overflow](../README.md#disposición-posicionamiento-y-overflow) | [Volver al índice](#indice)</sub>