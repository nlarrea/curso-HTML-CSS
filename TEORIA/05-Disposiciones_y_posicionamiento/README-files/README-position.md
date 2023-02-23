# POSICIONAMIENTO

En esta parte de la guía se va a hablar de cómo posicionar los elementos en nuestra página web.

<p id="indice">He aquí un pequeño índice donde se muestra el temario a tratar:</p>

* [Coordenadas](#coordenadas)
  * [top](#top)
  * [right](#right)
  * [bottom](#bottom)
  * [left](#left)
  * [z-index](#z-index)
* [position](#position)
  * [static](#static)
  * [relative](#relative)
  * [absolute](#absolute)
  * [fixed](#fixed)
  * [sticky](#sticky)

<br>

[Disposición, Posicionamiento y Overflow](../README.md#disposición-posicionamiento-y-overflow)


<br><hr><br>


## Coordenadas

Una forma básica de posicionar los elementos en la web es utilizar la idea de las coordenadas, con la ayuda de las siguientes propiedades:

* top
* right
* bottom
* left
* z-index

<br>

Éstas son básicas y necesarias para los apartados que se verán en [position](#position).

El valor *por defecto* de cada una de ellas, es `auto`, lo que consigue que el elemento en cuestión se mantenga en una determinada posición.

Este es el código HTML que se va a utilizar a lo largo de este apartado:

```html
<div class="container">
    <div class="element">Pos. final</div>
</div>
```


<br><hr>


### top

* **OPCIÓN 1 (position: relative)**

Si se indica que el valor de la propiedad `position` es *relative*, al utilizar `top`, el elemento se moverá hacia abajo desde la posición en la que se encontraba.

He aquí un ejemplo:

```css
/* código al piincipio */
.element {
    position: relative;
    top: 0;
}
```

<br>

En la imagen se puede apreciar cómo el elemento ha sido desplazado respecto a su posición original `30px` hacia abajo.

Este es el resultado:

![1-top_relative](https://user-images.githubusercontent.com/110897750/202438653-b249a156-c3aa-472f-98fc-ccf4217528e6.jpg)

<br>

* **OPCIÓN 2 (position: absolute)**

Si se utiliza el valor *absolute* para la propiedad `position` dentro del elemento con propiedad `top`, éste se posicionara con respecto al elemento en el que se encuentra.

He aquí un ejemplo:

```css
.container {
    position: relative;
}

.element {
    position: absolute;
    top: 0;
}
```

<br>

Al indicar `top: 0;` se envía el elemento *"hijo"* a la parte de arriba del todo del elemento *"padre"*, a la posición 0.

**Recordar que la coordenada (0, 0) se encuentra en la parte superior izquierda de los elementos.**

![2-top_absolute](https://user-images.githubusercontent.com/110897750/202427082-e094514d-edcd-4a25-a78a-96942c08c66a.jpg)

<sub>[Disposición, Posicionamiento y Overflow](../README.md#disposición-posicionamiento-y-overflow) | [Volver al índice](#indice)</sub>


<br><hr>


### right

* **OPCIÓN 1 (position: relative)**

Si la propiedad `position` del elemento *"hijo"* tiene el valor *relative*, el elemento se movera hacia la izquierda de la posición en la que debería encontrarse.

He aquí un ejemplo:

```css
.element {
    position: relative;
    right: 30px;
}
```

<br>

Este es el resultado:

![3-right_relative](https://user-images.githubusercontent.com/110897750/202427088-cee3b72b-1ffd-41be-bf80-9b6235dfcb64.jpg)

<br>

* **OPCIÓN 2 (position: absolute)**

Si la propiedad `position` del elemento *"hijo"* tiene el valor *absolute*, el elemento se movera hacia la izquierda desde el borde derecho del elemento padre.

Si se le dan valores negativos a la propiedad `right`, entonces se movería en dirección contraria.

Este es el código de ejemplo:

```css
.container {
    position: relative;
}

.element {
    position: absolute;
    right: 30px;
}
```

Este es el resultado del código mostrado:

![4-right_absolute](https://user-images.githubusercontent.com/110897750/202427090-b7bdc0bd-2c8a-4e0a-949e-dc0a64603df7.jpg)

<sub>[Disposición, Posicionamiento y Overflow](../README.md#disposición-posicionamiento-y-overflow) | [Volver al índice](#indice)</sub>


<br><hr>


### bottom

* **OPCIÓN 1 (position: relative)**

Hace el efecto contrario a `top`: se moverá hacia arriba la cantidad de espacio indicada.

```css
.element {
    position: relative;
    bottom: 20px;
}
```

<br>

Este es el resultado del código:

![5-bottom_relative](https://user-images.githubusercontent.com/110897750/202427095-45111e31-9df5-4af7-8b5d-8a4b10509d25.jpg)

<br>

* **OPCIÓN 2 (position: absolute)**

El elemento se moverá a la parte de abajo del elemento *"padre"*.

He aquí un ejemplo:

```css
.container {
    position: relative;
}

.element {
    position: absolute;
    bottom: 40px;
}
```

<br>

Este sería el resultado:

![6-bottom_absolute](https://user-images.githubusercontent.com/110897750/202427097-63d6b5a7-c721-4ca0-9a40-19701770cfc8.jpg)

<sub>[Disposición, Posicionamiento y Overflow](../README.md#disposición-posicionamiento-y-overflow) | [Volver al índice](#indice)</sub>


<br><hr>


### left

* **OPCIÓN 1 (position: relative)**

Hace el efecto contrario a la porpiedad `right`. Moverá a la derecha los elementos en la cantidad de espacio indicada.

He aquí un ejemplo:

```css
.element {
    position: relative;
    left: 60px;
}
```

<br>

Este es el resultado:

![7-left_relative](https://user-images.githubusercontent.com/110897750/202427099-9ede5bc5-b1c7-47d8-87fe-e384ca07ca49.jpg)

<br>

* **OPCIÓN 2 (position: absolute)**

Se moverá al borde izquierdo del elemento padre, desplazándose la cantidad de espacio que se indique desde la misma.

He aquí un ejemplo:

```css
.container {
    position: relative;
}

.element {
    position: absolute;
    left: 0px;
}
```

<br>

Este sería el resultado:

![8-left_absolute](https://user-images.githubusercontent.com/110897750/202427104-a3a9966b-50f7-46b4-96ce-b043c98d5270.jpg)

<sub>[Disposición, Posicionamiento y Overflow](../README.md#disposición-posicionamiento-y-overflow) | [Volver al índice](#indice)</sub>


<br><hr>


### z-index

Esta propiedad permite ordenar los elementos en el eje Z, es decir, nos permite indicar qué elemento queremos que esté por encima del otro sin tener en cuenta cuál fue colocado primero en el código HTML.

Su valor *por defecto* es `auto`.

Suponiendo que se tiene este código HTML:

```html
<div class="container">
    <div class="element">Uno</div>
    <div class="element">Dos</div>
    <div class="element">Tres</div>
    <div class="element">Cuatro</div>
</div>
```

<br>

Con este código CSS:

```css
.container {
    position: relative;
}

.element:nth-child(1){
    position: absolute;
    top: 0;
    left: 0;
}

.element:nth-child(2) {
    position: absolute;
    right: 0;
    bottom: 0;
}

.element:nth-child(3){
    position: absolute;
    top: 50px;
    left: 100px;
}

.element:nth-child(4){
    width: 200px;
    height: 150px;
    position: absolute;
    right: 50px;
    bottom: 20px;
}
```

<br>

Con este código, tal y como está, este es el resultado:

![9-z-index](https://user-images.githubusercontent.com/110897750/202427106-50dd22a5-83d8-4ce3-9e67-a1d10f262af2.jpg)

<br>

Como se puede observar, el elemento número 4 no permite que se vean bien los demás elementos. Esto puede solucionarse utilizando el `z-index`, donde se pueden asignar **valores negativos y positivos**. Aquel que tenga el valor más alto será el que más arriba se coloque.

He aquí un ejemplo simple sobre cómo solucionar el código anterior (mandar el elemento 4 al fondo):

```css
.container {
    position: relative;
    z-index: -2;
}

.element:nth-child(4){
    width: 200px;
    height: 150px;
    position: absolute;
    right: 50px;
    bottom: 20px;
    z-index: -1;
}
```

<br>

Este sería el resultado:

![10-z-index-solucion](https://user-images.githubusercontent.com/110897750/202427111-d0dc8aa9-ed90-43be-9ea3-23084029f6ed.jpg)

<sub>[Disposición, Posicionamiento y Overflow](../README.md#disposición-posicionamiento-y-overflow) | [Volver al índice](#indice)</sub>


<br><hr>
<hr><br>


## position

Para poder posicionar los elementos, es necesario todo lo que se ha visto hasta ahora. Sin embargo, habrá ocasiones en las que se desee que se posicionen respecto a algun elemento concreto o que tengan otro tipo de habilidades.

Para ello, existe la propiedad `position`, la cual tiene los siguientes valores disponibles:

* static *(por defecto)*
* relative
* absolute
* fixed
* sticky

<br><hr>

### static

Este es el valor por defecto.

Aquellos elementos que tengan este valor en la propiedad `position` se situarán en el orden o posicion por defecto, siguiendo el criterio de los elementos HTML.

Además, no se verá afectado por ninguna de las propiedades vistas en [Coordenadas](#coordenadas):

* top
* right
* bottom
* left
* z-index

<br>

He aquí un ejemplo sencillo:

```css
.container {
    position: relative;
}

.element {
    background-color: #D66DDC;
    position: static;
    bottom: 0; /* no va a hacer caso a esto */
}
```

<br>

Este sería el resultado:

![11-position_static](https://user-images.githubusercontent.com/110897750/202427114-4801ee78-64e0-4c8f-8921-11beb2b1123c.jpg)

<sub>[Disposición, Posicionamiento y Overflow](../README.md#disposición-posicionamiento-y-overflow) | [Volver al índice](#indice)</sub>


<br><hr>


### relative

Al igual que el valor `static`, se posiciona siguiendo el criterio del código HTML. Sin embargo, este tipo de posicionamiento sí permite utilizar las siguientes propiedades:

* top
* right
* bottom
* left
* z-index

<br>

He aquí un ejemplo:

```css
.container {
    position: relative;
}

.element {
    background-color: #D66DDC;
    position: relative;
    top: 150px;
    right: -100px;
}
```

<br>

Este sería el resultado:

![12-position_relative](https://user-images.githubusercontent.com/110897750/202427119-ffac7414-bba9-4a50-bce6-2611b629489f.jpg)

<sub>[Disposición, Posicionamiento y Overflow](../README.md#disposición-posicionamiento-y-overflow) | [Volver al índice](#indice)</sub>


<br><hr>


### absolute

Esta vez, el elemento no se posicionará siguiendo el criterio del HTML. Éste se moverá de acuerdo al *"padre"* más cercano posible, aquel que tenga *relative* como valor en `position`.

También se verá desplazado utilizando los siguientes:

* top
* right
* bottom
* left
* z-index

<br>

He aquí un ejemplo:

```css
.container {
    position: relative;
}

.element {
    position: absolute;
    bottom: 0;
    right: 150px;
}
```

<br>

Este sería el resultado del código:

![13-position_absolute](https://user-images.githubusercontent.com/110897750/202427121-7f9570de-be83-4976-b9ed-4a4e1a637a9c.jpg)

<sub>[Disposición, Posicionamiento y Overflow](../README.md#disposición-posicionamiento-y-overflow) | [Volver al índice](#indice)</sub>


<br><hr>


### fixed

Al igual que lo ocurrido con el valor `absolute`, utilizando este valor para la propiedad `position` el elemento no se posiciona siguiendo el criterio establecido en el archivo HTML. Sin embargo, se posiciona **respecto a la pantalla**, y permanece en esa posición fija aunque se navegue en cualquier dirección dentro de dicha página.

He aquí un ejemplo:

```css
.element {
	position: fixed;
	top: 0;
}
```

<br>

Con este código se consigue que el elemento deseado se posicione en la parte superior de la ventana y permanezca en dicha posición a pesar de que se haga *scroll* en cualquier dirección.

Aquí se muestra la posición del `div` que contiene un *About Us* en una posición:

<img src="https://user-images.githubusercontent.com/110897750/202427123-9d91d0bb-7057-4fa0-a71d-3143d5751c02.jpg" alt="14-position_fixed" width="80%"/>

<br>

Y después de hacer *scroll* dicho `div` se mantiene en el mismo lugar:

<img src="https://user-images.githubusercontent.com/110897750/202427132-d87a108b-fc4c-4b0e-ad8c-60b135ffbd2e.jpg" alt="15-position_fixed_2" width="80%"/>

<sub>[Disposición, Posicionamiento y Overflow](../README.md#disposición-posicionamiento-y-overflow) | [Volver al índice](#indice)</sub>


<br><hr>


### sticky

Esta propiedad actúa como una mezcla de static y fixed. En primer lugar, el elemento se mantendrá en una posición establecida, sin embargo, al hacer scroll, se mantendrá en la posición indicada (como si fuera `fixed`).

He aquí un ejemplo:

```css
.element {
	position: sticky;
	top: 0;
}
```

<br>

En un principio, el texto *"HTML Styled Fried"* permanece en una posición. Cuando se hace *scroll* y dicho elemento debería *salir* de la pantalla, éste se quedará en la posición `top: 0`.

Imagen inicial:

<img src="https://user-images.githubusercontent.com/110897750/202427138-fcb0b7b2-4783-45e6-8bef-924ed37b4b4f.jpg" alt="16-position_fixed" width="80%"/>

<br>

Imagen final:

<img src="https://user-images.githubusercontent.com/110897750/202427149-e98e25b6-b9f1-4d6d-8b0c-a4c93399e861.jpg" alt="17-position_fixed_2" width="80%"/>

<sub>[Disposición, Posicionamiento y Overflow](../README.md#disposición-posicionamiento-y-overflow) | [Volver al índice](#indice)</sub>