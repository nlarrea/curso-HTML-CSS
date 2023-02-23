# Formularios y tablas

Este es el capítulo número 2 del curso. Aquí se hablará de formularios y tablas.

Dentro de los formularios, existen muchísimas opciones posibles, por lo que esta guía puede resultar bastante extensa. Se ha dividido en tres páginas en total, incluyendo esta. Las otras dos páginas están dedicadas a los inputs y puedes acceder a ellas cuando quieras.

El contenido de las tablas no es nada extenso, por lo que su contenido básico se encuentra al final de esta página.

<p id="indice">He aquí un índice de los temas a tratar en esta guía:</p>

* [`FORMULARIOS`](#form)
  * [`<input>`](#input)
  * [`<label>`](#label)
  * [`<select>`](#select)
  * [`<textarea>`](#textarea)
  * [`<button>`](#button)
  * [`<fieldset> y <legend>`](#fieldset-legend)
  * [`<datalist>`](#datalist)
  * [`<output>`](#output)
* [`TABLAS`](#tabla)

<br>

[<< TEMA 1](../01-Etiquetas_y_atributos/README.md#etiquetas-y-atributos) | [INICIO](../../README.md#temario-del-curso---teoria) | [TEMA 3 >>](../03-Imagenes/README.md#contenido-multimedia)


<br><hr>
<hr><br>


<h2 id="form">Formularios</h2>

<sub>* [Ver código](./formularios.html)</sub>

Antes de comenzar, convendría saber qué es un formulario, o qué aspecto suelen tener. Por ello, a continuación se muestra una imagen con el ejempli de uno de ellos:

<img src="https://user-images.githubusercontent.com/110897750/196996079-a7171134-12b5-43ca-ac5f-c42a28187f25.jpg" alt="formulario" width="400">

<br>

Para crear un formulario es necesatio utilizar las etiquetas específicas para ello: como siempre, `<form>` para abrir y `</form>` para cerrar. Todos los elementos contenidos en su interior, formarán el formulario.

Como se puede observar en la imagen situada arriba, para crearlos hacen falta varios elementos, por lo que, existen muchísimos tipos de elementos diferentes que se pueden utilizar para crearlos.

He aquí una lista que contiene todos los elementos disponibles en un formulario:

* [`<input>`](#input)
* [`<label>`](#label)
* [`<select>`](#select)
* [`<textarea>`](#textarea)
* [`<button>`](#button)
* [`<fieldset> y <legend>`](#fieldset-legend)
* [`<datalist>`](#datalist)
* [`<output>`](#output)


<br><hr>


<h3 id="input">< input ></h3>

Este es el elemento más utilizado en los formularios, como siempre, se crean haciendo uso de la etiqueta `<input>` y no requiere de otra etiqueta de cierre adicional. El hecho de que sean tan utilizadas, principalmente se debe a la gran variedad de inputs que se pueden insertar a base de cambiar uno de sus atributos, el atributo `type` concretamente.

He aquí un ejemplo sencillo de un par de elementos de este tipo:

```HTML
<form>
    <input type="text" id="uname" name="username">
    <input type="password" id="pword">
</form>
```

<br>

Como ya se ha mencionado, existen muchísitmos tipos de inputs distintos, todos ellos serán explicados a lo largo de [esta guía](README-inputTypes.md#tipos-de-inputs). Además, también se dispone de [esta otra guía](README-inputAtrib.md#atributos-de-los-inputs) donde se mostrarán cuáles son los atributos más usados. Haz clic en dicho enlace para acceder a la página correspondiente.

<sub>[Volver al índice](#indice) | [Tablas](#tabla)</sub>


<br><hr>


<h3 id="label">< label ></h3>

Este elemento permite definir una etiqueta para otro elemento concreto del formulario.

Es muy útil para aquellas personas que tengan dificultades para marcar un elemento pequeño, como un radio o checkbox, puesto que cuando un `<label>` está haciendo referencia a uno de ellos, al clicar en él, también se selecciona el input.

Para poder *"emparejar"* los `<input>` con los `<label>`, el atributo `for` de la etiqueta debe coincidir con el atributo `id` del campo de entrada.

He aquí un pequeño ejemplo:

```HTML
<form>
    <input type="checkbox" id="box">
    <label for="box">He leído y acepto los Términos y condiciones.</label>
</form>
```

<br>

Este sería su resultado:

![2-label](https://user-images.githubusercontent.com/110897750/196996058-c67ce677-7c27-4e82-820a-17fb7b58003f.jpg)

<br>

Gracias a este código, el usuario puede seleccionar la casilla haciendo clic en el texto que la acompaña en lugar de tener que clicar esplícitamente en la propia casilla.

<sub>[Volver al índice](#indice) | [Tablas](#tabla)</sub>


<br><hr>


<h3 id="select">< select ></h3>

Este elemento permite definir una lista seleccionable.

Se debe utilizar acompañado del elemento `<option>`, el cual sirve para definir cuáles serán las opciones seleccionables. Por defecto, la primera de las opciones será la marcada siempre.

He aquí un ejemplo:

```HTML
<form>
    <label for="sist">Selecciona tu sistema operativo:</label>
    <select id="sist">
        <option value="windows">Windows</option>
        <option value="linux">Linux</option>
        <option value="apple">Apple</option>
    </select>
</form>
```

<br>

Este sería el resultado de dicho código:

![3-select](https://user-images.githubusercontent.com/110897750/196996063-97303d10-2e9d-467c-826b-0fd75df63e49.jpg)

<br>

Como se puede ver, por defecto está seleccionada la primera de las opciones. Sin embargo, esto puede modificarse utilizando el atributo `selected` en aquel elemento que se desee definir como pre-seleccionado.

Este elemento también permite atributos como `size` y `multiple`. Ambos están explicados en [esta guía](README-inputAtrib.md).

<sub>[Volver al índice](#indice) | [Tablas](#tabla)</sub>


<br><hr>


<h3 id="textarea">< textarea ></h3>

Este elemento define un input multilínea.

Tiene atributos como `rows` y `cols` que permiten definir el tamaño del input. El tamaño también puede ser definido haciendo uso de estilos mediante CSS, con los atributos `width` y `height`.

He aquí un ejemplo:

```HTML
<form>
    <textarea name="mensaje" id="msg" cols="30" rows="10">Este es un mensaje dentro del textarea.</textarea>
</form>
```

<br>

Este sería el resultado del código:

![4-textarea](https://user-images.githubusercontent.com/110897750/196996068-c7a14b3b-ba00-48db-8b41-45d844825b33.jpg)

<br>

<sub>[Volver al índice](#indice) | [Tablas](#tabla)</sub>


<br><hr>


<h3 id="button">< button ></h3>

Los botones se definen utilizando la etiqueta `<button>` de apertura, seguida de su etiqueta de cierre `</button>`. Si se introduce un texto en el espacio situado entre ambas etiquetas, dicho texto estará contenido en el botón.

Se recomienda especificar siempre el tipo del botón mediante el atributo `type`. Además, se pueden añadir acciones al pulsarlo haciendo uso del atributo `onclick`.

Aquí te dejo un ejemplo sencillo:

```HTML
<form>
    <button type="button" onclick="alert('Hello World!')">¡Te mando un saludo!</button>
</form>
```

<br>

¡Te invito a copiar el código mostrado y ejecutarlo por tu cuenta!

He aquí el resultado del botón:

![5-button](https://user-images.githubusercontent.com/110897750/196996069-1646c76a-d41d-49ac-8fdc-fa191ca06e5f.jpg)

<br>

<sub>[Volver al índice](#indice) | [Tablas](#tabla)</sub>


<br><hr>


<h3 id="fieldset-legend">< fieldset > y < legend ></h3>

El elemento `<fieldset>` se utiliza para crear un grupo de elementos en los formularios. Va acompañado del elemento `<legend>`, el cual define una descripción para dicho grupo.

He aquí un breve ejemplo:

```HTML
<form>
    <fieldset>
        <legend>Datos personales:</legend>
        <label for="nombre">Nombre:</label>
        <input type="text" id="nombre" placeholder="Tu nombre"><br>
        <label for="apellido">Apellido:</label>
        <input type="text" id="apellido" placeholder="Tu apellido">
    </fieldset>
</form>
```

<br>

Este es el resultado del código mostrado:

![6-fieldset-legend](https://user-images.githubusercontent.com/110897750/196996070-16c81779-68f9-4e1f-a797-5b40acbe97d6.jpg)

<br>

<sub>[Volver al índice](#indice) | [Tablas](#tabla)</sub>


<br><hr>


<h3 id="datalist">< datalist ></h3>

Este tipo de elemento sirve para definir una lista de opciones predefinidas para un `<input>`. El usuario verá una lista desplegable con dichas opciones, las cuales también irán apareciendo a medida que se escribe un dato.

El atributo `list` del elemento `<input>` debe coincidir con el atributo `id` del elemento `<datalist>`.

Este es un ejemplo sencillo:

```HTML
<form>
    <input type="text" list="browsers">
    <datalist id="browsers">
        <option value="Internet Explorer"></option>
        <option value="Firefox"></option>
        <option value="Chrome"></option>
        <option value="Opera"></option>
    </datalist>
</form>
```

<br>

Este sería el resultado de dicho código:

![7-datalist](https://user-images.githubusercontent.com/110897750/196996072-05bf1c7f-ea21-4580-95a4-2425b6b1eddb.jpg)

<br>

<sub>[Volver al índice](#indice) | [Tablas](#tabla)</sub>


<br><hr>


<h3 id="output">< output ></h3>

Este elemento permite representar cálculos que hayan sido obtenidos mediante script.

He aquí un ejemplo:

```HTML
<form oninput="x.value = parseInt(a.value) + parseInt(b.value)">
    <label for="a">Valor de a:</label>
    <input type="number" id="a">
    <label for="b">Valor de b:</label>
    <input type="number" id="b"><br>
    <label for="out">Respuesta: a + b = </label>
    <output name="x" for="a b" id="out"></output>
</form>
```

<br>

Este sería el resultado del código:

![8-output](https://user-images.githubusercontent.com/110897750/196996076-5f7e4d53-6734-47f5-98eb-ee364c85d075.jpg)

<br>

<sub>[Volver al índice](#indice) | [Tablas](#tabla)</sub>


<br><hr>
<hr><br>


<h2 id="tabla">Tablas</h2>

<sub>* [Ver código](./tablas.html)</sub>

Las tablas en HTML se definen usando las etiquetas `<table>` y `</table>`. Dentro de éstas, habrá que ir definiendo los siguientes elementos de la tabla, siempre teniendo en cuenta que se crean utilizando etiquetas para definir el contenido de las filas. Para crear una nueva fila, se deben usar `<tr>` y `</tr>`.

A la hora de añadir datos, se dispone de las siguientes dos opciones:

* Añadir encabezados: se crean usando `<th>` y `</th`, siempre teniendo en cuenta que por defecto el texto aparecerá centrado y en negrita.
* Añadir datos: se crean usando `<td>` y `</td>`.

He aquí un ejemplo:

```HTML
<table>
    <tr>
        <th>Nombre</th>
        <th>Apellido</th>
        <th>Edad</th>
    </tr>
    <tr>
        <td>John</td>
        <td>Smith</td>
        <td>34</td>
    </tr>
    <tr>
        <td>Tom</td>
        <td>Grant</td>
        <td>28</td>
    </tr>
</table>
```

<br>

Este sería el resultado:

![tabla](https://user-images.githubusercontent.com/110897750/196996081-860198d3-3cab-42e5-8cac-b7f69c057889.jpg)

<br>

<sub>[Volver al índice](#indice)</sub>

<br>

[<< TEMA 1](../01-Etiquetas_y_atributos/README.md#etiquetas-y-atributos) | [INICIO](../../README.md#temario-del-curso---teoria) | [TEMA 3 >>](../03-Imagenes/README.md#contenido-multimedia)


<br><hr>
<hr><br>


# Créditos

La información de esta página ha sido obtenida a través de realizar diferentes cursos por mi cuenta. Sin embargo, el índice y los datos utilizados aquí han sido traducidos de [w3schools](https://www.w3schools.com/html/html_form_elements.asp).
