# Estilar formularios

Existen todas las posibilidades imaginables para estilizar los formularios. En este caso, vamos a ver ejemplos simples para poder ver cómo se puede hacer y dar ideas a quien quiera.

<p id="indice">En este apartado se encuentran 3 archivos con formularios o ítems de formularios:</p>

* [Introducción](#introducción)
* [Formulario 1](#formulario-1)
* [Formulario 2](#formulario-2)

<br>

[<< TEMA 6](../06-Selectores/README.md#selectores-pseudoclases-y-pseudoelementos) | [INICIO](../../README.md#temario-del-curso---teoria)


<br><hr>
<hr><br>


## Introducción

En este primer apartado o archivo, se muestran los elementos más básicos que forman un formulario, así como formas super simples (y horribles todo sea dicho) de estilizarlos. Consiste en ver que hay muchas opciones posibles, no en hacer un formulario bonito.

De todas formas, si lo que deseas es volver a recordar las opciones para formularios que ofrece HTML, puedes regresar al [TEMA 2](../02-Formularios_y_tablas/README.md#formularios-y-tablas) donde encontrarás una lista de todos los inputs disponibles.

Este es el código HTML:

```html
<form action="" method="">
    <div class="input-wrapper">
        <label for="name">Usuario:</label>
        <input class="input input-name" type="text" id="name"/> <!-- input de tipo texto -->
        <label for="pass">Contraseña:</label>
        <input class="input input-password" type="password" id="pass"/> <!-- input de tipo contraseña -->
    </div>
    <!-- input para modificar con un diseño más moderno: -->
    <input class="input-moderno" type="text" placeholder="Tu nombre"/><br>
    <!-- input para modificar el color de fondo y añadirle sombras: -->
    <input class="input-background" type="text" placeholder="Escribe algo"/><br>
    <!-- input para añadirle una imagen de fondo: -->
    <input class="input-search" type="text" placeholder="Buscar"/><br>
    <!-- área de texto: -->
    <textarea name="descripcion" placeholder="Danos tu opinión"></textarea><br>
    <!-- selector de opciones: -->
    <select>
        <option>Opción 1</option>
        <option>Opción 2</option>
        <option>Opción 3</option>
    </select>
</form>
```

<br>

Y este es el código CSS:

```css
/* GRUPO DE INPUT 1 */
.input-wrapper {
    width: 100%;
    height: fit-content;
    display: flex;
    justify-content: space-evenly;
}

.input {
    width: 30%;
    padding: 5px 10px;
    margin-bottom: 10px;
    border: 2px solid green;
    border-radius: 10px;
}

/* acceder a la clase input cuyo atributo type sea password: */
.input[type="password"] {
    color: red;
    outline: none;
}

/* INPUT 2 */
.input-moderno {
    border: none;
    border-bottom: 1px solid #c2c2c2;
    outline: none;
    padding: 5px;
    margin-bottom: 10px;
    color: #5f5f5f;
}

.input-moderno::placeholder{
    color: #c2c2c2;
}

.input-moderno:focus{
    border-bottom: 1px solid #5f5f5f;
}

/* CAMBIAR EL BACKGROUND Y AÑADIR SHADOWS */
.input-background {
    background-color: aquamarine;
    border: none;
    border-radius: 5px;
    padding: 5px 10px;
    margin-bottom: 10px;
    outline: none;
    box-shadow: 0 0 10px #ccc;
}

.input-background::placeholder{
    color: #777;
}

/* AÑADIR UNA IMAGEN DE FONDO */
.input-search {
    padding: 10px;
    padding-left: 30px;
    margin-bottom: 10px;
    border: none;
    border-radius: 8px;
    background-color: #eee;
    background-image: url('./img/searchicon.png');
    background-size: 20px;
    background-repeat: no-repeat;
    background-position: 5px;
}

/* ÁREA DE TEXTO */
textarea {
    resize: both;
    /* both: permite modificar su tamaño en horizontal y vertical
        horizontal: permite redimensionarlo solo de forma horizontal
        vertical: permite redimensionarlo solo de forma vertical
        none (por defecto): no permite redimensionarlo */
    margin-bottom: 10px;
}

/* SELECTOR DE OPCIONES */
select {
    width: 100%;
    padding: 15px;
    background-color: #ccc;
}
```

<br>

Y este es el resultado:

![1-elementos-formularios](https://user-images.githubusercontent.com/110897750/209569321-6f947f47-4d57-4ea7-ae1c-0a6dc1d84b3e.jpg)

<sub>[Ver código](./1-intro/) | [Volver al índice](#indice)</sub>


<br><hr>
<hr><br>


## Formulario 1

En este segundo apartado se muestra un formulario más completo, no únicamente ítems sueltos, sino que se enseña cómo podría ser un formulario real para iniciar sesión o registrarse en una página web.

Este es el código HTML:

```html
<div class="container"> <!-- alberga todos los elementos -->
    <h3>Regístrate en los formularios</h3>
    <div class="buttons"> <!-- botones de google y twitter -->
        <button class="google-btn"> <!-- google -->
            <picture>
                <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/53/Google_%22G%22_Logo.svg/2048px-Google_%22G%22_Logo.svg.png" alt="logo-google"/>
            </picture>
            <span>Registrarse con Google</span>
        </button>
        <button class="twitter-b"> <!-- twitter -->
            <picture>
                <img src="https://upload.wikimedia.org/wikipedia/fr/thumb/c/c8/Twitter_Bird.svg/1200px-Twitter_Bird.svg.png" alt="logo-twitter"/>
            </picture>
        </button>
    </div>
    <div class="separator"> <!-- la línea separadora -->
        <hr/>
        <span>Or</span>
        <hr/>
    </div>
    <form action="" method=""> <!-- formulario para registrarse -->
        <div class="section-inputs">
            <label for="name"> <!-- nombre -->
                <span>Name</span>
                <input id="name" name="name"/>
            </label>
            <label for="username"> <!-- usuario -->
                <span>Username</span>
                <input id="username" name="username"/>
            </label>
        </div>
        <label for="email"> <!-- email -->
            <span>Email</span>
            <input id="email" name="email"/>
        </label>
        <label for="password"> <!-- contraseña -->
            <span>Password</span>
            <input id="password" name="password" placeholder="6+ characters"/>
        </label>
        <label for="checkbox" class="checkbox-label"> <!-- aceptar términos -->
            <input type="checkbox" id="checkbox"/>
            <span>Acepto las condiciones y el aviso legal</span>
        </label>
        <!-- enviar los resultados del formulario: -->
        <button type="submit" class="submit-btn">Crear cuenta</button>
    </form>
</div>
```

<br>

El código CSS en este caso es bastante más largo, por lo que si deseas verlo completo, puedes hacerlo desde [aquí](./2-formulario/css/login.css).

En cualquier caso, este es el resultado:

![2-fomulario](https://user-images.githubusercontent.com/110897750/209569324-88a26ddd-8711-4bd1-ba0e-6d39fca44cf9.jpg)

<sub>[Ver código](./2-formulario/) | [Volver al índice](#indice)</sub>


<br><hr>
<hr><br>


## Formulario 2

En este tercer apartado, se muestra un ejemplo más sobre cómo podría ser un formulario.

Este es el código HTML:

```html
<div class="page-container">
    <div class="contact-grid-wrapper">
        <div class="company-metadata-sidebar-wrapper">
            <div class="logo">
                <img src="./img/logo.png" alt="logo">
            </div>

            <div class="company-details-wrapper">
                <i class="fa-solid fa-location-dot"></i>
                <div>
                    123 Any St<br>Scottsdale, AZ, 85251
                </div>
            </div>
            <div class="company-details-wrapper">
                <i class="fa-solid fa-phone-volume"></i>
                <div>
                    555 555 5555
                </div>
            </div>
            <div class="company-details-wrapper">
                <i class="fa-regular fa-clock"></i>
                <div>
                    10 AM - MIDNIGHT
                </div>
            </div>
        </div>

        <div class="form">
            <div class="form-group">
                <input type="text" id="fullName" placeholder="Your name">
                <label for="fullName">Your name</label>
            </div>
            <div class="form-group">
                <input type="email" id="email" placeholder="Email">
                <label for="email">Email</label>
            </div>
            <div class="form-group">
                <textarea name="message" id="message" placeholder="Some message..."></textarea>
                <label for="message">Message</label>
            </div>
            <div class="spacer10"></div>
            <div class="centered-btn-wrapper">
                <button type="submit" class="btn">Send</button>
            </div>
        </div>
    </div>
</div>
```

<br>

El código CSS en este caso es bastante más largo, por lo que si deseas verlo completo, puedes hacerlo desde [aquí](./3-formulario/styles.css).

En cualquier caso, este es el resultado:

![3-fromulario](https://user-images.githubusercontent.com/110897750/209569326-1ef33f8b-c265-40d4-9a30-7fdf1454270e.jpg)

<sub>[Ver código](./3-formulario/) | [Volver al índice](#indice)</sub>


<br><hr>
<hr><br>


[<< TEMA 6](../06-Selectores/README.md#selectores-pseudoclases-y-pseudoelementos) | [INICIO](../../README.md#temario-del-curso---teoria)