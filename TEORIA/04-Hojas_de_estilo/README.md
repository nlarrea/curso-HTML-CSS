# Introducción a CSS

En este tema se hablará de las hojas de estilo, las cuales nos permiten modificar el estilo del contenido de la página web, o incluso añadir o eliminar (u ocultar) contenido de la misma.

<p id="indice">Para crear hojas de estilo se utiliza el lenguaje CSS. He aquí un pequeño índice sobre los temas a tratar en esta guía:</p>

* [AÑADIR ESTILOS AL DOCUMENTO HTML](#addStyle)
* [PROPIEDADES BÁSICAS](#properties)
  * [Ancho (width) y alto (height)](#width-height)
  * [Bordes](#border)
  * [Margen](#margin)
  * [Padding](#padding)
  * [Background](#background)
  * [Textos](#texts)

<br>

<sub>* [Ver código](./)</sub>

[<< TEMA 3](../03-Imagenes/README.md#contenido-multimedia) | [INICIO](../../README.md#temario-del-curso---teoria) | [TEMA 5 >>](../05-Disposiciones_y_posicionamiento/README.md#disposición-posicionamiento-y-overflow)


<br><hr>
<hr><br>

<h2 id="addStyle">CÓMO AÑADIR ESTILOS AL DOCUMENTO HTML</h2>

Como ya se ha mencionado en el tema anterior, existen varias formas distintas de añadir estilos al documento:

1. **Insertar estilos directamente en el elemento HTML:**

He aquí un pequeño ejemplo:

```HTML
<h1 style="color: goldenrod;">Este es un título de prueba</h1>
```

<br>

2. **Insertar código de estilo en el documento HTML con `<style>`:**

He aquí un ejemplo:

```HTML
<head>
    <!-- aquí habría otros elementos meta, title, etc. -->
    <style>
        h1 {
            color: goldenrod;
        }
    </style>
</head>
<body>
    <h1>Este es un título de prueba</h1>
</body>
```

<br>

3. **Insertar hojas de forma externa:**

Esta es la que más vamos a ver y utilizar sin lugar a dudas a lo largo de este curso. Para implementar este método se deben usar las etiquetas `<link>`, donde se deben especificar tanto la **relación** entre la hoja que se va a *importar* y el documento HTML, como la dirección de referencia a dicha hoja, la cual puede ser local (un documento CSS que hayamos creado nosotros) o una página de internet como puede ser *Bootstrap*.

En este bloque se muestra el código HTML:

```HTML
<head>
    <!-- aquí habría otros elementos meta, title, etc. -->
    <link rel="stylesheet" href="prueba.css">
</head>
<body>
    <h1>Este es un título de prueba</h1>
</body>
```

Y a continuación, se muestra el código del archivo CSS:

```CSS
h1 {
    color: goldenrod;
}
```

<br>

**En los 3 ejemplos se obtiene el mismo resultado**, donde se consigue cambiar el color del encabezado:

![1-addStyles](https://user-images.githubusercontent.com/110897750/197635041-05bcfe12-f395-49fa-b0a9-20c86fb1c801.jpg)

<br>

Si se utilizaran los tres ejemplos mostrados a la vez, cada uno con un color, el color mostrado sería el del ejemplo 1, puesto que es el que más especificidad tiene. Si ese no estuviera, se mostraría el del caso 2, y así sucesivamente.

<sub>[Volver al índice](#indice)</sub>


<br><hr>
<hr><br>


<h2 id="properties">PROPIEDADES BÁSICAS</h2>

Aquí se van a mostrar algunas de las propiedades más básicas de CSS. Para aprender más cosas acerca de CSS (*selectores, displays, etc.*) deberás seguir avanzando en el temario.


<br><hr>


<h3 id="width-height">Ancho (width) y alto (height)</h3>

Estos dos casos ya han sido vistos en el tema anterior. Como ya sabrás, se pueden definir la altura y la anchura de los elementos haciendo uso de CSS.

He aquí un ejemplo sobre cómo definir el tamaño de una imagen introducida en HTML:

```CSS
img {
    width: 500px;
    height: 100%;
}
```

<br>

Este sería el resultado:

![2-width-height](https://user-images.githubusercontent.com/110897750/197635047-49bfdd3c-ce6e-4b8b-9467-64b31473682a.jpg)

<sub>[Volver al índice](#indice)</sub>


<br><hr>


<h3 id="border">Bordes</h3>

1. **`border-style`**

Pueden añadirse bordes de diferentes estilos a cualquier elemento del HTML con `border-style`. He aquí una lista de los estilos permitidos:

* `dotted`: crea un borde hecho con puntos.
* `dashed`: crea un borde hecho con rayas pequeñas (-)
* `solid`: es **de los más usados**, crea un borde sólido.
* `double`: crea un borde con dos líneas sólidas.
* `groove`: crea un borde como si fuera una especie de surco.
* `ridge`: crea un borde con un efecto hacia afuera.
* `inset`: da un estilo de *sombreado* arriba y a la izquierda.
* `outset`: da un estilo de *sombreado* abajo y a la derecha.
* `none`: quita el borde, es un valor también **muy utilizado**.
* `hidden`: oculta el borde.
* **Añadir hasta 4:** si se añaden 4 de estos estilos, el primero afectara al superior, el segundo al derecho, el tercero al inferior y el cuarto al izquierdo. Consiguiendo así un elemento con 4 estilos de borde distintos.

<br>

2. **`border-width`**

Puede escogerse el ancho del borde con la propiedad `border-width`, donde se le puede dar un valor tanto en pixels como en otros ya definidos (*thick*, *medium*, etc.).

Se le puede dar más de un valor a la propiedad, indicando así a cuál de los bordes queremos que se le aplique el estilo.

<br>

3. **`border-color`**

Esta propiedad permite seleccionar el color del borde. Se pueden especificar colores de la siguiente forma:

* **Por nombre:** CSS cuenta con varios colores ya predefinidos, solo hay que escribir el nombre de uno de esos colores para que aparezca.

```CSS
h1 {
    border-style: solid;
    border-width: 2px;
    border-color: red;
}
```

<br>

* **De forma hexadecimal:** para añadir colores de forma hexadecimal es necesario escribir el color precedido por `#`.

```CSS
h1 {
    border-style: solid;
    border-width: 2px;
    border-color: #cea135;
}
```

<br>

* **Colores RGB:** se especifican escribiendo `rgb()` con los colores dentro separados por comas.

```CSS
h1 {
    border-style: solid;
    border-width: 2px;
    border-color: rgb(255, 192, 199);
}
```

<br>

* **Colores RGBA:** son iguales que los colores **RGB pero añadiendo** un parámetro más entre paréntesis: la **opacidad**.

```CSS
h1 {
    border-style: solid;
    border-width: 2px;
    border-color: rgba(255, 192, 199, 0.5);
}
```

<br>

4. **Escribirlo en una única línea**

Todo lo visto en este punto puede ser escrito en una sola línea de código haciendo uso de `border` de la siguiente manera:

```CSS
h1 {
    border: 2px solid #cea135;
}
```

<br>

5. **Escoger el lado del borde**

En ocasiones conviene que solo sea aplicado el estilo en uno de los lados del elemento. Por ello, se puede hacer uso de las siguietnes propiedades:

* `border-top`
* `border-right`
* `border-bottom`
* `border-left`

<br>

Aquí se muestra un ejemplo de un texto rodeado con un borde al que se le ha cambiado el color y definido su estilo:

![3-border](https://user-images.githubusercontent.com/110897750/197635050-82d0be71-dd8e-4e54-b6b3-c027f4e1f768.jpg)

<sub>[Volver al índice](#indice)</sub>


<br><hr>


<h3 id="margin">Margen</h3>

Los márgenes se utilizan para **añadir el espacio** deseado en la parte de fuera de cada elemento, por **fuera de los bordes**.

Al igual que se ha visto en el apartado anterior, se puede especificar qué margen se quiere modificar haciendo uso de:

* `margin-top`
* `margin-right`
* `margin-bottom`
* `margin-left`

<br>

Se puede utilizar también `margin` sin especificar el lado y añadir hasta 4 valores dentro del mismo:

* `margin: 10px`: añade 10px de espacio al rededor de cada uno de los cuatro lados del elemento.
* `margin: 10px 20px`: añade 10px de espacio arriba y abajo, y 20px a izquierda y derecha.
* `margin: 10px 20px 30px`: añade 10px arriba, 20px a la izquierda y derecha, y 30px abajo.
* `margin: 10px 20px 30px 40px`: añade 10px arriba, 20px a la derecha, 30px abajo y 40px a la izquierda.

<sub>[Volver al índice](#indice)</sub>


<br><hr>


<h3 id="padding">Padding</h3>

El padding se utiliza para **añadir el espacio** deseado en la parte de dentro de cada elemento, por **dentro de los bordes**.

Lo ya visto en el punto anterior de márgenes es aplicable aquí también, pero haciendo uso de `padding` en lugar de `margin`.

<sub>[Volver al índice](#indice)</sub>


<br><hr>


<h3 id="background">Background</h3>

Se pueden aplicar muchísimos estilos a los fondos de los elementos o de la página en general.

En este punto vamos a desplegar todos sus valores posibles en diferentes propiedades para que se vean de forma más clara, pero al igual que con los bordes, se puede utilizar una propiedad única que recoge todas las que vamos a ver, llamada `background`.

<br>

1. **`background-color`**

Con esta propiedad se puede definir un color de fondo para cualquier elemento de la siguiente manera:

```CSS
h1 {
    width: 590px; /* para definir un tamaño */
    background-color: lightcoral;
}
```

<br>

Este sería el resultado:

![1-color](https://user-images.githubusercontent.com/110897750/197635291-927e63c7-5b5f-4a7a-8ee0-63ab0fb0856a.jpg)

<br>

Se le puede añadir la propiedad `opacity` para que el color de fondo tenga menos opacidad.

<br>

2. **`background-image`**

Esta propiedad permite añadir una imagen cualquierda como fondo de un elemento. Para poder añadirla, se debe hacer uso de `url()`, donde, entre paréntesis, se escribirá la dirección de la imagen en cuestión:

```CSS
h1 {
    width: 600px; /* para añadirle una anchura */
    height: 200px; /* para añadirle una altura */
    background-image: url("../img/fondo.jpg");
    background-position: center center;
}
```

<br>

Este sería el resultado:

![2-image](https://user-images.githubusercontent.com/110897750/197635293-07265ce4-8edc-47df-a468-20987dc71d13.jpg)

<br>

Se puede utilizar la propiedad `background-position` para especificar qué parte de la imagen se desea ver, indicando el eje X y el Y.

<br>

3. **`background-repeat`**

Se utiliza cuando se está usando una imagen de fondo. La imagen se repetirá para ocupar el espacio indicado. Se puede utilizar la propiedad `background-repeat` para definir cómo debe (o no) repetirse dicha imagen.

Estos son sus valores posibles:

* `repeat-x`: para permitir que sólo se repita en el eje x.
* `repeat-y`: para sólo permitir que se repita en el eje y.
* `no-repeat`: para evitar que se repita.

<br>

Por defecto, la imagen podrá repetirse en ambos ejes. He aquí un ejemplo:

```CSS
h1 {
    color: red;
    background-image: url("../github.png");
    background-repeat: repeat-x;
}
```

<br>

Este sería el resultado:

![3-repeat](https://user-images.githubusercontent.com/110897750/197635298-9f32732f-08dd-462c-8d94-90dd78db8bdc.jpg)

<br>

4. **`background-attachment`**

Permite a la imagen desplazarse con el resto de la página al hacer scroll, o quedarse quieta mientras el resto se mueve.

Estos son los dos valores posibles:

* `scroll`: permite a la imagen moverse con el contenido de la página.
* `fixed`: la imagen de fondo se queda fija. Hace parecer que el contenido se desliza encima de ella.

<br>

He aquí un ejemplo:

```CSS
.container {
    background-image: url("../img/fondo.jpg");
    background-attachment: fixed;
}
```

<br>

Este sería el resultado:

![4-attachment](https://user-images.githubusercontent.com/110897750/197635300-bdaf9fbe-8de8-436a-aa62-1ef22e7e25b9.jpg)

<sub>[Volver al índice](#indice)</sub>


<br><hr>


<h3 id="texts">Textos</h3>

Los textos tienen muchísimas opciones posibles. En este apartado se va a hablar únicamente de alguna de las más usadas.

<br>

1. **Cambiar el color del texto**

Para cambiar el color de cualquier texto, basta con usar la propiedad `color`. De la misma forma que la ya vista en los [bordes](#border), el color puede definirse por **nombre**, **de forma hexadecirmal**, como **RGB**, o como **RGBA**.

He aquí un ejemplo simple:

```CSS
p {
    color: red;
}
```

<br>

Este sería el resultado de dicho código:

![1-color](https://user-images.githubusercontent.com/110897750/197635523-553f14e1-863d-4825-9a43-1e5f6b01ed02.jpg)

<br>

2. **Alinear el texto**

Se puede alinear el texto de múltiples maneras y con varias opciones distintas. Las más comunes son las siguientes:

* `text-align`: para alinear el texto horizontalmente. Sus valores pueden ser:
  * `center`: se alinean los centros.
  * `left`: todo el texto se alinea a la izquierda.
  * `right`: se alinea a la derecha.
  * `justify`: crea una justificación a ambos lados.
* `vertical-align`: para alinear el texto de forma vertical. Tiene varios valores posibles, estos son algunos:
  * `top`:
  * `middle`
  * `bottom`

<br>

He aquí un ejemplo simple:

```CSS
button {
    vertical-align: bottom;
}
```

<br>

Este sería el resultado:

![2-align](https://user-images.githubusercontent.com/110897750/197635525-59469a7a-f4b4-46ce-a3e2-5dded8329f16.jpg)

<br>

En este caso, se han utilizado botones como ejemplo para que se aprecie más el resultado.

<br>

3. **Decorar el texto**

Existen muchísimas posibilidades para poder decorar el texto. Para ello se usa la propiedad `text-decoration`, la cual es la versión corta de las siguientes opciones:

* `text-decoration-line`: permite añadir una línea al texto (*un subrayado, por ejemplo*).
* `text-decoration-color`: permite modificar el color de dicha línea.
* `text-decoration-style`: permite indicar qué tipo de línea va a ser.
* `text-decoration-thickness`: permite modificar el grosor de la línea.

<br>

He aquí un ejemplo:

```CSS
p {
    text-decoration: underline red solid 2px;
}
```

<br>

Este sería el resultado:

![3-decoration](https://user-images.githubusercontent.com/110897750/197635527-9ebefdaa-4b8f-43ea-8250-338157722923.jpg)

<br>

4. **Transformar el texto**

Como ya indica el título, existe una forma de transformar el texto, su formato en este caso, haciendo uso de `text-transform`. Aquí se muestran las opciones posibles:

* `uppercase`: hace que todas las letras se vean en mayúscula.
* `lowercase`: hace que todas las letras se vean en minúscula.
* `capitalize`: hace que la primera letra de cada palabra se vea mayúscula.

<br>

Este sería un ejemplo sencillo:

```CSS
p {
    text-transform: capitalize;
}
```

<br>

Y este su resultado:

![4-transform](https://user-images.githubusercontent.com/110897750/197635528-0a942d45-7890-4931-b56c-8c838b0a72f1.jpg)

<br>

5. **Espaciado del texto**

Existen muchas propiedades para dar espacio al texto, he aquí un resumen de las mismas:

* `text-indent`: esta propiedad permite desplazar o indentar la primera línea del texto.
* `letter-spacing`: esta propiedad permite aumentar o disminuir el espacio entre los caracteres del texto.
* `line-height`: esta propiedad permite aumentear o disminuir el espacio entre las líneas de un texto.
* `word-spacing`: esta propiedad permite aumentar o disminuir el espacio entre las palabras de un texto.
* `white-space`: esta propiedad permite que un texto se mantenga en una sola línea o se divida en varias al no caber en su *contenedor* o la pantalla.

<sub>[Volver al índice](#indice)</sub>

<hr><br>
<br><hr>

[<< TEMA 3](../03-Imagenes/README.md#contenido-multimedia) | [INICIO](../../README.md#temario-del-curso---teoria) | [TEMA 5 >>](../05-Disposiciones_y_posicionamiento/README.md#disposición-posicionamiento-y-overflow)


