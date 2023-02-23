# Pseudoclases

En este apartado se va a hablar de las pseudoclases que se pueden utilizar en CSS, concretamente, de aquellas **pseudoclases estándar** que se pueden utilizar en **cualquier navegador web**, mostrando un ejemplo sencillo de cada una de ellas.

<p id="indice">He aquí el índice de los temas a tratar:</p>

* [:active](#active)
* [:checked](#checked)
* [:default](#default)
* [:disabled](#disabled)
* [:empty](#empty)
* [:enabled](#enabled)
* [:first-child](#first-child)
* [:first-of-type](#first-of-type)
* [:focus](#focus)
* [:hover](#hover)
* [:indeterminate](#indeterminate)
* [:in-range](#in-range)
* [:invalid](#invalid)
* [:lang()](#lang)
* [:last-child](#last-child)
* [:last-of-type](#last-of-type)
* [:left](#left)
* [:link](#link)
* [:not()](#not)
* [:nth-child()](#nth-child)
* [:nth-last-child()](#nth-last-child)
* [:nth-last-of-type()](#nth-last-of-type)
* [:nth-of-type()](#nth-of-type)
* [:only-child](#only-child)
* [:only-of-type](#only-of-type)
* [:optional](#optional)
* [:out-of-range](#out-of-range)
* [:read-only](#read-only)
* [:read-write](#read-write)
* [:required](#required)
* [:right](#right)
* [:root](#root)
* [:target](#target)
* [:valid](#valid)
* [:visited](#visited)

[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos)


<br><hr><br>


## :active

La pseudoclase `:active` se utiliza para seleccionar un elemento que está siendo activado por el usuario. Por ejemplo, si se pulsa un botón, este se activará y se mostrará con el estilo que se le haya asignado a la pseudoclase `:active`.

He aquí un ejemplo de cómo se puede utilizar:

```html
<button>¡Púlsame!</button>
```

<br>

Dando el siguiente estilo con CSS:

```css
button {
    padding: 10px 15px;
}

button:active {
    background-color: #000;
    color: #fff;
}
```

<br>

Este sería el resultado antes y después de activar el botón:

![1-active](https://user-images.githubusercontent.com/110897750/203446662-8eedcb8f-bd3d-46ee-a0bd-2d6b6ca671c7.jpg)

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>


<br><hr>


## :checked

La pseudoclase `:checked` se utiliza para seleccionar un elemento que está marcado como seleccionado. Por ejemplo, si se pulsa un botón de radio, este se activará y se mostrará con el estilo que se le haya asignado a la pseudoclase `:checked`.

He aquí un ejemplo de cómo se puede utilizar:

```html
<input type="radio" name="radio" id="radio1">
<label for="radio1">No seleccionado</label>
<br>
<input type="radio" name="radio" id="radio2" checked>
<label for="radio2">Seleccionado</label>
```

<br>

Dando el siguiente estilo con CSS:

```css
input + label {
    color: blue;
}

input:checked + label {
    color: red;
}
```

<br>

Este sería el resultado antes y después de activar el botón de radio:

![2-checked](https://user-images.githubusercontent.com/110897750/203446665-bbc6a801-de79-4459-8a9e-76fbbcec7f5b.jpg)

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>


<br><hr>


## :default

La pseudoclase `:default` se utiliza para seleccionar un elemento que está marcado como seleccionado por defecto. Por ejemplo, si se pulsa un botón de radio, este se activará y se mostrará con el estilo que se le haya asignado a la pseudoclase `:default`.

He aquí un ejemplo de cómo se puede utilizar:

```html
<input type="radio" name="radio" id="radio1">
<label for="radio1">Opción 1</label>
<br>
<input type="radio" name="radio" id="radio2">
<label for="radio2">Opción 2</label>
<br>
<input type="radio" name="radio" id="radio3" checked>
<label for="radio3">Opción 3</label>
<br>
<input type="radio" name="radio" id="radio4">
<label for="radio4">Opción 4</label>
```

<br>

Dando el siguiente estilo con CSS:

```css
input:default + label {
    color: red;
}
```

<br>

Este sería el resultado:

![3-default](https://user-images.githubusercontent.com/110897750/203446666-be84998e-5439-4716-ad79-c3547c2c8ad5.jpg)

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>


<br><hr>


## :disabled

La pseudoclase `:disabled` se utiliza para seleccionar un elemento que está desactivado. Por ejemplo, si se insertan unos campos de texto en un formulario, y se indica que están desactivados, se mostrarán con el estilo que se le haya asignado a la pseudoclase `:disabled`.

He aquí un ejemplo de cómo se puede utilizar:

```html
    <form action="#">
        <fieldset id="direccion-envio">
          <legend>Dirección de Envío</legend>
          <input type="text" placeholder="Nombre">
          <input type="text" placeholder="Dirección">
          <input type="text" placeholder="Código postal">
        </fieldset>
        <fieldset id="direccion-facturacion">
          <legend>Dirección de facturación</legend>
          <label for="iguales">Igual que la dirección de envío:</label>
          <input type="checkbox" id="iguales" checked>
          <br>
          <input type="text" placeholder="Nombre" disabled>
          <input type="text" placeholder="Dirección" disabled>
          <input type="text" placeholder="Código postal" disabled>
        </fieldset>
    </form>
```

<br>

Dando el siguiente estilo con CSS:

```css
fieldset {
    width: 300px;
}

input {
    padding: 5px;
}

input[type="text"]:disabled {
    background: #ccc;
}
```

<br>

Este sería el resultado:

![4-disabled](https://user-images.githubusercontent.com/110897750/203446668-a0954afd-d7fb-429d-95e4-e124b488b2d1.jpg)

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>


<br><hr>


## :empty

La pseudoclase `:empty` se utiliza para seleccionar un elemento que no tiene ningún hijo ni texto en el interior. Por ejemplo, si se inserta un elemento `<div>` vacío, se mostrará con el estilo que se le haya asignado a la pseudoclase `:empty`.

He aquí un ejemplo de cómo se puede utilizar:

```html
<div><!-- Este bloque tendrá color salmón --></div>
<div>Color azul</div>
<div>
    <!-- Este bloque también tendrá color azul
    porque tiene espacios en el interior -->
</div>
<div>Color azul</div>
```

<br>

Dando el siguiente estilo con CSS:

```css
div {
    width: 100px;
    height: 100px;
    background-color: lightblue;
}

div:empty {
    background-color: salmon;
}
```

<br>

Este sería el resultado:

![5-empty](https://user-images.githubusercontent.com/110897750/203446670-f3201cf8-810b-43fb-839a-d59f406376bc.jpg)

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>


<br><hr>


## :enabled

La pseudoclase `:enabled` representa cualquier elemento habilitado. Se considera que un elemento está habilitado si puede ser activado o si acepta el foco.

He aquí un ejemplo de cómo se puede utilizar, utilizando código HTML del ejemplo anterior:

```html
<form action="#">
    <fieldset id="direccion-envio">
      <legend>Dirección de Envío</legend>
      <input type="text" placeholder="Nombre">
      <input type="text" placeholder="Dirección">
      <input type="text" placeholder="Código postal">
    </fieldset>
    <fieldset id="direccion-facturacion">
      <legend>Dirección de facturación</legend>
      <label for="iguales">Igual que la dirección de envío:</label>
      <input type="checkbox" id="iguales" checked>
      <br>
      <input type="text" placeholder="Nombre" disabled>
      <input type="text" placeholder="Dirección" disabled>
      <input type="text" placeholder="Código postal" disabled>
    </fieldset>
</form>
```

<br>

Dando el siguiente estilo:

```css
fieldset {
    width: 300px;
}

input:enabled {
    background-color: lightgreen;
    color: black;
}

input:disabled {
    background-color: lightcoral;
    color: white;
}
```

<br>

Este sería el resultado:

![6-enabled](https://user-images.githubusercontent.com/110897750/203446965-7988e82b-eafd-4ea5-ab79-3835fad93a78.jpg)

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>


<br><hr>


## :first-child

La pseudoclase `:first-child` se utiliza para seleccionar el primer elemento hijo de un elemento. Por ejemplo, si se inserta un elemento `<div>` con varios elementos `<p>` dentro, se mostraría con el estilo aquel `p` que esté en primer lugar.

He aquí un ejemplo de cómo se puede utilizar:

```html
<div>
    <p>Este texto sí se selecciona, es una p y es el primer hijo</p>
    <p>Este texto no se selecciona, no es el primer hijo</p>
</div>
<div>
    <span>Este texto no se selecciona, es un span</span>
    <p>Este texto no se selecciona, no es el primer hijo</p>
</div>
```

<br>

Dando el siguiente estilo con CSS:

```css
p:first-child {
    color: lightgreen;
}
```

<br>

Este sería el resultado:

![7-first-child](https://user-images.githubusercontent.com/110897750/203446673-a3483c33-3dbf-4219-82cf-0f50f8cf3de3.jpg)

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>


<br><hr>


## :first-of-type

La pseudoclase `:first-of-type` se utiliza para seleccionar el primer elemento de un tipo de elemento. Por ejemplo, si se inserta un elemento `<div>` con varios elementos `<p>` dentro, se mostraría con el estilo aquel `p` que esté en primer lugar.

He aquí un ejemplo de cómo se puede utilizar:

```html
<div>
    <span>Este texto no se selecciona, es un span</span>
    <p>Este texto sí se selecciona, es una p y es la primera de ese tipo</p>
    <p>Este texto no se selecciona, no es el primer hijo</p>
    <p>Este texto no se selecciona, no es el primer hijo</p>
</div>
```

<br>

Dando el siguiente estilo con CSS:

```css
p:first-of-type {
    color: lightgreen;
}
```

<br>

Este sería el resultado:

![8-first-of-type](https://user-images.githubusercontent.com/110897750/203446675-9a1b31c5-feac-4175-8fab-a0c63e390c07.jpg)

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>


<br><hr>


## :focus

La pseudoclase `:focus` se utiliza para seleccionar el elemento que tiene el foco. El foco es el elemento que está activo en ese momento, por ejemplo, el elemento que está siendo editado en un formulario.

He aquí un ejemplo de cómo se puede utilizar:

```html
<label for="rojo">Seré de color rojo cuando enfoque:</label>
<input type="text" class="rojo" id="rojo" value="Soy color rojo">
<br>
<label for="verde">Seré de color verde cuando enfoque:</label>
<input type="text" class="verde" id="verde" value="Soy color verde">
```

<br>

Dando el siguiente estilo con CSS:

```css
.rojo:focus {
    background-color: red;
    color: white;
}

.verde:focus {
    background-color: green;
    color: white;
}
```

<br>

Este sería el resultado de cada input al ser enfoqueado:

![9-focus](https://user-images.githubusercontent.com/110897750/203446678-fdccf329-2f99-4882-a27f-678cab1b763a.jpg)

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>


<br><hr>


## :hover

La pseudoclase `:hover` se utiliza para seleccionar el elemento que está siendo apuntado por el ratón. Por ejemplo, si se inserta un botón, al pasar el ratón por encima de él, se mostraría con el estilo que se le haya dado.

He aquí un ejemplo de cómo se puede utilizar:

```html
<button>¡Pasa por encima!</button>
```

<br>

Dando el siguiente estilo con CSS:

```css
button {
    padding: 10px 15px;
}

button:hover {
    background-color: #000;
    color: #fff;
}
```

<br>

Este sería el resultado:

![10-hover](https://user-images.githubusercontent.com/110897750/203446681-13cb9c47-fe56-4fc1-b6bf-21593e8be37a.jpg)

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>


<br><hr>


## :indeterminate

La pseudoclase `:indeterminate` se utiliza para seleccionar los elementos que están en un estado indeterminado.

Los elementos que pueden tener este estado son los siguientes:

* `<input type="checkbox">` cuya propiedad `indeterminate` tiene el valor `true`.
* `<input type="radio">` cuando todos los radio buttons con el mismo valor `name` están desmarcados.
* `<progress>` cuando su valor no está definido.

He aquí un ejemplo de cómo se puede utilizar:

```html
<input type="radio" id="radio1" name="radio">
<label for="radio1">Etiqueta1</label><br>
<input type="radio" id="radio2" name="radio">
<label for="radio2">Etiqueta2</label><br>
<input type="radio" id="radio3" name="radio">
<label for="radio3">Etiqueta3</label><br>
<input type="radio" id="radio4" name="radio">
<label for="radio4">Etiqueta4</label><br>
```

<br>

Dando el siguiente estilo con CSS:

```css
input:indeterminate + label {
    color: red;
}
```

<br>

Este sería el resultado:

![11-indeterminate](https://user-images.githubusercontent.com/110897750/203446683-24d7d2ea-cb92-4596-bc40-2f33895e9aef.jpg)

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>


<br><hr>


## :in-range

La pseudoclase `:in-range` se utiliza para seleccionar los elementos que están dentro del rango especificado. Este rango se especifica con las propiedades `min` y `max` de los elementos.

He aquí un ejemplo de cómo se puede utilizar:

```html
<label for="nota">Inserta la puntuación:</label><br>
<input type="number" id="nota" min="0" max="10">
<br>
<label for="nota">Inserta la puntuación:</label><br>
<input type="number" id="nota" min="0" max="10">
```

<br>

Dando el siguiente estilo con CSS:

```css
input:in-range {
    background-color: lightgreen;
}
```

<br>

Este sería el resultado:

![12-in-range](https://user-images.githubusercontent.com/110897750/203446685-d482b9f8-6ee9-4f03-9882-949d9e99b5fb.jpg)

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>


<br><hr>


## :invalid

La pseudoclase `:invalid` se utiliza para seleccionar los elementos que no son válidos. Un elemento es válido cuando cumple con las reglas de validación que se le han dado.

He aquí un ejemplo de cómo se puede utilizar:

```html
<label for="email">Introduce tu email:</label>
<input type="email">
```

<br>

Dando el siguiente estilo con CSS:

```css
input:invalid {
    background-color: lightcoral;
}
```

<br>

Este sería el resultado:

![13-invalid](https://user-images.githubusercontent.com/110897750/203446688-3b58e324-2ddb-44fc-b8c0-35ecd8b2f1f3.jpg)

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>


<br><hr>


## :lang()

La pseudoclase `:lang()` se utiliza para modificar elementos en función del idioma que se le haya dado. Este idioma se especifica con el atributo `lang` de los elementos o el elemento `<meta>`.

He aquí un ejemplo de cómo se puede utilizar:

```html
<div lang="es">La fecha se escribe:</div>
<div lang="en">The date is written:</div>
<div lang="fr">La date est écrite:</div>
```

<br>

Dando el siguiente estilo con CSS:

```css
div:lang(es)::after {
    content: " dia / mes / año";
}

div:lang(en)::after {
    content: " month / day / year";
}

div:lang(fr)::after {
    content: " jour / mois / année";
}
```

<br>

Este sería el resultado:

![14-lang](https://user-images.githubusercontent.com/110897750/203446689-4cfda62e-3b1f-498d-9714-2fc7dc30296c.jpg)

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>


<br><hr>


## :last-child

La pseudoclase `:last-child`, al contrario que `:first-child`, se utiliza para seleccionar el último hijo de un elemento.

He aquí un ejemplo de cómo se puede utilizar:

```html
<div>
    <p>Este texto no se selecciona, no es el último hijo</p>
    <p>Este texto sí se selecciona, es una p y es el último hijo</p>
</div>
<div>
    <p>Este texto no se selecciona, no es el último hijo</p>
    <span>Este texto no se selecciona, es un span</span>
</div>
```

<br>

Dando el siguiente estilo con CSS:

```css
p:last-child {
    color: lightgreen;
}
```

<br>

Este sería el resultado:

![15-last-child](https://user-images.githubusercontent.com/110897750/203446691-756c6aad-a8c9-48e9-818e-b3251ffca17e.jpg)

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>


<br><hr>


## :last-of-type

La pseudoclase `:last-of-type`, al contrario que `:first-of-type`, se utiliza para seleccionar el último elemento de un tipo de elemento.

He aquí un ejemplo de cómo se puede utilizar:

```html
<div>
    <p>Este texto no se selecciona, no es el último de ese tipo</p>
    <p>Este texto no se selecciona, no es el último de ese tipo</p>
    <span>Este texto no se selecciona, es un span</span>
    <p>Este texto sí se selecciona, es una p y es el último de ese tipo</p>
</div>
```

<br>

Dando el siguiente estilo con CSS:

```css
p:last-of-type {
    color: lightgreen;
}
```

<br>

Este sería el resultado:

![16-last-of-type](https://user-images.githubusercontent.com/110897750/203446695-5b01604e-d6ac-4bcb-84a9-7d3c748b61a7.jpg)

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>


<br><hr>


## :left

Esta pseudoclase se utiliza con la regla `@page` para especificar ciertos atributos de la página izquierda de un documento impreso.

Los atributos que se pueden especificar son:

* `margin`
* `padding`
* `border`
* `background`

He aquí un ejemplo de cómo se puede utilizar:

```css
@page:left {
    margin: 1cm;
    padding: 1cm;
    border: 1px solid black;
    background: lightblue;
}
```

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>


<br><hr>


## :link

La pseudoclase `:link` se utiliza para seleccionar los enlaces que no han sido visitados.

He aquí un ejemplo de cómo se puede utilizar:

```html
<a href="#">Este link no ha sido visitado</a>
<a href="https://github.com/nlarrea">Este link ha sido visitado</a>
```

<br>

Dando el siguiente estilo con CSS:

```css
a:link {
    color: orange;
}
```

<br>

Este sería el resultado:

![17-link](https://user-images.githubusercontent.com/110897750/203446697-9ce0784c-99bd-4aa4-a9a0-6787c958dd07.jpg)

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>


<br><hr>


## :not()

La pseudoclase `:not()` se utiliza para seleccionar todos los elementos que no cumplan con el selector que se le haya dado.

He aquí un ejemplo de cómo se puede utilizar:

```html
<p class="igual">Este párrafo tiene la clase "igual"</p>
<p class="igual">Este párrafo tiene la clase "igual"</p>
<p class="no-igual">Este párrafo tiene la clase "no-igual"</p>
<p class="igual">Este párrafo tiene la clase "igual"</p>
```

<br>

Dando el siguiente estilo con CSS:

```css
p:not(.igual) {
    color: red;
}
```

<br>

Este sería el resultado:

![18-not](https://user-images.githubusercontent.com/110897750/203446698-743da1ea-6600-4026-a802-5438edfb6e58.jpg)

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>


<br><hr>


## :nth-child()

La pseudoclase `:nth-child()` se utiliza para seleccionar un elemento basándose en su posición entre los elementos de su mismo tipo.

Pueden utilizarse las siguientes palabras clave o valores:

* `odd` para seleccionar los elementos impares.
* `even` para seleccionar los elementos pares.
* `n` para seleccionar todos los elementos.
* `n+X` para seleccionar los elementos que estén en la posición X, X+1, X+2, etc.
* `n-X` para seleccionar los elementos que estén en la posición X, X-1, X-2, etc.
* `n*X` para seleccionar los elementos que estén en la posición X, X*2, X*3, etc.
* `n/X` para seleccionar los elementos que estén en la posición X, X/2, X/3, etc.

He aquí un ejemplo de cómo se puede utilizar:

```html
<div class="bloques">
    <div class="bloque bloque1">Bloque 1</div>
    <div class="bloque bloque2">Bloque 2</div>
    <div class="bloque bloque3">Bloque 3</div>
    <div class="bloque bloque4">Bloque 4</div>
    <div class="bloque bloque5">Bloque 5</div>
</div>
```

<br>

Dando el siguiente estilo con CSS:

```css
.bloque:nth-child(1) {
    background-color: red;
}

.bloque:nth-child(2) {
    background-color: orange;
}

.bloque:nth-child(3) {
    background-color: green;
}

.bloque:nth-child(4) {
    background-color: blue;
}

.bloque:nth-child(5) {
    background-color: purple;
}
```

<br>

Este sería el resultado:

![19-nth-child](https://user-images.githubusercontent.com/110897750/203446699-9ae080e1-defa-4735-bb42-4bd5b6e88cf0.jpg)

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>


<br><hr>


## :nth-last-child()

La pseudoclase `:nth-last-child()` se usa para seleccionar uno o más elementos basándose en su posición entre los elementos de su mismo tipo, pero contando desde el final.

Pueden utilizarse las siguientes palabras clave o valores:

* `odd` para seleccionar los elementos impares.
* `even` para seleccionar los elementos pares.
* `n` para seleccionar todos los elementos.
* `n+X` para seleccionar los elementos que estén en la posición X, X+1, X+2, etc.
* `n-X` para seleccionar los elementos que estén en la posición X, X-1, X-2, etc.
* `n*X` para seleccionar los elementos que estén en la posición X, X*2, X*3, etc.
* `n/X` para seleccionar los elementos que estén en la posición X, X/2, X/3, etc.

Siguiendo el ejemplo del apartado anterior, pero utilizando `:nth-last-child()`:

```css
.bloque:nth-last-child(-n+2){
    color: white;
    font-weight: 900;
}
```

<br>

Este sería el resultado:

![20-nth-last-child](https://user-images.githubusercontent.com/110897750/203446700-e43bd0f6-264c-489f-b314-efd9fdc5820e.jpg)

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>


<br><hr>


## :nth-last-of-type()

La pseudoclase `:nth-last-of-type()` se usa para seleccionar uno o más elementos basándose en su posición entre los elementos de su mismo tipo, pero contando desde el final.

He aquí un ejemplo de cómo se puede utilizar:

```html
<p>Esto es un párrafo</p>
<p>Esto es otro párrafo</p>
<p>Esto es otro párrafo</p>
<span>Esto es un span</span>
<span>Esto es otro span</span>
<p>Esto es otro párrafo</p>
```

<br>

Dando el siguiente estilo con CSS:

```css
span:nth-last-of-type(2) {
    color: red;
}

p:nth-last-of-type(3) {
    color: blue;
}
```

<br>

Este sería el resultado:

![21-nth-last-of-type](https://user-images.githubusercontent.com/110897750/203446701-872ce4f6-3646-44bd-9dae-2e7954a58c5c.jpg)

<br>

Como se puede observar, el primer párrafo no cambia de color, ya que no es el tercer párrafo contando desde el final. El segundo párrafo sí cambia de color, porque sí lo es, y el tercer párrafo no cambia de color, ya que tampoco es el tercero contando desde el final.

El primer span sí cambia de color ya que es el segundo span contando desde el final, y el segundo span no cambia de color.

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>


<br><hr>


## :nth-of-type()

La pseudoclase `:nth-of-type()` se usa para seleccionar uno o más elementos basándose en su posición entre los elementos de su mismo tipo. Es decir, hace la misma función que `:nth-last-of-type()`, pero contando desde el principio.

Por tanto, siguiendo el mismo ejemplor que en el apartado anterior:

```html
<p>Esto es un párrafo</p>
<p>Esto es otro párrafo</p>
<p>Esto es otro párrafo</p>
<span>Esto es un span</span>
<span>Esto es otro span</span>
<p>Esto es otro párrafo</p>
```

<br>

Dando el siguiente estilo con CSS:

```css
span:nth-of-type(2) {
    color: red;
}

p:nth-of-type(3) {
    color: blue;
}
```

<br>

Este sería el resultado:

![22-nth-of-type](https://user-images.githubusercontent.com/110897750/203446703-59f20502-a1ed-4a74-bafa-32e143589fda.jpg)

<br>

En este caso, cambia el color del tercer párrafo y del segundo span, ya que se cuenta desde el principio.

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>


<br><hr>


## :only-child

La pseudoclase `:only-child` se usa para seleccionar un elemento que es el único hijo de su padre.

Por ejemplo:

```html
<div>
    <p>Yo soy el único hijo</p>
</div>
<div>
    <p>Yo tengo hermanos</p>
    <p>Yo tengo hermanos</p>
    <p>Yo tengo hemanos y <span>tengo un elemento hijo</span></p>
</div>
```

<br>

Dando el siguiente estilo con CSS:

```css
p:only-child, span:only-child {
    color: red;
}
```

<br>

Este sería el resultado:

![23-only-child](https://user-images.githubusercontent.com/110897750/203446705-2a557d86-89b3-4603-bfbd-a859513adfa3.jpg)

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>


<br><hr>


## :only-of-type

La pseudoclase `:only-of-type` se usa para seleccionar un elemento de su mismo tipo dentro de su padre.

Por ejemplo:

```html
<div>
    <p>Yo soy un párrafo</p>
    <p>Yo soy otro párrafo</p>
    <span>Yo soy el único span</span><br>
</div>
<div>
    <span>Yo soy un span</span>
    <p>Yo soy el único párrafo</p>
    <span>Yo soy otro span</span>
</div>
```

<br>

Dando el siguiente estilo con CSS:

```css
p:only-of-type, span:only-of-type {
    color: red;
}
```

<br>

Este sería el resultado:

![24-only-of-type](https://user-images.githubusercontent.com/110897750/203446707-cd198251-7f7d-4896-92b5-999dff1c558c.jpg)

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>


<br><hr>


## :optional

La pseudoclase `:optional` se usa para seleccionar un elemento que no es obligatorio, los `<input>` dentro de un formulario por ejemplo.

He aquí un ejemplo visual:

```html
<form>
    <label for="name">Nombre</label>
    <input type="text" id="name" name="name"><br>
    <label for="email">Email</label>
    <input type="email" id="email" name="email" required><br>
    <label for="phone">Teléfono</label>
    <input type="tel" id="phone" name="phone"><br>
    <button type="submit">Enviar</button>
</form>
```

<br>

Dando el siguiente estilo con CSS:

```css
input:optional {
    background-color: #eee;
}
```

<br>

Para que la pseudoclase `:optional` funcione, el elemento que NO sea opcional debe tener el atributo `required` en su etiqueta.

Este sería el resultado:

![25-optional](https://user-images.githubusercontent.com/110897750/203446710-1cd343c5-e4e3-4688-9320-3350061cbc91.jpg)

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>


<br><hr>


## :out-of-range

La pseudoclase `:out-of-range` se usa para seleccionar un elemento que no está dentro del rango de valores que se le ha asignado.

Siguiendo el ejemplo visto en la pseudoclase [`:in-range`](#in-range), he aquí un ejemplo visual:

```html
<label for="nota">Inserta la puntuación:</label><br>
<input type="number" id="nota" min="0" max="10">
<br>
<label for="nota">Inserta la puntuación:</label><br>
<input type="number" id="nota" min="0" max="10">
```

<br>

Dando el siguiente estilo con CSS:

```css
input:in-range {
    background-color: #00FF0077;
}

input:out-of-range {
    background-color: #FF000077;
}
```

<br>

Este sería el resultado:

![26-out-of-range](https://user-images.githubusercontent.com/110897750/203446711-8bd808c9-1812-4cdd-84de-2fb1d7f55153.jpg)

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>


<br><hr>


## :read-only

La pseudoclase `:read-only` se usa para seleccionar un elemento que no puede ser modificado por el usuario.

He aquí un ejemplo:

```html
<form action="#">
    <label for="name">Nombre</label>
    <input type="text" name="name" id="name">
    <br>
    <label for="email">Email</label>
    <input type="email" name="email" id="email" value="example@email.com" readonly>
    <div>
        <input type="checkbox" name="mantener" id="mantener-email" checked>
        <label for="mantener-email">Mantener email</label>
    </div>
</form>
```

<br>

Dando el siguiente estilo con CSS:

```css
input {
    padding: 5px 10px;
}

input:read-only {
    background-color: #f2f2f2;
    border: 1px solid #ccc;
}
```

<br>

Este sería el resultado:

![27-read-only](https://user-images.githubusercontent.com/110897750/203446712-2c528f13-06c7-4edb-a4c5-f4181dbaa441.jpg)

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>


<br><hr>


## :read-write

La pseudoclase `:read-write` se usa para seleccionar un elemento que puede ser modificado por el usuario.

Siguiendo con el ejemplo visto en la pseudoclase [`:read-only`](#read-only):

```html
<form action="#">
    <label for="name">Nombre</label>
    <input type="text" name="name" id="name">
    <br>
    <label for="email">Email</label>
    <input type="email" name="email" id="email" value="example@email.com" readonly>
    <div>
        <input type="checkbox" name="mantener" id="mantener-email" checked>
        <label for="mantener-email">Mantener email</label>
    </div>
</form>
```

<br>

Dando el siguiente estilo con CSS:

```css
input {
    padding: 5px 10px;
}

input:read-only {
    background-color: #f2f2f2;
    border: 1px solid #ccc;
}

input:read-write {
    background-color: #fff;
    border: 1px solid #ccc;
}
```

<br>

En este caso, el input que sí puede ser editado recibe un color de fondo blanco y un borde gris.

Este sería el resultado:

![28-read-write](https://user-images.githubusercontent.com/110897750/203446713-8e0dac18-4954-47ed-babe-aa29ec4f075c.jpg)

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>


<br><hr>


## :required

La pseudoclase `:required` se usa para seleccionar un elemento que es obligatorio para el usuario.

He aquí un ejemplo:

```html
<form action="#">
    <div>
        <input type="text" name="name" id="name">
        <label for="name">Nombre</label>
    </div>
    <div>
        <input type="email" name="email" id="email" required>
        <label for="email">Email</label>
    </div>
    <div>
        <input type="password" name="password" id="password" required>
        <label for="password">Password</label>
    </div>
    <div>
        <input type="tel" name="phone" id="phone">
        <label for="phone">Teléfono</label>
    </div>
</form>
```

<br>

Dando el siguiente estilo con CSS:

```css
input {
    display: flex;
    order: 2;
    padding: 5px 10px;
}

label {
    display: flex;
    order: 1;
}

input:required {
    border: 1px solid red;
}

input:required ~ label::after {
    content: "*";
    color: red;
}
```

<br>

Este sería el resultado:

![29-required](https://user-images.githubusercontent.com/110897750/203446717-3cb59c85-5a76-4b9a-86da-222012fb6483.jpg)

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>


<br><hr>


## :right

Esta pseudoclase se utiliza con la regla `@page` para especificar ciertos atributos de la página derecha de un documento impreso.

Los atributos que se pueden especificar son:

* `margin`
* `padding`
* `border`
* `background`

He aquí un ejemplo de cómo se puede utilizar:

```css
@page:right {
    margin: 1cm;
    padding: 1cm;
    border: 1px solid black;
    background: lightblue;
}
```

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>


<br><hr>


## :root

La pseudoclase `:root` se usa para seleccionar el elemento raíz del documento. Este elemento es el `<html>`. Ambos son idénticos, sin embargo, el elemento `:root` tiene mayor especificidad.

Esta pseudoclase es muy útil para definir variables CSS globales en CSS.

He aquí un ejemplo:

```html
<div>Esto es un div con variables</div>
```

<br>

Dando el siguiente estilo con CSS:

```css
:root {
    --color: #f5f5f5;
    --background: #cea431;
}

div {
    margin: 15px;
    width: 200px;
    height: 100px;
    background-color: var(--color);
    color: var(--background);
}
```

<br>

Este sería el resultado:

![30-root](https://user-images.githubusercontent.com/110897750/203446718-fd6001d8-48c5-4194-b394-fd66fc0f5f9d.jpg)

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>


<br><hr>


## :target

La pseudoclase `:target` se usa para seleccionar un elemento único con un ID que coincide con el fragmento de la URL.

He aquí un ejemplo con una tabla de contenido:

```html
<ul>
    <li>
        <a href="#p1">Resaltar primer párrafo</a>
    </li>
    <li>
        <a href="#p2">Resaltar segundo párrafo</a>
    </li>
    <li>
        <a href="#ningun-lugar">No resaltar nada</a>
    </li>
</ul>
<p id="p1">Lorem ipsum dolor sit amet consectetur adipisicing elit. Vero, modi.</p>
<p id="p2">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Dolorum natus cupiditate aliquid? Eos, ad deserunt?</p>
```

<br>

Dando el siguiente estilo con CSS:

```css
p:target {
    background-color: goldenrod;
}

p:target::before {
    content: "-> ";
}
```

<br>

Con este código se puede conseguir hacer algo como lo siguiente:

* Al hacer click en el enlace "Resaltar primer párrafo", el primer párrafo se resaltará y se le añadirá un "-> " al principio. Los demás elementos no se verán afectados.

![31-target1](https://user-images.githubusercontent.com/110897750/203446719-fb805842-58b5-4e9d-a449-90043fa71b27.jpg)

<br>

* Al hacer click en el enlace "Resaltar segundo párrafo", el segundo párrafo se resaltará y se le añadirá un "-> " al principio. Los demás elementos no se verán afectados.

![31-target2](https://user-images.githubusercontent.com/110897750/203446721-5e2a3911-34a5-4c3d-bdbd-d38be3998eb9.jpg)

<br>

* Al hacer click en el enlace "No resaltar nada", no se resaltará nada.

![31-target3](https://user-images.githubusercontent.com/110897750/203446722-e149b193-0b9a-4a88-8811-7e06598ce1ef.jpg)

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>


<br><hr>


## :valid

La pseudoclase `:valid` se usa para seleccionar elementos que son válidos. Un elemento es válido si cumple con todas las reglas de validación del formulario.

Es la pseudoclase opuesta a `:invalid`.

Siguiendo con el ejemplo de dicha pseudoclase, se puede hacer lo siguiente:

```html
<label for="email">Introduce tu email:</label>
<input type="email">
```

<br>

Dando el siguiente estilo con CSS:

```css
input:invalid {
    background-color: lightcoral;
}

input:valid {
    background-color: lightgreen;
}
```

<br>

Este sería el resultado en este caso:

![32-valid](https://user-images.githubusercontent.com/110897750/203446723-b6713f09-9587-4ceb-b5b4-a438360fe5fc.jpg)

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>


<br><hr>


## :visited

La pseudoclase `:visited` se usa para seleccionar un enlace que ya ha sido visitado por el usuario.

He aquí un ejemplo:

```html
<a href="https://github.com/nlarrea">
    <i class="bi bi-github"></i>
    nlarrea
</a>
<br>
<a href="link">
    <i class="bi bi-eye-slash"></i>
    Link no visitado
</a>
```

<br>

Dando el siguiente estilo con CSS:

```css
a:visited {
    color: lightcoral;
}
```

<br>

Este sería el resultado:

![33-visited](https://user-images.githubusercontent.com/110897750/203446724-e606fad4-e6e0-4b57-8495-adbaf7f37691.jpg)

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>