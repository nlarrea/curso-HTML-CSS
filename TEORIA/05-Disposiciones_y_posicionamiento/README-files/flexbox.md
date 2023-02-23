# Flexbox

Ya se ha mencionado en el archivo de [Disposiciones](README-display.md) que el elemento *"padre"* actúa como un **contenedor Flexbox**, mientras que sus componentes *"hijos"* se convierten en **elementos Flexbox**.

<p id="indice">Por ello, en este apartado se van a explicar las propiedades pertenecientes a ellos, divididas de la siguiente manera:</p>

* [Propiedades para contenedores Flexbox](#propiedades-de-los-contenedores-flexbox)
  * [flex-direction](#flex-direction)
  * [flex-wrap](#flex-wrap)
  * [align-items](#align-items)
  * [justify-content](#justify-content)
  * [align-content](#align-content)
* [Propiedades para elementos Flexbox](#propiedades-de-los-elementos-flexbox)
  * [align-self](#align-self)
  * [flex-grow](#flex-grow)
  * [flex-shrink](#flex-shrink)
  * [order](#order)

<br>

[Disposición, Posicionamiento y Overflow](../README.md) | [Disposiciones](README-display.md)


<br><hr><br>


## Propiedades de los contenedores Flexbox

Las propiedades mostradas a continuación serán aquellas que deben definirse en el elemento *"padre"*, es decir, aquel que contenga en su interior a los demás elementos.

Para todos los ejemplos se va a utilizar el mismo código HTML, siendo este el siguiente:

```html
<div class="container">
    <div class="element">1</div>
    <div class="element">2</div>
    <div class="element">3</div>
    <div class="element">4</div>
    <div class="element">5</div>
</div>
```

<br>

Siendo este el código de CSS que se mantendrá constante casi todo el tiempo:

```css
.container {
    width: 500px;
    height: 100px;
    margin: 20px;
    padding: 10px;
    border: 1px solid black;
    background-color: bisque;
}

.element {
    width: 50px;
    height: 50px;
    text-align: center;
    line-height: 50px;
}

.element:nth-child(1){
    background-color: lightblue;
}
.element:nth-child(2){
    background-color: violet;
}
.element:nth-child(3){
    background-color: lightgreen;
}
.element:nth-child(4){
    background-color: yellow;
}
.element:nth-child(5){
    background-color: orange;
}
```


<br><hr>


### flex-direction

Cuando se tiene una cantidad de elementos dentro de un contenedor, se puede especificar en el contenedor cómo se desea que dichos elementos se posicionen.

A continuación, se van a mostrar varios ejemplos donde **sólo se mostrará el código CSS que sí ha sido añadido/modificado**:

* **`flex-direction: row;` *(por defecto)* y `flex-direction: row-reverse;`**

Código CSS añadido:

```css
.container {
    display: flex;
    flex-direction: row; /* no necesario */
}
```

<br>

Resultado del código anterior:

![1-flex-direction_row](https://user-images.githubusercontent.com/110897750/202166433-4eebd8ea-dc41-4573-ad4f-a56725353e07.jpg)

<br>

Código CSS añadido:

```css
.container {
    display: flex;
    flex-direction: row-reverse;
}
```

<br>

Resultado del código:

![2-flex-direction_row-reverse](https://user-images.githubusercontent.com/110897750/202166438-fd7c1933-e17f-441f-933e-356d41c26b58.jpg)

<br>

* **`flex-direction: column;` y `flex-direction: column-reverse;`**

Código CSS añadido:

```css
.container {
    height: 300px;
    display: flex;
    flex-direction: column;
}
```

<br>

Resultado del código:

![3-flex-direction_column](https://user-images.githubusercontent.com/110897750/202166440-3e37d060-9e38-45de-8d1d-6bbfd4970060.jpg)

<br>

Código CSS añadido:

```css
.container {
    height: 300px;
    display: flex;
    flex-direction: column-reverse;
}
```

<br>

Resultado del código:

![4-flex-direction_column-reverse](https://user-images.githubusercontent.com/110897750/202166442-a5bef6f5-3845-4ab6-b4c3-39973d673660.jpg)

<sub>[Disposición, Posicionamiento y Overflow](../README.md) | [Volver al índice](#indice) | [Disposiciones](README-display.md)</sub>


<br><hr>


### flex-wrap

En ocasiones se deseará ajustar el contenido de tal forma que "salte" a la siguiente línea si no cabe en el contenedor o sobrepasa ciertas medidas. Para ello, se utiliza esta propiedad, la cual tiene las siguientes opciones:

* **`flex-wrap: nowrap;`**

Si los elementos no entran en el contenedor, se redimensionarán uniformemente para poder entrar en el espacio definido.

Este es el código CSS añadido y modificado:

```css
.container {
    width: 250px;
    height: auto;
    display: flex;
    flex-direction: row;
    flex-wrap: nowrap;
}
```

<br>

Resultado del código:

![5-flex-wrap_nowrap](https://user-images.githubusercontent.com/110897750/202166444-bbb65587-02fa-4d4f-9589-7e71bcef4cdb.jpg)

<br>

* **`flex-wrap: wrap;`**

Si los elementos no entran en el contenedor, aquel que *"sobre"* para no sobrepasar el espacio será enviado a la siguiente línea.

Este es el código CSS añadido y modificado:

```css
.container {
    width: 250px;
    height: auto;
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
}
```

<br>

Resultado del código:

![6-flex-wrap_wrap](https://user-images.githubusercontent.com/110897750/202166447-0e49d80f-2e8d-4853-9d64-b17975a4dc0b.jpg)

<br>

* **`flex-wrap: wrap-reverse;`**

En este caso, si los elementos no entran en el contenedor, aquel que *"sobre"* para no sobrepasar el espacio será el que se quede en la línea superior y los demás serán enviados a la siguiente línea.

Este es el código CSS añadido y modificado:

```css
.container {
    width: 250px;
    height: auto;
    display: flex;
    flex-direction: row;
    flex-wrap: wrap-reverse;
}
```

<br>

Resultado del código:

![7-flex-wrap_wrap-reverse](https://user-images.githubusercontent.com/110897750/202166449-767232ba-7a81-4bf9-9ddf-bc035775307e.jpg)

<sub>[Disposición, Posicionamiento y Overflow](../README.md) | [Volver al índice](#indice) | [Disposiciones](README-display.md)</sub>


<br><hr>


### align-items

Como bien su nombre indica, esta propiedad sirve para alinear los elementos en uno de los ejes (X o Y). El eje dependerá del valor introducido en `flex-direction`, siendo por defecto el eje Y (al ser `flex-direction: row` el valor por defecto).

Estos son sus valores posibles:

* **`align-items: flex-start;`**

Alinea todos los elementos en la parte superior (`flex-direction: row`) o a la izquierda (`flex-direction: column`). Este es el código CSS añadido y modificado:

```css
.container {
    width: fit-content;
    height: auto;
    display: flex;
    align-items: flex-start;
}

.element:nth-child(1){
    height: 40px;
}
.element:nth-child(2){
    height: 80px;
}
.element:nth-child(3){
    height: 60px;
}
.element:nth-child(5){
    height: 60px;
}
```

<br>

Este es el resultado del código:

![8-align-items_flex-start](https://user-images.githubusercontent.com/110897750/202166452-2cbf8f5b-ac60-40a3-9934-ca7a319514a9.jpg)

<br>

* **`align-items: flex-end;`**

Es exactamente igual que el anterior, solo que alineando los elementos abajo, por defecto, o a la derecha cuando la dirección del display es en columna. Este es el código CSS añadido y modificado:

```css
.container {
    width: fit-content;
    height: auto;
    display: flex;
    align-items: flex-end;
}

.element:nth-child(1){
    height: 40px;
}
.element:nth-child(2){
    height: 80px;
}
.element:nth-child(3){
    height: 60px;
}
.element:nth-child(5){
    height: 60px;
}
```

<br>

Este es el resultado del código:

![9-align-items_flex-end](https://user-images.githubusercontent.com/110897750/202166455-5c7acb28-1731-482d-b850-4c99d3d3d107.jpg)

<br>

* **`align-items: center;`**

Alinea todos los elementos en el centro del eje, sea cual sea. Este es el código CSS añadido y modificado:

```css
.container {
    width: fit-content;
    height: auto;
    display: flex;
    align-items: center;
}

.element:nth-child(1){
    height: 40px;
}
.element:nth-child(2){
    height: 80px;
}
.element:nth-child(3){
    height: 60px;
}
.element:nth-child(5){
    height: 60px;
}
```

<br>

Se ha añadido una línea roja mostrando por dónde se han alineado los elementos. Hay que tener en cuenta que **dicha línea no es añadida por el código**, su objetivo es únicamente mostrar la alineación.

Este es el resultado del código:

![10-align-items_center](https://user-images.githubusercontent.com/110897750/202166459-f9bc337f-081b-4658-be5f-d75af9e749d5.jpg)

<br>

* **`align-items: baseline;`**

Con este valor, los elementos son alineados en la base del eje. Este es el código CSS utilizado:

```css
.container {
    width: fit-content;
    height: auto;
    display: flex;
    align-items: center;
}

.element:nth-child(1){
    height: 40px;
}
.element:nth-child(2){
    height: 80px;
}
.element:nth-child(3){
    height: 60px;
}
.element:nth-child(5){
    height: 60px;
}
```

<br>

Se ha añadido una línea roja mostrando por dónde se han alineado los elementos. Hay que tener en cuenta que **dicha línea no es añadida por el código**, su objetivo es únicamente mostrar la alineación.

Este es el resultado del código:

![11-align-items_baseline](https://user-images.githubusercontent.com/110897750/202166461-758d2c8d-cf4e-4978-a0f4-a0b2ed42f6dc.jpg)

<br>

* **`align-items: stretch;`**

Este valor alargará los elementos hasta ocupar el máximo espacio permitido por el contenedor. El código CSS añadido y modificado se muestra a continuación:

```css
.container {
    width: fit-content;
    height: 100px;
    display: flex;
    align-items: stretch;
}

.element {
    width: 50px;
    /* height: 50px -> no definir altura */
}
```

<br>

Este es el resultado del código:

![12-align-items_stretch](https://user-images.githubusercontent.com/110897750/202166464-5a6cad0e-906d-4b65-9f8a-783ccbb3a091.jpg)

<sub>[Disposición, Posicionamiento y Overflow](../README.md) | [Volver al índice](#indice) | [Disposiciones](README-display.md)</sub>


<br><hr>


### justify-content

Esta propiedad es complementaria a la propiedad anterior. Permite alinear los elementos en el eje principal.

Estos son sus valores posibles:

* **`justify-content: flex-start;`**

Su valor por defecto es `justify-content: flex-start;`, el cual alinea los elementos llevándolos a la izquierda (cuando `flex-direction` tiene el valor de `row`). Este es el código CSS utilizado:

```css
.container {
    width: 400px;
    height: fit-content;
    display: flex;
    justify-content: flex-start;
}
```

<br>

Este es el resultado del código:

![13-justify-content_flex-start](https://user-images.githubusercontent.com/110897750/202166467-412ea8ce-5963-4535-8483-613521517415.jpg)

<br>

* **`justify-content: flex-end;`**

Alinea los elementos de forma contraria al `flex-start`, es decir, alinea los elementos llevando los elementos hacia la derecha. Este es el código CSS:

```css
.container {
    width: 400px;
    height: fit-content;
    display: flex;
    justify-content: flex-end;
}
```

<br>

Este es el resultado del código:

![14-justify-content_flex-end](https://user-images.githubusercontent.com/110897750/202166468-f20341a1-fe6e-469d-8fe2-7a6f42651af3.jpg)

<br>

* **`justify-content: space-between;`, `justify-content: space-around;` y `justify-content: space-evenly;`**

Los tres valores permiten separar los elementos en el eje principal distribuyéndolos uniformemente de la siguiente manera:
  
  1. **space-between:** distribuye todos los elementos sin dejan ningún márgen lateral exterior en el primer y último elemento.

```css
.container {
    width: 400px;
    height: fit-content;
    padding: 10px 0;
    display: flex;
    justify-content: space-between;
}
```

<br>

Este es el resultado:

![15-justify-content_space-between](https://user-images.githubusercontent.com/110897750/202166470-d8aa2168-ac31-445b-b71f-921164e89760.jpg)

<br>

  2. **space-around:** distribuye todos los elementos dejando un margen lateral igual a la mitad del espacio que deja entre los elementos.

```css
.container {
    width: 400px;
    height: fit-content;
    padding: 10px 0;
    display: flex;
    justify-content: space-around;
}
```

<br>

Este es el resultado:

![16-justify-content_space-around](https://user-images.githubusercontent.com/110897750/202166473-0e9c642f-fa1e-4dc0-b748-c8b904cd832f.jpg)

<br>

  3. **space-evenly:** distribuye los elementos de forma equitativa, dejando el mismo espacio entre elementos y el *borde exterior*.

```css
.container {
    width: 400px;
    height: fit-content;
    padding: 10px 0;
    display: flex;
    justify-content: space-evenly;
}
```

<br>

Este es el resultado:

![17-justify-content_space-evenly](https://user-images.githubusercontent.com/110897750/202166476-dd48f9fe-c548-43a6-98e2-6e242be6cd03.jpg)

<sub>[Disposición, Posicionamiento y Overflow](../README.md) | [Volver al índice](#indice) | [Disposiciones](README-display.md)</sub>


<br><hr>


### align-content

Esta propiedad define cómo cada línea es alineada.

Para su uso, debe haber más de una línea y estar definido el `flex-wrap: wrap`.

Se añaden más elementos en el archivo HTML y se les da formato usando CSS:

```html
<div class="container">
    <div class="element">1</div>
    <div class="element">2</div>
    <div class="element">3</div>
    <div class="element">4</div>
    <div class="element">5</div>
    <div class="element">6</div>
    <div class="element">7</div>
    <div class="element">8</div>
    <div class="element">9</div>
</div>
```

Estos son sus posibles valores:

* **`align-content: flex-start;`**

Sigue el mismo principio visto en [align-items](#align-items) con el `flex-start`, pero con más filas de elementos:

```css
.container {
    width: 200px;
    height: 300px;
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    align-content: flex-start;
}
```

<br>

Este es el resultado:

![18-align-content_flex-start](https://user-images.githubusercontent.com/110897750/202166478-1fffa438-38de-4358-b2f7-c19d5ccd0079.jpg)

<br>

* **`align-content: flex-end;`**

Sigue el mismo principio visto en [align-items](#align-items) con el `flex-end`, pero con más filas de elementos:

```css
.container {
    width: 200px;
    height: 300px;
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    align-content: flex-end;
}
```

<br>

Este es el resultado:

![19-align-content_flex-end](https://user-images.githubusercontent.com/110897750/202166479-22b846fc-619b-4e8f-b474-53c3d5565e10.jpg)

<br>

* **`align-content: center;`**

Sigue el mismo principio visto en [align-items](#align-items) con el `center`, pero con más filas de elementos:

```css
.container {
    width: 200px;
    height: 300px;
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    align-content: center;
}
```

<br>

Este es el resultado:

![20-align-content_center](https://user-images.githubusercontent.com/110897750/202166480-49242765-845f-4613-aeb9-83bd41074148.jpg)

<br>

* **`align-content: space-between;`, `align-content: space-around;` y `align-content: space-evenly;`**

Sigue el mismo principio visto en [align-items](#align-items) con el `space-between`, `space-around` y `space-evenly`, pero con más filas de elementos:

  1. **space-between:** distribuye todos los elementos sin dejan ningún márgen lateral exterior en el primer y último elemento.

```css
.container {
    width: 200px;
    height: 300px;
    /*padding: 10px;*/
    display: flex;
    flex-wrap: wrap;
    align-content: space-between;
}
```

<br>

Este es el resultado:

![21-align-content_space-between](https://user-images.githubusercontent.com/110897750/202166486-4f58da50-735b-4b7f-b472-cee3e124a6bc.jpg)

<br>

  2. **space-around:** distribuye todos los elementos dejando un margen lateral igual a la mitad del espacio que deja entre los elementos.

```css
.container {
    width: 200px;
    height: 300px;
    /*padding: 10px;*/
    display: flex;
    flex-wrap: wrap;
    align-content: space-around;
}
```

<br>

Este es el resultado:

![22-align-content_space-around](https://user-images.githubusercontent.com/110897750/202166488-535c6dbd-1487-469f-b029-5373e7fd9ecf.jpg)

<br>

  3. **space-evenly:** distribuye los elementos de forma equitativa, dejando el mismo espacio entre elementos y el *borde exterior*.

```css
.container {
    width: 200px;
    height: 300px;
    /*padding: 10px;*/
    display: flex;
    flex-wrap: wrap;
    align-content: space-evenly;
}
```

<br>

Este es el resultado:

![23-align-content_space-evenly](https://user-images.githubusercontent.com/110897750/202166491-5e112b58-9d95-406d-a5da-db5dafa8c0b0.jpg)

<sub>[Disposición, Posicionamiento y Overflow](../README.md) | [Volver al índice](#indice) | [Disposiciones](README-display.md)</sub>


<br><hr>
<hr><br>


## Propiedades de los elementos Flexbox

Las propiedades mostradas a continuación serán aquellas que deben definirse en los elementos *"hijos"*, es decir, aquellos que se encuentran dentro del *contenedor*.

El código HTML a utilizar es el mostrado a continuación:

```html
<div class="container">
    <div class="element">1</div>
    <div class="element">2</div>
    <div class="element">3</div>
    <div class="element">4</div>
    <div class="element">5</div>
</div>
```

Donde el código CSS por defecto será el siguiente:

```css
.container {
    width: 300px;
    height: fit-content;
    margin: 20px;
    padding: 10px;
    border: 1px solid black;
    background-color: darkslategrey;
    display: flex;
}

.element {
    width: 50px;
    height: 50px;
}

.element:nth-child(1){
    background-color: #2A80B9; /* azul oscuro */
}

.element:nth-child(2){
    background-color: #8F44AD; /* violeta oscuro */
}

.element:nth-child(3){
    background-color: #16A086; /* verde oscuro */
}

.element:nth-child(4){
    background-color: #F1C40F; /* amarillo anaranjado */
}

.element:nth-child(5){
    background-color: #E77E23; /* naranja */
}
```


<br><hr>


### align-self

Esta propiedad trabaja exactamente igual que `align-items`, solo que es aplicada únicamente a un elemento concreto.

Por ello, se mostrarán imágenes a modo de ejemplo sin entrar en explicaciones que [ya hayan sido realizadas](#align-items) y se explicarán aquellas que no hayan sido vistas con anterioridad.

* **`align-self: auto;` *(por defecto)***

Código CSS utilizado para este ejemplo:

```css
.container {
    display: flex;
    align-items: center;
}

.element:nth-child(2){
    align-self: center; /* por defecto */
}
```

<br>

Este es el resultado:

![1-align-self_auto](https://user-images.githubusercontent.com/110897750/202167284-589afbb4-2515-49b0-871c-7d108104c9c3.jpg)

<br>

* **`align-self: flex-start;`**

Código CSS modificado:

```css
.element:nth-child(2){
    align-self: flex-start;
}
```

<br>

Este es el resultado:

![2-align-self_flex-start](https://user-images.githubusercontent.com/110897750/202167286-bf30e350-822f-4ae3-b1b7-5121b3c89d04.jpg)

<br>

* **`align-self: flex-end;`**

Código CSS modificado:

```css
.element:nth-child(2){
    align-self: flex-end;
}
```

<br>

Este es el resultado de dicho código:

![3-align-self_flex-end](https://user-images.githubusercontent.com/110897750/202167287-cc093812-2219-4a20-98ba-4f4428fa153c.jpg)

<br>

* **`align-self: center;`**

Código CSS modificado:

```css
.element:nth-child(2){
    align-self: center;
}
```

<br>

En este caso, el resultado se ve idéntico al mostrado con `align-self: auto` debido a que con el auto se heredaba el valor del elemento *"padre"*, el cual era `center`.

Por ello, este es el resultado de dicho código:

![4-align-self_center](https://user-images.githubusercontent.com/110897750/202167289-fdca3e44-a19a-4f77-a93a-1a1073c14209.jpg)

<br>

* **`align-self: baseline;`**

Este es el código CSS modificado:

```css
.element:nth-child(2){
    align-self: baseline;
}
```

<br>

Se ha añadido una línea roja mostrando por dónde se han alineado los elementos haciendo uso de las propiedades del contenedor, `align-items: center`, y una línea blanca donde se muestra por dónde se ha alineado el elemento número 2, haciendo uso de `align-self: baseline`. Hay que tener en cuenta que **dicha línea no es añadida por el código**, su objetivo es únicamente mostrar la alineación.

Este es el resultado del código:

![5-align-self_baseline](https://user-images.githubusercontent.com/110897750/202167291-250caeb8-fb55-49e0-8a9c-e3ea2641aed1.jpg)

<br>

* **`align-self: stretch;`**

Este es el código CSS modificado:

```css
.element {
    width: 50px;
    /* height: 50px; -> no modificar la altura */
}

.element:nth-child(2){
    align-self: stretch;
}
```

<br>

Este es el resultado del código:

![6-align-self_stretch](https://user-images.githubusercontent.com/110897750/202167294-5e977aa9-6591-4193-9ee3-57133a5af860.jpg)

<sub>[Disposición, Posicionamiento y Overflow](../README.md) | [Volver al índice](#indice) | [Disposiciones](README-display.md)</sub>


<br><hr>


### flex-grow

Con esta propiedad se puede modificar el tamaño de los elementos deseados. A continuación, se utiliza esta propiedad con algunos de los elementos *"hijos"* para demostrar cómo funciona.

Este es el código CSS modificado:

```css
.element {
    width: 50px;
    height: 50px;
}

.element:nth-child(1){
    background-color: #2A80B9;
    flex-grow: 0.5;
}

.element:nth-child(2){
    background-color: #8F44AD;
    flex-grow: 2;
}

.element:nth-child(3){
    background-color: #16A086;
}

.element:nth-child(4){
    background-color: #F1C40F;
    flex-grow: 1;
}

.element:nth-child(5){
    background-color: #E77E23;
}
```

<br>

Este es el resultado:

![7-flex-grow](https://user-images.githubusercontent.com/110897750/202167295-4e3b4016-9177-4eb6-b746-98fe1ef32890.jpg)

<sub>[Disposición, Posicionamiento y Overflow](../README.md) | [Volver al índice](#indice) | [Disposiciones](README-display.md)</sub>


<br><hr>


### flex-shrink

Esta propiedad es muy útil cuando se dispone de una cantidad de elementos *"hijos"* que ocupan o sobrepasan el espacio total del elemento *"padre"*, es decir, del contenedor. Sirve para comunicar a cada elemento cuánto debe empequeñecerse para permitir a todos los elementos entrar dentro del espacio disponible.

Este es el código CSS en este caso:

```css
.element:nth-child(1){
    background-color: #2A80B9;
    flex-shrink: 1;
}

.element:nth-child(2){
    background-color: #8F44AD;
    flex-shrink: 2;
}

.element:nth-child(3){
    background-color: #16A086;
}

.element:nth-child(4){
    background-color: #F1C40F;
    flex-shrink: 3;
}

.element:nth-child(5){
    background-color: #E77E23;
}
```

<br>

Este es el resultado:

![8-flex-shrink](https://user-images.githubusercontent.com/110897750/202167298-0a2d9e5f-5fcd-428f-ac3d-e6fd4b75969c.jpg)

<sub>[Disposición, Posicionamiento y Overflow](../README.md) | [Volver al índice](#indice) | [Disposiciones](README-display.md)</sub>


<br><hr>


### order

Esta propiedad permite reordenar los elementos contenidos en el elemento *"padre"*. Esta opción es muy útil y utilizada cuando se diseña una aplicación para diferentes tamaños de pantalla, puesto que permite modificar el orden en el que se muestra el contenido, por ejemplo.

Este sería el código CSS utilizado:

```css
.element:nth-child(1){
    background-color: #2A80B9;
    order: 4;
}

.element:nth-child(2){
    background-color: #8F44AD;
    order: 2;
}

.element:nth-child(3){
    background-color: #16A086;
    /* order: 1 -> por defecto */
}

.element:nth-child(4){
    background-color: #F1C40F;
    order: 2;
}

.element:nth-child(5){
    background-color: #E77E23;
    order: 3;
}
```

<br>

* El primer bloque en aparecer es el número 3. No se le ha asignado ningún valor a la propiedad `order` a este elemento, sin embargo, su valor por defecto es 1, por eso ocupa el primer puesto.
* Los bloques 2 y 4 tienen el valor 2 asignado, por ello, debido a que el bloque 2 es el primero al que se le asigna dicho valor, aparecen el 2 y el 4 a continuación.
* El bloque 5 tiene el valor 3 en la propiedad `order`, por lo que se coloca después del 2 y el 4.
* Por último, el bloque 1 tiene el valor 4, por lo que es el último en posicionarse.

Este sería el resultado:

![9-order](https://user-images.githubusercontent.com/110897750/202167299-13de652b-71d3-4d24-b19b-ec6040376c47.jpg)

<sub>[Disposición, Posicionamiento y Overflow](../README.md) | [Volver al índice](#indice) | [Disposiciones](README-display.md)</sub>