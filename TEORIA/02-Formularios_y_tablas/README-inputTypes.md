# TIPOS DE INPUTS

En esta guía se mostrarán los tipos distintos de inputs, mostrando un ejemplo básico por cada uno de los elementos.

Puede parecer una guía repetitiva, por ello, está planteada más como guía puntual para acceder de forma rápida a un ejemplo donde ver la sintaxis y las posibilidades de cada input.

<p id="indice">A continuación, se muestra el índice a seguir:</p>

* [text](#text)
* [password](#password)
* [submit](#submit)
* [reset](#reset)
* [radio](#radio)
* [checkbox](#checkbox)
* [button](#button)
* [email](#email)
* [tel](#tel)
* [file](#file)
* [number](#number)
* [date](#date)
* [time](#time)
* [datetime-local](#datetime-local)
* [month](#month)
* [week](#week)
* [url](#url)
* [color](#color)
* [image](#image)
* [range](#range)
* [search](#search)

<br>

[<< FORMULARIOS Y TABLAS](./README.md#formularios-y-tablas) | [ATRIBUTOS >>](./README-inputAtrib.md#atributos-de-los-inputs)


<br><hr>


<h2 id="text">type= "text"</h2> <!--******************** type= "text" ********************-->

Con este atributo se indica que el tipo de input es de tipo texto. Es uno de los más utilizados de todos los diponibles. Es muy común utilizarlo acompañado también por el atributo `placeholder`, el cual permite mantener un texto concreto dentro del input con el fin de mejorar la comprensión de su uso.

A continuación, se muestra un ejemplo:

```HTML
<form>
    <input type="text" placeholder="Nombre">
    <input type="text" placeholder="Apellido">
</form>
```

<br>

Y este sería el resultado:

![1-text](https://user-images.githubusercontent.com/110897750/196164381-dc2a3e61-2a61-48c5-b46a-2391e42bcf5b.jpg)

<br>

<sub>[<< Formularios y tablas](README.md#formularios-y-tablas) | [Volver al índice](#indice) | [Atributos >>](./README-inputAtrib.md#atributos-de-los-inputs)</sub>


<br><hr>


<h2 id="password">type= "password"</h2> <!--******************** type= "password" ********************-->

Con este atributo se indica que el input es de tipo contraseña. Esto significa, que a diferencia de lo visto en la imagen anterior, todo lo escrito en este input, no se verá, sino que se mostrarán asteriscos en lugar de los caracteres introducidos.

He aquí un ejemplo:

```HTML
<form>
    <input type="password" placeholder="Contraseña">
</form>
```

<br>

Y este sería el resultado:

![2-password](https://user-images.githubusercontent.com/110897750/196163471-c03fd8c9-76af-451f-868f-8b4057cb86f9.jpg)

<br>

<sub>[<< Formularios y tablas](README.md#formularios-y-tablas) | [Volver al índice](#indice) | [Atributos >>](./README-inputAtrib.md#atributos-de-los-inputs)</sub>


<br><hr>


<h2 id="submit">type= "submit"</h2> <!--******************** type= "submit" ********************-->

Este atributo crea un botón para enviar los datos obtenidos en el formulario a un "gestor de formularios" definido en el atributo *action* de la etiqueta `<form>`.

Si se desea modificar el valor del texto mostrado dentro del botón, se usará el atributo `value`, donde se deberá escribir el texto a mostrar.

He aquí un ejemplo:

```HTML
<form>
    <input type="submit" value="Enviar">
</form>
```

<br>

El resultado del código anterior sería el siguiente:

![3-submit](https://user-images.githubusercontent.com/110897750/196164281-3bec2e48-cf40-405d-8834-6f90f4168b92.jpg)

<br>

<sub>[<< Formularios y tablas](README.md#formularios-y-tablas) | [Volver al índice](#indice) | [Atributos >>](./README-inputAtrib.md#atributos-de-los-inputs)</sub>


<br><hr>


<h2 id="reset">type= "reset"</h2> <!--******************** type= "reset" ********************-->

Al igual que en el caso anterior, este atributo también creará un botón. Sin embargo, el objetivo de éste es borrar el contenido escrito en el formulario, es decir, resetar los valores introducidos en el mismo.

De nuevo, para cambiar el valor del texto mostrado en dicho botón, se puede utilizar el atributo `value`.

He aquí un código de ejemplo:

```HTML
<form>
    <input type="reset">
</form>
```

<br>

Este es el resultado:

![4-reset](https://user-images.githubusercontent.com/110897750/196167352-3485046c-f001-4eb1-b7dc-681dd74518c7.jpg)

<br>

<sub>[<< Formularios y tablas](README.md#formularios-y-tablas) | [Volver al índice](#indice) | [Atributos >>](./README-inputAtrib.md#atributos-de-los-inputs)</sub>


<br><hr>


<h2 id="radio">type= "radio"</h2> <!--******************** type= "radio" ********************-->

Este tipo de input crea un círculo seleccionable. Por norma general, son muy útiles cuando se quiere hacer escoger al usuario una de entre varias opciones disponibles.

Si se desea permitir elegir más de una de las opciones, se recomienda el uso de [checkbox](#checkbox), sin embargo, también es posible realizarlo eliminando el mismo nombre del atributo main. Es decir, si los inputs generados tienen el mismo main, solo podrá escogerse una de dichas opciones, si no tuvieran un atributo name asignado o cada uno tuviera uno diferente, podría seleccionarse más de una opción.

He aquí un ejemplo:

```HTML
<form>
    <input type="radio" id="op1" value="opcion1" name="opciones">
    <label for="op1">Opción 1</label>
    <input type="radio" id="op2" value="opcion2" name="opciones">
    <label for="op2">Opción 2</label>
    <input type="radio" id="op3" value="opcion3" name="opciones">
    <label for="op3">Opción 3</label>
</form>
```

<br>

Este sería el resultado:

![6-radio](https://user-images.githubusercontent.com/110897750/196787815-4c7081fe-bb8e-40e5-9e53-a264f7d0141a.jpg)

<br>

<sub>[<< Formularios y tablas](README.md#formularios-y-tablas) | [Volver al índice](#indice) | [Atributos >>](./README-inputAtrib.md#atributos-de-los-inputs)</sub>


<br><hr>


<h2 id="checkbox">type= "checkbox"</h2> <!--******************** type= "checkbox" ********************-->

Estos inputs son unos cuadrados que permiten seleccionar cero o más opciones, son muy utilizados.

A continuación, se muestra un ejemplo igual al visto en el apartado de [type= "radio"](#radio), donde, esta vez, sí se permite seleccionar más de una opción:

```HTML
<form>
    <input type="checkbox" id="op1" value="opcion1" name="opciones">
    <label for="op1">Opción 1</label>
    <input type="checkbox" id="op2" value="opcion2" name="opciones">
    <label for="op2">Opción 2</label>
    <input type="checkbox" id="op3" value="opcion3" name="opciones">
    <label for="op3">Opción 3</label>
</form>
```

<br>

He aquí el resultado:

![5-checkbox](https://user-images.githubusercontent.com/110897750/196787896-363ca419-2587-4c39-a315-cd4667850018.jpg)

<br>

<sub>[<< Formularios y tablas](README.md#formularios-y-tablas) | [Volver al índice](#indice) | [Atributos >>](./README-inputAtrib.md#atributos-de-los-inputs)</sub>


<br><hr>


<h2 id="button">type= "button"</h2> <!--******************** type= "button" ********************-->

Aunque se recomienda crear botones utilizando la etiqueta `<button>` ya definida para ello, también pueden crearse utilizando el atributo type.

Se puede indicar un texto concreto para que aparezca dentro del botón utilizando el atributo `value`. Además, se le puede añadir también el atributo `onclick`, para que realice una acción específica al clicar sobre él.

He aquí un ejemplo:

```HTML
<form>
    <input type="button" onclick="alert('Hello World!')" value="Clica aquí">
</form>
```

<br>

Y este sería el resultado:

![7-button](https://user-images.githubusercontent.com/110897750/196787948-aa26816c-86a0-4ea2-a6ea-d27711bd196a.jpg)

<br>

<sub>[<< Formularios y tablas](README.md#formularios-y-tablas) | [Volver al índice](#indice) | [Atributos >>](./README-inputAtrib.md#atributos-de-los-inputs)</sub>


<br><hr>


<h2 id="email">type= "email"</h2> <!--******************** type= "email" ********************-->

Tal y como su nombre indica, este tipo de input pide al usuario que inserte un email.

He aquí un ejemplo sencillo:

```HTML
<form>
    <label for="email">Intruduce tu email:</label>
    <input type="email" id="email" required>
</form>
```

<br>

Este sería el resultado:

![11-email](https://user-images.githubusercontent.com/110897750/196788159-e7e17b64-065e-4347-a2d7-bc0aae1fcc2e.jpg)

<br>

<sub>[<< Formularios y tablas](README.md#formularios-y-tablas) | [Volver al índice](#indice) | [Atributos >>](./README-inputAtrib.md#atributos-de-los-inputs)</sub>


<br><hr>


<h2 id="tel">type= "tel"</h2> <!--******************** type= "tel" ********************-->

Este tipo de input es muy útil cuando se desea que el usuario introduzca un número de teléfono.

Se puede utilizar el atributo `pattern` para especificar un formato y mostrarlo con el `placeholder`. En el caso de no cumplir el requisito del formato, no permitirá introducir ese dato.

```HTML
<form>
    <label for="numTel">Introduce tu número de teléfono:</label>
    <input type="tel" id="numTel" pattern="[0-9]{3}[0-9]{3}[0-9]{3}" placeholder="123456789">
</form>
```

<br>

Este sería el resultado:

![17-tel](https://user-images.githubusercontent.com/110897750/196788187-42b9b7c4-3285-4bcc-b5c7-b36770f7adf9.jpg)

<br>

<sub>[<< Formularios y tablas](README.md#formularios-y-tablas) | [Volver al índice](#indice) | [Atributos >>](./README-inputAtrib.md#atributos-de-los-inputs)</sub>


<br><hr>


<h2 id="file">type= "file"</h2> <!--******************** type= "file" ********************-->

Este tipo de input permite al usuario seleccionar un archivo. Por ello, se crean tanto un campo donde seleccionar el archivo, y se añade un comentario con el nombre del archivo seleccionado, o un texto que indique que no ha sido seleccionado ninguno aún.

A continuación, se muestra un ejemplo:

```HTML
<form>
    <label for="archivo">Selecciona un archivo:</label>
    <input type="file" id="archivo">
</form>
```

<br>

He aquí el resultado de dicho código:

![12-file](https://user-images.githubusercontent.com/110897750/196788167-8bcc90fc-d8e3-441d-90bc-fda2a85a9d76.jpg)

<br>

<sub>[<< Formularios y tablas](README.md#formularios-y-tablas) | [Volver al índice](#indice) | [Atributos >>](./README-inputAtrib.md#atributos-de-los-inputs)</sub>


<br><hr>


<h2 id="number">type= "number"</h2> <!--******************** type= "number" ********************-->

Este tipo de input solo permite la introducción de números.

Al igual que en ocasiones anteriores, se pueden definir opciones haciendo uso de atributos, con los cuales restringir o limitar ciertos valores.

En el ejemplo a continuación, se pide al usuario que intruduzca un valor numérico entre el 0 y el 100 con saltos de 5 en 5:

```HTML
<form>
    <label for="num">Puntuación:</label>
    <input type="number" id="num" min="0" max="100" step="5">
</form>
```

<br>

He aquí el resultado del código mostrado:

![14-number](https://user-images.githubusercontent.com/110897750/196788172-34b9a205-5994-4902-ad1a-cc4325689276.jpg)

<br>

<sub>[<< Formularios y tablas](README.md#formularios-y-tablas) | [Volver al índice](#indice) | [Atributos >>](./README-inputAtrib.md#atributos-de-los-inputs)</sub>


<br><hr>


<h2 id="date">type= "date"</h2> <!--******************** type= "date" ********************-->

Con este tipo de input, se puede seleccionar una fecha concretando el día, el mes y el año.

Se pueden utilizar los atributos `min` y `max` para restringir las opciones de selección entre unas fechas concretas.

He aquí un ejemplo:

```HTML
<form>
    <label for="fecha">Fecha de nacimiento:</label>
    <input type="date" id="fecha" max="2022-10-17">
</form>
```

<br>

He aquí el resultado:

![9-date](https://user-images.githubusercontent.com/110897750/196788064-3bd69a39-7ac3-470a-8e2e-e8b93f0281b8.jpg)

<br>

<sub>[<< Formularios y tablas](README.md#formularios-y-tablas) | [Volver al índice](#indice) | [Atributos >>](./README-inputAtrib.md#atributos-de-los-inputs)</sub>


<br><hr>


<h2 id="time">type= "time"</h2> <!--******************** type= "time" ********************-->

Este input permite al usuario seleccionar una hora concreta, sin tener en cuenta la zona horaria.

He aquí un ejemplo:

```HTML
<form>
    <label for="tiempo">Selecciona una hora:</label>
    <input type="time" id="tiempo">
</form>
```

<br>

Este sería el resultado:

![18-time](https://user-images.githubusercontent.com/110897750/196788191-42a71e2c-1f72-489b-a45e-9fe626c23631.jpg)

<br>

<sub>[<< Formularios y tablas](README.md#formularios-y-tablas) | [Volver al índice](#indice) | [Atributos >>](./README-inputAtrib.md#atributos-de-los-inputs)</sub>


<br><hr>


<h2 id="datetime-local">type= "datetime-local"</h2> <!--**************** type= "datetime-local" ****************-->

Este input se utiliza para insertar la fecha, al igual que el tipo de input [date](#date), sin embargo, en esta ocasión, también se debe escoger una hora concreta.

He aquí un ejemplo:

```HTML
<form>
    <label for="fecha-hora">Fecha de nacimiento:</label>
    <input type="datetime-local" id="fecha-hora">
</form>
```

<br>

Este sería el resultado:

![10-datetime-local](https://user-images.githubusercontent.com/110897750/196788152-994a15cd-13ff-4a02-9811-602db08cf5b8.jpg)

<br>

<sub>[<< Formularios y tablas](README.md#formularios-y-tablas) | [Volver al índice](#indice) | [Atributos >>](./README-inputAtrib.md#atributos-de-los-inputs)</sub>


<br><hr>


<h2 id="month">type= "month"</h2> <!--******************** type= "month" ********************-->

Este input permite al usuario introducir un mes y un año concretos.

Aquí se muestra un ejemplo:

```HTML
<form>
    <label for="mes">Mes y año:</label>
    <input type="month" id="mes">
</form>
```

<br>

He aquí el resultado:

![13-month](https://user-images.githubusercontent.com/110897750/196788169-154259b4-d1ad-4c94-91d4-feb54cba7305.jpg)

<br>

<sub>[<< Formularios y tablas](README.md#formularios-y-tablas) | [Volver al índice](#indice) | [Atributos >>](./README-inputAtrib.md#atributos-de-los-inputs)</sub>


<br><hr>


<h2 id="week">type= "week"</h2> <!--******************** type= "week" ********************-->

Este input permite al usuario seleccionar una semana y un año.

He aquí un ejemplo:

```HTML
<form>
    <label for="sem">Introduce una semana:</label>
    <input type="week" id="sem">
</form>
```

<br>

Este sería el resultado:

![20-week](https://user-images.githubusercontent.com/110897750/196788197-20c9f28c-a7cf-4f26-96f8-692fb5f16941.jpg)

<br>

<sub>[<< Formularios y tablas](README.md#formularios-y-tablas) | [Volver al índice](#indice) | [Atributos >>](./README-inputAtrib.md#atributos-de-los-inputs)</sub>


<br><hr>


<h2 id="url">type= "url"</h2> <!--******************** type= "url" ********************-->

Estos inputs se utilizan en aquellas ocasiones en las que se debe introducir un link como entrada.

Si no se introduce una url, la página mostrará un error en la introducción de dicho dato.

He aquí un ejemplo sencillo:

```HTML
<form>
    <label for="link">Introduce tu portfolio:</label>
    <input type="url" id="link">
</form>
```

<br>

Este sería el resultado obtenido:

![19-url](https://user-images.githubusercontent.com/110897750/196788194-576572f6-6894-45d7-a40c-e00e0be41fbe.jpg)

<br>

<sub>[<< Formularios y tablas](README.md#formularios-y-tablas) | [Volver al índice](#indice) | [Atributos >>](./README-inputAtrib.md#atributos-de-los-inputs)</sub>


<br><hr>


<h2 id="color">type= "color"</h2> <!--******************** type= "color" ********************-->

Este tipo de input permite seleccionar un color concreto. El usuario puede escoger el tipo de entrada (hexadecimal, rgb, etc.).

He aquí un ejemplo:

```HTML
<form>
    <label for="selColor">Selecciona un color:</label>
    <input type="color" id="selColor">
</form>
```

<br>

Este sería el resultado:

![8-color](https://user-images.githubusercontent.com/110897750/196788001-ad6ed258-2e8f-4b37-a4dc-94f8f2b5c86e.jpg)

<br>

<sub>[<< Formularios y tablas](README.md#formularios-y-tablas) | [Volver al índice](#indice) | [Atributos >>](./README-inputAtrib.md#atributos-de-los-inputs)</sub>


<br><hr>


<h2 id="image">type= "image"</h2> <!--******************** type= "image" ********************-->

Este tipo de input agraga una imagen como botón de *submit*. La dirección de la imagen se asigna a través del atributo `src`.

He aquí un ejemplo:

```HTML
<form>
    <input type="image" src="../image.jpg" alt="imagen" width="150" height="auto">
</form>
```

<br>

Este sería el resultado:

![21-image](https://user-images.githubusercontent.com/110897750/196789408-e17d407c-6ad6-4bd6-ab5c-47a609f59c65.jpg)

<br>

<sub>[<< Formularios y tablas](README.md#formularios-y-tablas) | [Volver al índice](#indice) | [Atributos >>](./README-inputAtrib.md#atributos-de-los-inputs)</sub>


<br><hr>


<h2 id="range">type= "range"</h2> <!--******************** type= "range" ********************-->

Este input permite seleccionar un valor entre un rango mediante una barra. El balor inicial por defecto aparece en el medio, de entre el mínimo y máximo especificados mediante los atributos *min* y *max* ya vistos anteriormente.

He aquí un ejemplo de código:

```HTML
<form>
    <label for="vol">Volumen global:</label>
    <input type="range" id="vol" min="0" max="100">
</form>
```

<br>

Y este sería el resultado:

![15-range](https://user-images.githubusercontent.com/110897750/196788174-b3b04d52-9a80-4161-8c80-7589f8f40334.jpg)

<br>

<sub>[<< Formularios y tablas](README.md#formularios-y-tablas) | [Volver al índice](#indice) | [Atributos >>](./README-inputAtrib.md#atributos-de-los-inputs)</sub>


<br><hr>


<h2 id="search">type= "search"</h2> <!--******************** type= "search" ********************-->

Este tipo de input genera una especie de rectángulo igual al tipo de input *text*. Sirve para buscar archivos.

He aquí un ejemplo:

```HTML
<form>
    <label for="buscar">Buscar:</label>
    <input type="search" id="buscar">
</form>
```

<br>

Este sería el resultado obtenido:

![16-search](https://user-images.githubusercontent.com/110897750/196788186-928e67ea-b432-49e4-86ef-aa51fc638c40.jpg)

<br>

<sub>[<< Formularios y tablas](README.md#formularios-y-tablas) | [Volver al índice](#indice) | [Atributos >>](./README-inputAtrib.md#atributos-de-los-inputs)</sub>


<br><hr>
<hr><br>


# Créditos

La información de esta página ha sido obtenida a través de realizar diferentes cursos por mi cuenta. Sin embargo, el índice y los datos utilizados aquí han sido traducidos de [w3schools](https://www.w3schools.com/html/html_form_input_types.asp).
