# Grid

Ya se ha mencionado en el archivo de [Disposiciones](README-display.md) que se utiliza una disposición de tipo *"rejilla"*, con la que definir el tamaño y la ubicación de cada uno de los elementos.

<p id="indice">Por ello, en este apartado se van a explicar las propiedades pertenecientes a este tipo de display, divididas de la siguiente manera:</p>

* [Posicionamiento del elemento](#posicionamiento-de-los-elementos)
  * [grid-column-start & grid-row-start](#grid-column-start--grid-row-start)
  * [grid-column-end & grid-row-end](#grid-column-end--grid-row-end)
  * [grid-column & grid-row](#grid-column--grid-row)
  * [grid-area](#grid-area)
  * [grid-auto-flow](#grid-auto-flow)
* [Definición de espacio](#definición-de-espacio-o-tamaño)
  * [grid-template-columns & grid-template-rows](#grid-template-columns--grid-template-rows)
  * [grid-template-areas](#grid-template-areas)
  * [grid-template](#grid-template)
  * [grid-auto-columns & grid-auto-rows](#grid-auto-columns--grid-auto-rows)
  * [grid](#grid-1)
* [Espacios entre celdas](#espacios-entre-celdas)
  * [column-gap](#column-gap)
  * [row-gap](#row-gap)
  * [grid-gap](#grid-gap)

<br>

[Disposición, Posicionamiento y Overflow](../README.md) | [Disposiciones](README-display.md)


<br><hr><br>


## Posicionamiento de los elementos

En este apartado se va a hablar de cómo posicionar los elementos haciendo uso de `grid` y algunas de sus propiedades.

Este será el código HTML a utilizar principalmente, aunque podría sufrir modificaciones para algún ejemplo concreto. En dicho caso, se indicarían cuáles han sido esos cambios:

```html
<div class="container">
    <div class="element">Item 1</div>
    <div class="element">Item 2</div>
    <div class="element">Item 3</div>
    <div class="element">Item 4</div>
    <div class="element">Item 5</div>
    <div class="element">Item 6</div>
</div>
```

<br>

Por otro lado, dichos elementos han recibido el siguiente estilo de base:

```css
.container {
    width: 400px;
    height: 200px;
    margin: 20px;
    padding: 10px;
    border: 1px solid black;
    background-color: darkslategrey;
    display: grid;
}

.element:nth-child(1){
    background-color: #D66DDC; /* violeta */
}

.element:nth-child(2){
    background-color: #32BBAB; /* azul verdoso */
}

.element:nth-child(3){
    background-color: #09C46A; /* verde */
}

.element:nth-child(4){
    background-color: #E9C46A; /* amarillo */
}

.element:nth-child(5){
    background-color: #F4A261; /* naranja */
}

.element:nth-child(6) {
    background-color: #FF6363; /* rojo */
}
```

<br><hr>

### grid-column-start & grid-row-start

* **`grid-column-start`**

Define la columna en la que debe comenzar el **ítem** seleccionado. Tener en cuenta que afecta al ítem, por lo que se debe especificar el *layout en el contenedor* previamente (esto será explicado [más adelante](#grid-template-columns--grid-template-rows)).

He aquí un ejemplo usando `grid-column-start`:

```css
.container {
    display: grid;
    /* más adelante se explica qué es lo qué 
    se consigue con esta línea de abajo */
    grid-template-columns: repeat(3, 1fr);
}

.element:nth-child(2){
    grid-column-start: auto; /* por defecto */
}
```

<br>

Como se puede observar, aparentemente no ha ocurrido nada. Esto se debe a que el valor `auto` es el usado por defecto.

Este sería el resultado:

![1-grid-column-start_auto](https://user-images.githubusercontent.com/110897750/202167806-02010e94-6611-4f5f-93a2-063223a07897.jpg)

<br>

Veamos ahora qué ocurre si modificamos este valor:

```css
.container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
}

.element:nth-child(2){
    grid-column-start: 3;
}
```

<br>

En este caso, si han sido desplazados los elementos, debido a que al elemento 2 se le ha indicado que comience en la columna número 3, y éste ha hecho que los siguientes ítems se muevan también a las siguientes posiciones.

Este es el resultado:

![2-grid-column-start_3](https://user-images.githubusercontent.com/110897750/202167811-88a1b33f-e8bd-44b6-9c64-e66be0e94a43.jpg)

<br>

* **`grid-row-start`**

Define la fila en la que debe comenzar el **ítem** seleccionado. Tener en cuenta que afecta al ítem, por lo que se debe especificar el *layout en el contenedor* previamente (esto será explicado [más adelante](#grid-template-columns--grid-template-rows)).

Siguendo el mismo ejemplo que en el punto anterior:

```css
.container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
}

.element:nth-child(2){
    grid-row-start: 3;
}
```

<br>

Este es el resultado:

![3-grid-row-start_3](https://user-images.githubusercontent.com/110897750/202167814-b092de92-192a-4a9a-851d-5b0daea07958.jpg)

<sub>[Disposición, Posicionamiento y Overflow](../README.md) | [Volver al índice](#indice) | [Disposiciones](README-display.md)</sub>


<br><hr>


### grid-column-end & grid-row-end

Funciona con la misma idea que la vista en el [apartado anterior](#grid-column-start--grid-row-start), pero en vez de indicar la posición de inicio, **se indica en cuál debe finalizar**.

* **`grid-column-end`**

He aquí un ejemplo:

```css
.container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
}

.element:nth-child(2){
    grid-column-end: 2;
}
```

<br>

En este caso se le ha indicado al ítem 2 que finalice en la segunda columna, por lo que éste se colocará en la primera columna saltando a la siguiente fila y arrastrando a los elementos que se posicionen detrás suyo.

Este es el resultado:

![4-grid-column-end](https://user-images.githubusercontent.com/110897750/202167815-a0383386-da7c-491a-94f0-1f67cbe19703.jpg)

<br>

* **`grid-row-end`**

Siguiendo el mismo ejemplo que el de antes:

```css
.container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
}

.element:nth-child(2){
    grid-row-end: 4;
}
```

<br>

Este es el resultado:

![5-grid-row-end_4](https://user-images.githubusercontent.com/110897750/202167819-262369be-30e5-4d00-9ad4-c3ae295d129b.jpg)

<sub>[Disposición, Posicionamiento y Overflow](../README.md) | [Volver al índice](#indice) | [Disposiciones](README-display.md)</sub>


<br><hr>


### grid-column & grid-row

Estas dos propiedades son las abreviaciones correspondientes a:

* **grid-column:** grid-column-start & grid-column-end
* **grid-row:** grid-row-start & grid-row-end

Con estas propiedades, **cambiar el posicionamiento y el tamaño** es una tarea muy sencilla y que se puede lograr con apenas unas líneas de código:

```css
.element:nth-child(2){
    /* desde la fila 1 hasta la 3 */
    grid-row: 1 / 3;
}

.element:nth-child(6) {
    /* desde fila 2 hasta fila 3 */
    grid-row: 2 / 3;
    /* desde columna 2 hasta columna 4 */
    grid-column: 2 / 4;
}
```

<br>

Como se puede ver en el bloque de código, se pueden realizar combinaciones de columnas y filas, modificando así totalmente la posición y/o el tamaño del **ítem**.

Este es el resultado de dicho código:

![6-grid-column--grid-row](https://user-images.githubusercontent.com/110897750/202167824-4ef92e72-2ce8-4582-8258-422772158b8f.jpg)

<sub>[Disposición, Posicionamiento y Overflow](../README.md) | [Volver al índice](#indice) | [Disposiciones](README-display.md)</sub>


<br><hr>


### grid-area

Ya hemos visto que existe una **forma abreviada de usar y definir columnas y filas** haciendo uso de `grid-column` y `grid-row`, sin embargo, éstas pueden ser abreviadas de nuevo con esta propiedad.

He aquí una muestra haciendo uso del ejemplo del apartado anterior:

```css
.element:nth-child(2){
    /* desde: fila 1, columna 1
    hasta: fila 3, columna 2 */
    grid-area: 1 / 1 / 3 / 2;
}

.element:nth-child(6) {
    /* desde: fila 2, columna 2
    hasta: fila 3, columna 4 */
    grid-area: 2 / 2 / 3 / 4;
}
```

<br>

Como se puede observar en la imagen a continuación, se ha conseguido el mismo resultado que en el último ejemplo visto en el apartado anterior:

![7-grid-area](https://user-images.githubusercontent.com/110897750/202167825-181c8977-df34-418b-9e4f-eb612f677b8b.jpg)

<sub>[Disposición, Posicionamiento y Overflow](../README.md) | [Volver al índice](#indice) | [Disposiciones](README-display.md)</sub>


<br><hr>


### grid-auto-flow

Esta propiedad permite definir la posición de los **elementos grid** que hayan sido generados automáticamente.

* **`grid-auto-flow: row;` *(por defecto)***

He aquí un ejemplo con el valor `row`:

```css
.container {
    display: grid;
    /* se definen las areas */
    grid-template-areas: 
        "header header header"
        "sidebar main main"
        "footer footer footer";
    /* se usa el valor fila */
    grid-auto-flow: row;
}

.element:nth-child(1){
    /* ocupará todo el header */
    grid-area: header;
}

.element:nth-child(2){
    /* ocupará todo el sidebar */
    grid-area: sidebar;
}

.element:nth-child(3){
    /* ocupará todo el main */
    grid-area: main;
}

.element:nth-child(4){
    /* ocupará todo el footer */
    grid-area: footer;
}
```

<br>

El *Item 5* y el *Item 6* no tienen especificada ninguna posición. Estos dos son considerados **ítems de tipo grid auto-generados**. Al especificar el valor `grid-auto-flow: row`, éstos son desplazados a una nueva fila.

Este es el resultado:

![8-grid-auto-flow_row](https://user-images.githubusercontent.com/110897750/202167827-819285c4-f9ec-4979-82c9-4847e6bbc159.jpg)

<br>

* **`grid-auto-flow: column;`**

Ahora, se muestra el mismo ejemplo utilizando el valor `column`:

```css
.container {
    display: grid;
    /* se definen las areas */
    grid-template-areas: 
        "header header header"
        "sidebar main main"
        "footer footer footer";
    /* se usa el valor columna */
    grid-auto-flow: column;
}

.element:nth-child(1){
    /* ocupará todo el header */
    grid-area: header;
}

.element:nth-child(2){
    /* ocupará todo el sidebar */
    grid-area: sidebar;
}

.element:nth-child(3){
    /* ocupará todo el main */
    grid-area: main;
}

.element:nth-child(4){
    /* ocupará todo el footer */
    grid-area: footer;
}
```

<br>

El *Item 5* y el *Item 6* no tienen especificada ninguna posición. Estos dos son considerados **ítems de tipo grid auto-generados**. Al especificar el valor `grid-auto-flow: column`, éstos son desplazados a una nueva columna.

Este es el resultado:

![9-grid-auto-flow_column](https://user-images.githubusercontent.com/110897750/202167830-545cf013-cbc9-4287-b14e-fd5e6951629b.jpg)

<sub>[Disposición, Posicionamiento y Overflow](../README.md) | [Volver al índice](#indice) | [Disposiciones](README-display.md)</sub>


<br><hr>
<hr><br>


## Definición de espacio o tamaño

Con estas propiedades se va a poder definir cómo se desea que sean las filas y columnas dentro del **contenedor**.

Se mantiene el código base visto en el apartado de [Posicionamiento de los elementos](#posicionamiento-de-los-elementos):

```html
<div class="container">
    <div class="element">Item 1</div>
    <div class="element">Item 2</div>
    <div class="element">Item 3</div>
    <div class="element">Item 4</div>
    <div class="element">Item 5</div>
    <div class="element">Item 6</div>
</div>
```

<br>

Y el código CSS correspondiente:

```css
.container {
    width: 400px;
    height: 200px;
    margin: 20px;
    padding: 10px;
    border: 1px solid black;
    background-color: darkslategrey;
    display: grid;
}

.element:nth-child(1){
    background-color: #D66DDC; /* violeta */
}

.element:nth-child(2){
    background-color: #32BBAB; /* azul verdoso */
}

.element:nth-child(3){
    background-color: #09C46A; /* verde */
}

.element:nth-child(4){
    background-color: #E9C46A; /* amarillo */
}

.element:nth-child(5){
    background-color: #F4A261; /* naranja */
}

.element:nth-child(6) {
    background-color: #FF6363; /* rojo */
}
```


<br><hr>


### grid-template-columns & grid-template-rows

Ambas propiedades sirven para definir las columnas o las filas dentro del **contenedor**.

Se puede especificar el tamaño utilizando `auto` *(por defecto)*, lo cual permite que ocupe el espacio o se distribuyan uniformemente, o utilizar unidades de medida como `px`, `em`, `rem` o `fr` (fracción).

He aquí un ejemplo:

```css
.container {
    display: grid;
    grid-template-columns: 1fr 7em 60px;
    grid-template-rows: 2fr 1fr;
}
```

<br>

En esas líneas de código hemos especificado qué tamaño debe ocupar cada una de las 3 columnas y cada una de las dos filas. Podrían haberse especificado únicamente las columnas o las filas, ya que por defecto el valor es siempre `auto`.

Este es el resultado:

![10-grid-template-columns--grid-template-rows](https://user-images.githubusercontent.com/110897750/202167834-d0958bf8-e68f-4776-a80a-378ac3c8d6cc.jpg)

<sub>[Disposición, Posicionamiento y Overflow](../README.md) | [Volver al índice](#indice) | [Disposiciones](README-display.md)</sub>


<br><hr>


### grid-template-areas

Esta propiedad ha sido usada en ejemplos anteriores. Sirve para definir áreas **dentro del contenedor**. Después, dichas áreas son referenciadas en los elementos *"hijos"*.

El valor *por defecto* es `none`.

Este sería un ejemplo donde damos espacio a cada elemento:

```css
.container {
    display: grid;
    grid-template-areas:
        "logo header header"
        "sidebar main image"
        "footer footer footer";
}

.element:nth-child(1){
    grid-area: header;
}

.element:nth-child(2){
    grid-area: logo;
}

.element:nth-child(3){
    grid-area: sidebar;
}

.element:nth-child(4){
    grid-area: main;
}

.element:nth-child(5){
    grid-area: image;
}

.element:nth-child(6) {
    grid-area: footer;
}
```

<br>

Este es el resultado:

![11-grid-template-areas](https://user-images.githubusercontent.com/110897750/202167837-b3d65983-de30-404d-bad2-7a0a1fdda0bf.jpg)

<sub>[Disposición, Posicionamiento y Overflow](../README.md) | [Volver al índice](#indice) | [Disposiciones](README-display.md)</sub>


<br><hr>


### grid-template

Esta es la forma abreviada de escribir estas tres propiedades:

* grid-template-columns
* grid-template-rows
* grid-template-areas

Su valor *por defecto* es `none`.

He aquí un ejemplo:

```css
.container {
    display: grid;
    /* se definen las filas y luego las columnas */
    grid-template: 50px auto / 1fr 5em 80px;
}
```

<br>

Este es el resultado de dicho código:

![12-grid-template](https://user-images.githubusercontent.com/110897750/202167839-6ce2bc34-6d9e-46e6-ad66-8fc9e1662220.jpg)

<br>

Otra opción posible:

```css
.container {
    display: grid;
    grid-template:
        "logo header header" 50px
        "sidebar main image" 100px
        "footer footer footer" auto;
}

.element:nth-child(1){
    grid-area: header;
}

.element:nth-child(2){
    grid-area: logo;
}

.element:nth-child(3){
    grid-area: sidebar;
}

.element:nth-child(4){
    grid-area: main;
}

.element:nth-child(5){
    grid-area: image;
}

.element:nth-child(6) {
    grid-area: footer;
}
```

<br>

En esta ocasión, se especifican las columnas y después se indica que la primera fila sea de `50px`, la segunda de `100px` y la tercera tenga un valor de `auto`.

Este es el resultado:

![12-grid-template-2](https://user-images.githubusercontent.com/110897750/202167843-75e07355-0f2e-401e-b6cb-c70b98f8b25a.jpg)

<sub>[Disposición, Posicionamiento y Overflow](../README.md) | [Volver al índice](#indice) | [Disposiciones](README-display.md)</sub>


<br><hr>


### grid-auto-columns & grid-auto-rows

En ocasiones, se dispondrá de elementos a los que no se les ha sido asignada una posición y, por tanto, tampoco un tamaño. Para estas situaciones, se utilizan estas dos propiedades.

El valor *por defecto* de cada una es `auto`.

* **`grid-auto-columns`**

He aquí un ejemplo:

```css
.container {
    display: grid;
    grid-template-areas:
        "header header header"
        "sidebar main main";
    grid-template-columns: 80px 100px;
    grid-auto-columns: 1fr;
}

.element:nth-child(1){
    background-color: #D66DDC;
    grid-area: header;
}

.element:nth-child(3){
    grid-area: sidebar;
}

.element:nth-child(4){
    grid-area: main;
}
```

<br>

Primero se especifican dos filas con sus columnas correspondientes haciendo uso de `grid-template-areas`, después, con `grid-template-columns` se especifica el tamaño de 2 columnas, sin embargo, hay 3. Por ello, con la propiedad `grid-auto-columns` se define que el tamaño de la tercera columna (aquella cuyo tamaño no ha sido especificado), sea de `1fr`.

Este es el resultado:

![13-grid-auto-columns](https://user-images.githubusercontent.com/110897750/202167846-51abd3d4-446c-4d41-8a6e-021b7e8d1ea1.jpg)

<br>

* **`grid-auto-rows`**

Sigue el mismo principio que `grid-auto-columns`, pero aplicado a las filas.

He aquí un ejemplo:

```css
.container {
    display: grid;
    grid-template-areas:
        "logo header header"
        "sidebar main image"
        "footer footer footer";
    grid-template-rows: 50px 100px;
    grid-auto-rows: 1fr;
}

.element:nth-child(1){
    grid-area: header;
}

.element:nth-child(2){
    grid-area: logo;
}

.element:nth-child(3){
    grid-area: sidebar;
}

.element:nth-child(4){
    grid-area: main;
}

.element:nth-child(5){
    grid-area: image;
}

.element:nth-child(6) {
    grid-area: footer;
}
```

<br>

Con `grid-template-areas` se especifican las columnas y se indica que hay 3 filas, sin embargo, con `grid-template-rows` solo se da la altura de dos de las filas. Por ello, haciendo uso de `grid-auto-rows` se especifica qué tamaño debe tener esa última fila.

Este es el resultado:

![14-grid-auto-rows](https://user-images.githubusercontent.com/110897750/202167848-09668b64-ca4e-484b-935e-34224da33221.jpg)

<sub>[Disposición, Posicionamiento y Overflow](../README.md) | [Volver al índice](#indice) | [Disposiciones](README-display.md)</sub>


<br><hr>


### grid

Esta es la forma abreviada de hacer referencia a casi todas las propiedades vistas en este apartado:

* grid-template-columns
* grid-template-rows
* grid-template-areas
* grid-auto-columns
* grid-auto-rows
* grid-auto-flow

He aquí un ejemplo:

```css
.container {
    display: grid;
    grid:
    "logo header header" 50px
    "sidebar main image" 100px
    "footer footer footer" auto
    / 80px 1fr 2fr;
}

.element:nth-child(1){
    grid-area: header;
}

.element:nth-child(2){
    grid-area: logo;
}

.element:nth-child(3){
    grid-area: sidebar;
}

.element:nth-child(4){
    grid-area: main;
}

.element:nth-child(5){
    grid-area: image;
}

.element:nth-child(6) {
    grid-area: footer;
}
```

<br>

Este es el resultado:

![15-grid](https://user-images.githubusercontent.com/110897750/202167849-5d920a75-46ee-4089-82fa-d60de4c47acc.jpg)

<sub>[Disposición, Posicionamiento y Overflow](../README.md) | [Volver al índice](#indice) | [Disposiciones](README-display.md)</sub>


<br><hr>
<hr><br>


## Espacios entre celdas

Cada vez que se quiera dejar un espacio en blanco entre las filas o las columnas, estas son las propiedades a las que se debe acudir.

El código HTML utilizado se mantiene:

```html
<div class="container">
    <div class="element">Item 1</div>
    <div class="element">Item 2</div>
    <div class="element">Item 3</div>
    <div class="element">Item 4</div>
    <div class="element">Item 5</div>
    <div class="element">Item 6</div>
</div>
```

<br>

Y este es el código CSS base utilizado:

```css
.container {
    display: grid;
    /* cada fila tendrá 3 columnas iguales */
    grid-template-columns: repeat(3, 1fr);
}

.element:nth-child(1){
    background-color: #D66DDC; /* violeta */
}

.element:nth-child(2){
    background-color: #32BBAB; /* azul verdoso */
}

.element:nth-child(3){
    background-color: #09C46A; /* verde */
}

.element:nth-child(4){
    background-color: #E9C46A; /* amarillo */
}

.element:nth-child(5){
    background-color: #F4A261; /* naranja */
}

.element:nth-child(6) {
    background-color: #FF6363; /* rojo */
}
```

<br><hr>

### column-gap

Esta propiedad es la que se ha de utilizar si se desea dejar **espacio vacío entre columnas**.

He aquí un ejemplo:

```css
.container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    column-gap: 10px;
}
```

<br>

Este es el resultado:

![16-column-gap](https://user-images.githubusercontent.com/110897750/202167851-96ce6ebf-6e10-4be6-877c-87eb803268ba.jpg)

<sub>[Disposición, Posicionamiento y Overflow](../README.md) | [Volver al índice](#indice) | [Disposiciones](README-display.md)</sub>


<br><hr>


### row-gap

Esta propiedad es la que se ha de utilizar si se desea dejar **espacio vacío entre filas**.

He aquí un ejemplo:

```css
.container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    row-gap: 10px;
}
```

<br>

Este es el resultado:

![17-row-gap](https://user-images.githubusercontent.com/110897750/202167854-4d97a9d5-685c-4e7a-ae48-a6ee0f9a65ce.jpg)

<sub>[Disposición, Posicionamiento y Overflow](../README.md) | [Volver al índice](#indice) | [Disposiciones](README-display.md)</sub>


<br><hr>


### grid-gap

Esta es la forma abreviada de:

* column-gap
* row-gap

He aquí un ejemplo:

```css
.container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    /* entre filas: 10px
    entre columnas: 2em */
    grid-gap: 10px 2em;
}
```

<br>

Este es el resultado de dicho código:

![18-grid-gap](https://user-images.githubusercontent.com/110897750/202167856-50a12cb9-8fd5-4fb6-a4e3-a7d5327c1e78.jpg)

<sub>[Disposición, Posicionamiento y Overflow](../README.md) | [Volver al índice](#indice) | [Disposiciones](README-display.md)</sub>