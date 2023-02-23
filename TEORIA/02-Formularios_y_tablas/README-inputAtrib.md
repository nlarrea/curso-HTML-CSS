# ATRIBUTOS DE LOS INPUTS

En esta sección se hablará de los atributos disponibles en los formularios.

Puede parecer una guía repetitiva, por ello, está planteada más como guía puntual para acceder de forma rápida a un ejemplo donde ver la sintaxis y las posibilidades de cada input.

<p id="indice">Como siempre, he aquí un índice que permitirá una navegación más rápida y cómoda:</p>

* [value](#value)
* [readonly](#readonly)
* [disabled](#disabled)
* [size](#size)
* [maxlength](#maxlength)
* [min y max](#min-max)
* [multiple](#multiple)
* [pattern](#pattern)
* [placeholder](#placeholder)
* [required](#required)
* [step](#step)
* [autofocus](#autofocus)
* [height y width](#height-width)
* [list](#list)
* [autocomplete](#autocomplete)

<br>

[<< FORMULARIOS Y TABLAS](./README.md#formularios-y-tablas) | [INPUTS >>](./README-inputTypes.md#tipos-de-inputs)


<br><hr>

<h2 id="value">value</h2>

Este atributo permite especificar un valor inicial por defecto para un elemento de input.

En este ejemplo se muestra cómo la entrada *"Nombre"* tiene un valor inicial asignado, sin embargo, *"Apellido"* no, por eso aparece vacío. El usuario puede cambiar ambos valores por los deseados:

```HTML
<form>
    <label for="nombre">Nombre:</label>
    <input type="text" id="nombre" value="Naia">
    <label for="apellido">Apellido:</label>
    <input type="text" id="apellido">
</form>
```

<br>

He aquí el resultado:

![1-value](https://user-images.githubusercontent.com/110897750/196882132-7d6de24f-c9c6-4351-bc2d-a603d4106a37.jpg)

<br>

<sub>[<< Formularios y tablas](README.md#formularios-y-tablas) | [Volver al índice](#indice) | [Inputs >>](./README-inputTypes.md)</sub>


<br><hr>

<h2 id="readonly">readonly</h2>

Los inputs con este atributo no pueden ser editados. El usuario podrá acceder a este elemento con el tabulador, e incluso seleccionar y copiar su contenido, pero no podrá modificarlo. El valor que contenga este input será enviado al realizar la acción de enviar formulario.

En este caso, al igual que en el ejemplo anterior, el input *"Nombre"* tiene un valor por defecto, sin embargo, esta vez no puede ser editado:

```HTML
<form>
    <label for="nombre">Nombre:</label>
    <input type="text" id="nombre" value="Naia" readonly>
    <label for="apellido">Apellido:</label>
    <input type="text" id="apellido">
</form>
```

<br>

En un principio, esta imagen parece la misma que la del apartado anterior. Parecen lo mismo aunque no sea así, por ello te invito a que puebes ámbos códigos para ver la diferencia

Este sería el resultado:

![2-readonly](https://user-images.githubusercontent.com/110897750/196882134-7a3e014b-2a73-4445-b90e-cfa8aaeb6fd7.jpg)

<br>

<sub>[<< Formularios y tablas](README.md#formularios-y-tablas) | [Volver al índice](#indice) | [Inputs >>](./README-inputTypes.md)</sub>


<br><hr>

<h2 id="disabled">disabled</h2>

Los inputs de este tipo estarán deshabilitados, tal y como indica su nombre. No podrán ser modificados y su contenido no será enviado al realizar la acción de enviar formulario, al contrario que con el atributo anterior.

Aquí se muestra un código de ejemplo:

```HTML
<form>
    <label for="nombre">Nombre:</label>
    <input type="text" id="nombre" value="Naia" disabled>
    <label for="apellido">Apellido:</label>
    <input type="text" id="apellido">
</form>
```

<br>

Siguiendo el mismo ejemplo que en los apartados anteriores, esta vez se puede observar una pequeña diferencia entre el input con el atributo disabled y el input que no tiene ningún otro atributo.

He aquí el resultado del ejemplo:

![3-disabled](https://user-images.githubusercontent.com/110897750/196886639-21078884-31e3-4471-bbc8-b361605fa05f.jpg)

<br>

<sub>[<< Formularios y tablas](README.md#formularios-y-tablas) | [Volver al índice](#indice) | [Inputs >>](./README-inputTypes.md)</sub>


<br><hr>

<h2 id="size">size</h2>

Este atributo especifica la anchura visible en caracteres de un input. Su valor por defecto es siempre 20, y funciona con los siguientes tipos de inputs:

* text
* password
* email
* tel
* url
* search

<br>

He aquí un pequeño ejemplo:

```HTML
<form>
    <label for="nombre">Nombre:</label>
    <input type="text" id="nombre" size="10">
    <label for="email">Email:</label>
    <input type="email" id="email" size="30">
</form>
```

<br>

Aquí se muestra el resultado:

![4-size](https://user-images.githubusercontent.com/110897750/196882137-7a8f8d68-4d00-4708-84e7-71cbae9c2ae6.jpg)

<br>

<sub>[<< Formularios y tablas](README.md#formularios-y-tablas) | [Volver al índice](#indice) | [Inputs >>](./README-inputTypes.md)</sub>


<br><hr>

<h2 id="maxlength">maxlength</h2>

Este atributo especifica el número máximo de caracteres permitido en el input.

Se debe tener en cuenta que, a pesar de no aceptar más caractéres de los especificados, el usuario puede sobrepasar dicha cantidad sin que la página muestre ningún mensaje de alerta. Para evitar esto, se debería utilizar JavaSript.

He aquí un ejemplo de código:

```HTML
<form>
    <label for="user">ID:</label>
    <input type="text" id="user" maxlength="5" placeholder="12345">
    <label for="pword">Pin:</label>
    <input type="password" id="pword">
</form>
```

<br>

Este sería el resultado:

![5-maxlength](https://user-images.githubusercontent.com/110897750/196882139-bb96f29a-7a60-4016-bb56-b0e8e0a6537e.jpg)

<br>

<sub>[<< Formularios y tablas](README.md#formularios-y-tablas) | [Volver al índice](#indice) | [Inputs >>](./README-inputTypes.md)</sub>


<br><hr>

<h2 id="min-max">min y max</h2>

Este par de atributos sirven para especificar un valor mínimo y máximo del input. Estos son los inputs con los que se pueden utilizar estos atributos:

* number
* range
* date
* time
* datetime-local
* month
* week

<br>

He aquí un ejemplo de código:

```HTML
<form>
    <label for="nombre">Nombre:</label>
    <input type="text" id="nombre">
    <label for="bday">Fecha de nacimiento:</label>
    <input type="date" id="bday" max="2022-10-20">
</form>
```

<br>

Con este ejemplo, no se permite seleccionar una fecha mas actual que la del 2022-10-20. De nuevo, te invito a copiar el código mostrado y probar a introducir los datos.

Este sería el resultado:

![6-min-max](https://user-images.githubusercontent.com/110897750/196882105-0f2cf643-a0a7-4035-8425-c92c5d80b1f5.jpg)

<br>

<sub>[<< Formularios y tablas](README.md#formularios-y-tablas) | [Volver al índice](#indice) | [Inputs >>](./README-inputTypes.md)</sub>


<br><hr>

<h2 id="multiple">multiple</h2>

Este atributo permite al usuario introducir más de un dato en un mismo campo. Es válido para los siguientes inputs:

* email
* file

<br>

He aquí un ejemplo de código:

```HTML
<form>
    <label for="nombre">Nombre:</label>
    <input type="text" id="nombre" size="10">
    <label for="email">Emails de contacto:</label>
    <input type="email" id="email" size="40" multiple placeholder="ejemplo1@algo.com, ejemplo2@algo.com">
</form>
```

<br>

Este sería el resultado:

![7-multiple](https://user-images.githubusercontent.com/110897750/196882110-28ad5ccd-4d5b-426d-9d2b-b906e31c6e5b.jpg)

<br>

<sub>[<< Formularios y tablas](README.md#formularios-y-tablas) | [Volver al índice](#indice) | [Inputs >>](./README-inputTypes.md)</sub>


<br><hr>

<h2 id="pattern">pattern</h2>

Este atributo permite especificar una *expresión regular* con la que comparar la entrada del usuario al enviar el formulario. Funciona con los siguientes tipos de inputs:

* text
* password
* email
* tel
* date
* url
* search

<br>

He aquí un ejemplo de código:

```HTML
<form>
    <label for="usuario">ID de Usuario:</label>
    <input type="text" id="usuario" pattern="[A-z0-9]{5}" title="5 dígitos alfa-numéricos">
</form>
```

<br>

Como tip, se podría añadir el atributo `title`, donde escribir un breve resumen de lo añadido en el atributo `pattern`. Ese atributo funciona en cualquier elemento de HTML y actúa como un tooltip. ¡Te invito a que realices el código mostrado arriba para probarlo!

Si los datos introducidos no corresponden con la expresión de `pattern`, a la hora de enviar el formulario, la página mostrará una alerta donde se puede ver la información descrita en el atributo `title`.

Si quieres saber más acerca de expresiones regulares, te invito a buscar más información [aquí](https://www.w3schools.com/jsref/jsref_obj_regexp.asp).

Este sería el resultado:

![8-pattern](https://user-images.githubusercontent.com/110897750/196882112-a9385422-b2c4-46d6-a628-29474cce539d.jpg)

<br>

<sub>[<< Formularios y tablas](README.md#formularios-y-tablas) | [Volver al índice](#indice) | [Inputs >>](./README-inputTypes.md)</sub>


<br><hr>

<h2 id="placeholder">placeholder</h2>

Este atributo es muy común y ya ha sido utilizado en varias ocasiones a lo largo de esta guía. Sirve para mostrar un ejemplo del tipo de input a introducir, o una breve descripción del mismo.

Funciona con los siguientes inputs:

* text
* password
* email
* tel
* url
* search

<br>

He aquí un pequeño ejemplo:

```HTML
<form>
    <label for="usuario">Usuario:</label>
    <input type="text" id="usuario" placeholder="user0123">
    <label for="email">Email:</label>
    <input type="email" id="email" placeholder="user0123@algo.com">
</form>
```

<br>

Este sería el resultado:

![9-placeholder](https://user-images.githubusercontent.com/110897750/196882115-c7e84106-634a-4be7-8fed-26df5316cbdc.jpg)

<br>

<sub>[<< Formularios y tablas](README.md#formularios-y-tablas) | [Volver al índice](#indice) | [Inputs >>](./README-inputTypes.md)</sub>


<br><hr>

<h2 id="required">required</h2>

Este atributo indica que un input concreto es obligatorio para enviar el formulario. Funciona con los siguientes campos:

* texto
* password
* email
* radio
* checkbox
* tel
* file
* number
* cualquier tipo de date-pickers
* url
* search

<br>

He aquí un ejemplo sencillo:

```HTML
<form>
    <label for="usuario">Usuario:</label>
    <input type="text" id="usuario" required>
    <label for="pword">Contraseña:</label>
    <input type="password" id="pword">
</form>
```

<br>

Este sería el resultado:

![10-required](https://user-images.githubusercontent.com/110897750/196882118-7d18a15f-1879-45ab-ad94-009734ec467f.jpg)

<br>

A simple vista, no se aprecia la diferencia entre tener dicho requisito o no, ambos campos se ven iguales. Pero si el campo con el atributo `required` no está especificado, no permitirá enviar el formulario.

<sub>[<< Formularios y tablas](README.md#formularios-y-tablas) | [Volver al índice](#indice) | [Inputs >>](./README-inputTypes.md)</sub>


<br><hr>

<h2 id="step">step</h2>

Este atributo permite especificar el intervalo entre un valor y el siguiente. Conviene utilizarlo con `min` y `max` para crear rangos y es posible utilizarlo con los siguientes tipos de inputs:

* number
* range
* date
* time
* datetime-local
* month
* week

<br>

He aquí un ejemplo sencillo:

```HTML
<form>
    <label for="vol">Volumen:</label>
    <input type="range" id="vol" min="0" max="100" step="10">
</form>
```

<br>

En este ejemplo, a pesar de no apreciarse en la imagen, solo permite mover el valor del rango de 10 en 10. ¡Copia el código y pruébalo en tu editor!

Este sería el resultado:

![11-step](https://user-images.githubusercontent.com/110897750/196882120-8626a219-07c9-4012-a778-aba0d1e900d6.jpg)

<br>

<sub>[<< Formularios y tablas](README.md#formularios-y-tablas) | [Volver al índice](#indice) | [Inputs >>](./README-inputTypes.md)</sub>


<br><hr>

<h2 id="autofocus">autofocus</h2>

Este atributo hace que el input se vea *"enfocado"* o *"destacado"* desde el momento en el que la página es cargada.

He aquí un ejemplo:

```HTML
<form>
    <label for="usuario">Usuario:</label>
    <input type="text" id="usuario">
    <label for="email">Email:</label>
    <input type="email" id="email" autofocus>
</form>
```

<br>

En este ejemplo, el usuario es llevado automáticamente al campo de *"Email"*.

Este es el resultado:

![12-autofocus](https://user-images.githubusercontent.com/110897750/196882122-bf64cbe1-64d6-461f-87a3-cb429b2b943a.jpg)

<br>

<sub>[<< Formularios y tablas](README.md#formularios-y-tablas) | [Volver al índice](#indice) | [Inputs >>](./README-inputTypes.md)</sub>


<br><hr>

<h2 id="height-width">height y width</h2>

Este par de atributos sirven para especificar la altura y anchura de un tipo de input `image`, respectivamente.

Siempre es recomendable introducir ambos datos, para así indicar a la página cuánto ocupará dicha imagen y que no modifique su disposición cuando ésta se cargue.

A continuación, se muestra un ejemplo:

```HTML
<form>
    <label for="image">Imagen:</label><br>
    <input type="image" id="image" src="../03-Imagenes/img/skyrim.jpg" alt="logo" width="200" height="150">
</form>
```

<br>

Este es el resultado:

![13-height-width](https://user-images.githubusercontent.com/110897750/196882126-8d54e8d1-1ef9-43c0-a40e-6e94e96954b6.jpg)

<br>

<sub>[<< Formularios y tablas](README.md#formularios-y-tablas) | [Volver al índice](#indice) | [Inputs >>](./README-inputTypes.md)</sub>


<br><hr>

<h2 id="list">list</h2>

Este atributo se utiliza con el elemento `<datalist>`, el cual contiene opciones predefinidas como input.

He aquí un ejemplo:

```HTML
<form>
    <input list="consolas">
    <datalist id="consolas">
        <option value="Nintendo Switch"></option>
        <option value="Xbox"></option>
        <option value="Play Station"></option>
    </datalist>
</form>
```

<br>

En este ejemplo, se muestra una barra donde el usuario puede escribir. A medida que escriba algo, si coincide con algún valor predefinido, le aparecerá como sugerencia. También puede optar por no escribir y seleccionar el dato de la lista desplegable.

He aquí el resultado:

![14-list](https://user-images.githubusercontent.com/110897750/196882127-f874fe3f-1ac9-4193-89e6-0618ed64504a.jpg)

<br>

<sub>[<< Formularios y tablas](README.md#formularios-y-tablas) | [Volver al índice](#indice) | [Inputs >>](./README-inputTypes.md)</sub>


<br><hr>

<h2 id="autocomplete">autocomplete</h2>

Este atributo especifica si un campo debe ser autocompletado o no. Si está activo, el buscador comenzará a predecir el dato introducido basándose en datos anteriores. El atributo funciona en los formularios con los siguientes tipos de inputs:

* text
* password
* email
* tel
* url
* selectores de tiempos o fechas
* range
* color
* search

<br>

He aquí un ejemplo:

```HTML
<form autocomplete="on">
    <label for="nombre">Nombre:</label>
    <input type="text" id="nombre">
    <label for="email">Email:</label>
    <input type="email" id="email" autocomplete="off">
</form>
```

<br>

En este caso, permitirá autocompletar todos los campos excepto aquel que esté marcado como `autocomplete="off"`, donde el buscador no ofrecerá ningún valor posible. ¡Prueba el código por tu cuenta para ver las diferencias entre ambos campos!

Este es el resultado:

![15-autocomplete](https://user-images.githubusercontent.com/110897750/196882129-9384db7f-bb53-43b4-a9ef-b9a51001d1f1.jpg)

<br>

<sub>[<< Formularios y tablas](README.md#formularios-y-tablas) | [Volver al índice](#indice) | [Inputs >>](./README-inputTypes.md)</sub>


<br><hr>
<hr><br>


# Créditos

La información de esta página ha sido obtenida a través de realizar diferentes cursos por mi cuenta. Sin embargo, el índice y los datos utilizados aquí han sido traducidos de [w3schools](https://www.w3schools.com/html/html_form_attributes.asp).
