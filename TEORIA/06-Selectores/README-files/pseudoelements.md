# Pseudoelementos

En este apartado se va a hablar de los pseudoelementos que se pueden utilizar en CSS.

Al igual que con las pseudoclases, los pseudoelementos son palabras clave que se añaden al final de un selector para seleccionar partes de un elemento que no se pueden seleccionar con un selector normal.

La diferencia entre los pseudoelementos y las pseudoclases es que los pseudoelementos no describen un estado del elemento, sino que seleccionan partes del elemento. Además, para utilizar pseudoelementos se debe utilizar el doble dos puntos (`::`) en lugar del simple dos puntos (`:`).

<p id="indice">He aquí el índice de los temas a tratar:</p>

* [::after](#after)
* [::before](#before)
* [::first-letter](#first-letter)
* [::first-line](#first-line)
* [::selection](#selection)
* [::placeholder](#placeholder)
* [::marker](#marker)

<br>

[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos)


<br><hr><br>


## ::after

El pseudoelemento `::after` permite añadir contenido **después de un elemento**. Este contenido puede ser texto, una imagen, etc.

He aquí un ejemplo:

```html
<p class="not-important">
    Lorem ipsum dolor sit amet, consectetur adipisicing elit.
    Reiciendis voluptas in dignissimos quos, ullam explicabo!
</p>
<p class="important">
    Lorem ipsum dolor sit amet consectetur adipisicing elit.
    Veritatis, praesentium.
    </p>
<p class="important">
    Lorem ipsum dolor sit amet consectetur adipisicing elit.
    Cupiditate quaerat adipisci, reprehenderit aut atque dolore
    dolorum ipsum quos fugiat provident?
</p>
<p class="not-important">
    Lorem ipsum dolor sit amet consectetur adipisicing elit.
    Quisquam, quod.
</p>
```

<br>

Dando el siguiente estilo con CSS:

```css
.important::after {
    content: " (Importante)";
    color: red;
}
```

<br>

Se obtiene el siguiente resultado:

![1-after](https://user-images.githubusercontent.com/110897750/203524071-a917648c-a99a-41d1-8179-cab7d4883d37.jpg)

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>


<br><hr>


## ::before

El pseudoelemento `::before` es igual que el pseudoelemento `::after`, solo que permite añadir contenido **antes de un elemento** en vez de después. Este contenido puede ser texto, una imagen, etc.

He aquí un ejemplo:

```html
<p>Poner algo <q>entre comillas</q> así es muy fácil</p>
```

<br>

Dando el siguiente estilo con CSS:

```css
q::before {
    content: "«";
    color: red;
}

q::after {
    content: "»";
    color: red;
}
```

<br>

Se obtiene el siguiente resultado:

![2-before](https://user-images.githubusercontent.com/110897750/203524080-8cb0f50f-c64c-4d79-ba85-3e6c801121c6.jpg)

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>


<br><hr>


## ::first-letter

El pseudoelemento `::first-letter` permite seleccionar la **primera letra** de un elemento. Este pseudoelemento puede ser utilizado para darle un estilo diferente a la primera letra de un párrafo, por ejemplo.

He aquí un ejemplo:

```html
<p>
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Impedit 
    neque velit numquam amet? Dignissimos inventore officiis animi iusto 
    nisi quo eos consectetur esse dolores, vel quia sit reprehenderit 
    praesentium velit quod tempore possimus quae aliquam exercitationem 
    impedit rerum expedita! Adipisci eligendi eveniet fugiat nesciunt 
    cumque reiciendis tempora quis ea. Debitis!
</p>
```

<br>

Dando el siguiente estilo con CSS:

```css
p::first-letter {
    font-size: 2em;
    font-weight: 900;
    color: red;
}
```

<br>

Se obtiene el siguiente resultado:

![3-first-letter](https://user-images.githubusercontent.com/110897750/203524082-81f77299-2733-4b3a-84d9-d7653dc55bea.jpg)

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>


<br><hr>


## ::first-line

El pseudoelemento `::first-line` permite seleccionar la **primera línea** de un elemento. Este pseudoelemento puede ser utilizado para darle un estilo diferente a la primera línea de un párrafo.

He aquí un ejemplo:

```html
<p>
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Impedit 
    neque velit numquam amet? Dignissimos inventore officiis animi iusto 
    nisi quo eos consectetur esse dolores, vel quia sit reprehenderit 
    praesentium velit quod tempore possimus quae aliquam exercitationem 
    impedit rerum expedita! Adipisci eligendi eveniet fugiat nesciunt 
    cumque reiciendis tempora quis ea. Debitis!
</p>
```

<br>

Dando el siguiente estilo con CSS:

```css
p::first-line {
    font-weight: 900;
    color: blue;
}
```

<br>

Se obtiene el siguiente resultado:

![4-first-line](https://user-images.githubusercontent.com/110897750/203524086-74451aa4-c558-44ce-881c-6bfef645d3ca.jpg)

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>


<br><hr>


## ::selection

El pseudoelemento `::selection` permite seleccionar el **texto seleccionado por el usuario**.

He aquí un ejemplo:

```html
<p>Este texto tiene parte seleccionada.</p>
```

<br>

Dando el siguiente estilo con CSS:

```css
p::selection {
    background-color: green;
    color: white;
}
```

<br>

Se obtiene el siguiente resultado:

![5-selection](https://user-images.githubusercontent.com/110897750/203524087-a04894cf-8762-4b9f-abb3-8e331e492ffc.jpg)

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>


<br><hr>


## ::placeholder

El pseudoelemento `::placeholder` permite seleccionar el texto de un elemento `<input>` que se muestra cuando el elemento no tiene ningún valor.

He aquí un ejemplo:

```html
<label for="name">Nombre</label>
<input type="text" id="name" placeholder="Tu nombre">
```

<br>

Dando el siguiente estilo con CSS:

```css
input {
    padding: 5px 10px;
}

input::placeholder {
    color: orange;
}
```

<br>

Se obtiene el siguiente resultado:

![6-placeholder](https://user-images.githubusercontent.com/110897750/203524090-f1b15381-0b31-4bf8-a884-6029100c6397.jpg)

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>


<br><hr>


## ::marker

El pseudoelemento `::marker` permite seleccionar el marcador de una lista.

Es un pseudoelemento que **está en fase de desarrollo**, por lo que no es soportado por todos los navegadores, aunque sí por la mayoría.

He aquí un ejemplo:

```html
<ul>
    <li>Elemento 1</li>
    <li>Elemento 2</li>
    <li>Elemento 3</li>
    <li>Elemento 4</li>
</ul>
```

<br>

Dando el siguiente estilo con CSS:

```css
ul {
    list-style: square;
}

li::marker {
    color: red;
    font-size: 1.5em;
}
```

<br>

Se obtiene el siguiente resultado:

![7-marker](https://user-images.githubusercontent.com/110897750/203524094-ba955916-1c93-4a36-b5b1-37cc0c7dc0ba.jpg)

<sub>[Selectores, Pseudoclases y Pseudoelementos](../README.md#selectores,-pseudoclases-y-pseudoelementos) | [Volver al índice](#indice)</sub>