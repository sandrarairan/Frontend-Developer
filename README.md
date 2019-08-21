# Frontend-Developer
Escuela JS- Curso Platzi
# TABLA DE CONTENIDO
- [¿Qué son y para qué nos sirven HTML y CSS?](#¿Qué-son-y-para-qué-nos-sirven-HTML-y-CSS?)
- [DOM, CSSOM, Render Tree y proceso renderizado Web](#DOM,-CSSOM,-Render-Tree-y-proceso-renderizado-Web)
- [Conceptos iniciales de HTML](#Conceptos-iniciales-de-HTML) 
- [Conceptos iniciales de CSS](#Conceptos-iniciales-de-CSS)
- [Modelo de caja](#Modelo-de-caja)
- [Valores relativos y absolutos](#Valores-relativos-y-absolutos) 
- [Arquitectura CSS](#Arquitectura-CSS) 
- [Construcción de componentes](#Construcción-de-componentes)
- [Maquetación y diseño responsivo](#Maquetación-y-diseño-responsivo)
- [](#) 
- [](#)
- [](#)
- [](#)
- [](#) 
- [](#)
- [](#)**
<!-- toc -->
## ¿Qué son y para qué nos sirven HTML y CSS?
HTML: Es un lenguaje de marcado usado para decirle a tu navegador cómo estructurar las páginas web que visitas. No es un lenguaje de programación.

CSS: Es un lenguaje que nos permite crear páginas web con un diseño agradable para los usuarios. Tampoco es un lenguaje de programación.

https://htmlreference.io/
https://cssreference.io/

## DOM, CSSOM, Render Tree y proceso renderizado Web
DOM: Document Object Model. Es una transformación del código HTML escrito por nosotros a objetos entendibles para el navegador.

CSSOM: así como el DOM para el HTML, EL CSSOM es una representación de objetos de nuestros estilos en CSS.

Render Tree: es la unión entre el DOM y el CSSOM para renderizar todo el código de nuestra página web.

Pasos que sigue el navegador para construir las páginas web:

Procesa el HTML para construir el DOM.
Procesa el CSS para construir el CSSOM.
El DOM se une con el CSSOM para crear el Render Tree.
Se aplican los estilos CSS en el Render Tree.
Se ““pintan”” los nodos en la pantalla para que los usuarios vean el contenido de la página web.

## Conceptos iniciales de HTML

**Anatomía de un Elemento HTML: Atributos, Anidamiento y Elementos vacíos
Nuestros elementos HTML se componen de:**

Etiqueta de apertura: el nombre de nuestra etiqueta encerrado entre símbolos de mayor o menor. Por ejemplo: <h1>.
Contenido: dentro de nuestras etiquetas podemos añadir texto u otros elementos HTML, lo que conocemos como anidamiento.
Etiqueta de cierre: son casi iguales que las etiquetas de cierre, pero también necesitan un slash (\) antes del nombre de la etiqueta. Por ejemplo: </h1>.
Las etiquetas de apertura también pueden tener atributos. Los atributos nos permiten definir características especiales para nuestros elementos: <etiqueta atributo=""valor del atributo"">. Por ejemplo: <h1 class=""saludo"">.

También existen elementos vacíos. Estos elementos no tienen contenido ni etiqueta de cierre, solo etiqueta de apertura y atributos. Por ejemplo: ```<img src=""puppy.png"" alt=""mi mascota"">.```

**Anatomía de un Documento HTML: DOCTYPE, html, head y body**

```<!DOCTYPE html> <!-- El Documento sea analizado de la misma forma en los difrentes navegadores -->
                    <html lang="en"><!-- La etiqueta html es root -->
                    <head>
                        <meta charset="UTF-8">
                        <meta name="viewport" content="width=device-width, initial-scale=1.0">
                        <meta http-equiv="X-UA-Compatible" content="ie=edge">
                        <title>Document</title>
                    </head>
                    <body>
                        <h1>Esta es mi primera etiqueta html</h1>
                        <div>
                            <p>Estoy muy feliz</p>
                        </div>
                    </body>
                    </html>
  ```
  
**La importancia del código semántico**
Es importante que como desarrolladores tengamos claro el significado de escribir código. Debes ser consciente de que la manera en la que codeas tenga sentido.

La semántica HTML no es más que darle sentido y estructura a lo que estas escribiendo. Muy importante para el navegador. No todos los elementos deberían ser un div.

```<body>
	<header>
		<nav></nav>
		<aside></aside>
	</header>
	<main>
		<section>
			<article> ... </article>
		</section>
	</main>
	<footer></footer>
</body>
```

**Tipos de errores en HTML, debugging y servicio de validación de etiquetas**
Errores sintácticos: Son errores de escritura en el código y evitan que el programa funcione. Pueden ser errores de tipado.

Errores lógicos: En estos la sintaxis es correcta, pero el código no hace lo que debería. El programa funciona, pero de forma incorrecta.
-En esta página se colcoa el coódigo para validar si tiene errores:
https://validator.w3.org/

## Conceptos iniciales de CSS

**Anatomía de una declaración CSS: Selectores, Propiedades y Valores
Nuestros estilos con CSS se componen de:**

Selector: son la referencia a los elementos HTML que queremos estilizar. Los nombres de estas etiquetas van seguidas de una llave de apertura y otra de cierre ({}). Por ejemplo: h1 {}.
Propiedades: son el tipo de estilo que queremos darle a nuestros elementos. Van seguidas de dos puntos (:). Las propiedades deben estar dentro de las llaves del selector que definimos anteriormente. Podemos escribir diferentes propiedades en un mismo selector. Por ejemplo: h1 { color: }.
Valores: son el estilo que queremos que tomen nuestros elementos HTML con respecto a una propiedad. Van seguidas de un punto y coma (;). Por ejemplo: h1 { color: red; }.
h1 {
  color: red;
}

**Tipos de selectores, pseudo-clases y pseudo-elementos**
*(asterisco): Es el selector universal. Las propiedades se aplicaran a todos los elementos de nuestro HTML.

Tipo: Son selectores que se aplican a cierto elemento HTML en específico. Las propiedades se aplicaran a la etiqueta que queremos, por ejemplo p, body, html, div, etc.

Clase: Si nuestras etiqueta de HTML tienen un atributo de class podemos usar ese valor o identificador para que los cambios en el CSS afecten únicamente a ese elemento.

ID: Es similar al anterior, si la etiqueta HTML tiene un ID podemos afectar solo ese elemento.

Las Pseudo-clases y Pseudo-elementos nos permiten ser aún más específicos con qué elemento o partes de nuestros elementos deben recibir los estilos.

Para usarlas debemos definir el selector base (por ejemplo, p) seguido de dos puntos y la pseudo-clase que queremos estilizar (por ejemplo: p:first-child). En el caso de los pseudo-elementos debemos usar el dos puntos 2 veces (p::first-letter).

/* Asterisco (universal) */
* {
  margin: 0;
}

/* Tipo */
h1 {
  color: red;
}

/* Clase */
.saludo {
  font-size: 2em;
}

/* ID */
#id {
  border-radius: 20px;
}

/* Pseudo-clases */
p:first-child {
  color: white;
}

p:last-child {
  color: purple;
}

p:nth-child(2n) {
  color: red;
}
**Pseudo-elementos**
p::first-letter{
color:red
font-size: 20px;

https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes

https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-elements

https://coolsymbol.com/emojis/emoji-for-copy-and-paste.html

**Modelo de caja**
Todos los elementos de HTML tienen un modelo de caja y esta compuesto por cuatro elementos: contenido, padding, border, margin.

```.caja{
        background-color:#b7e778
        width: 20px;
       height: 20px;
       padding: 20px;
       border: 2px solid #be6283;
       box-sizing: boder-box;/*Respeta el width y heith*/
       margin: 10px 20px 30 px 40px;
    }
  ```
    
}

## Valores relativos y absolutos
Los valores absolutos son, por ejemplo, centímetros, milímetros, pixeles y pulgadas. Se llaman de esta forma porque no tienen en cuenta a nadie más, no depende de la medida de otra unidad.

Los valores relativas, llevan este nombre porque depende de otra unidad de medida o elemento. Por ejemplo, porcentajes, vmx, em, entre otros.

Recuerda que podemos darle estilos a etiquetas HTML muy específicas indicando dónde se van a encontrar. Por ejemplo: si queremos darle estilos únicamente a la imagen que está dentro del header, podemos usar el selector css header img { ... }.

**Displays en CSS**
Todos los elementos en CSS son cuadrados o rectángulos y aparte de eso, estos elementos tienen un comportamiento que se define a través de la propiedad display. Los display más comunes y usados son: 
block, inline, inline-block, none, table, flex y grid. Veamos de qué se tratan:

https://css-tricks.com/snippets/css/a-guide-to-flexbox/
https://css-tricks.com/snippets/css/complete-guide-grid/

**Funciones de las propiedades CSS más usadas**
Width
Height
Background
backgroun-color
color
border
border-radius
margin
padding
font-size
opacity
outlet
box-sizing
Transition
animation

**El posicionamiento en CSS** es una de las cosas más importantes, pues establece cómo van a estar ubicados nuestros elementos en la pantalla.

En CSS los elementos se posicionan utilizando las propiedades top (superior), bottom (inferior), left (izquierda) y right (derecha), pero sólo funcionarán si la propiedad position está establecida. Esto quiere decir que si quiero que mi elemento div esté completamente a la derecha, debo escribir en mi CSS lo siguiente:

div { position: absolute: right: 0px; }

La propiedad position tiene 7 valores diferentes: relative, absolute, fixed, sticky, static, initial e inherit. Veremos de qué se tratan:
Position: Relative. position:absolute
position:fixed
Position: sticky
Position:static
Position:initial
Position:inherital

https://developer.mozilla.org/es/docs/Web/CSS/position

## Arquitectura CSS

**¿Qué son y para qué nos sirven las arquitecturas CSS?**
Objetivos de una arquitectura CSS:

Predecible
Reutilizable
Mantenible
Escalable
Buenas Practicas:

Establecer reglas (en equipo)
Explicar estructura base
Establecer estándares de codificación
Evitar largas hojas de estilos
Documentación

**OOCSS, BEM, SMACSS, ITCSS y Atomic Design**
- OOCSS: https://www.smashingmagazine.com/2011/12/an-introduction-to-object-oriented-css-oocss/

```
<style>
.gobalwidth{
width: 100px;
}
.header{
}
.footer{
}
</style>
<body>
 <header class="header globalwidth"></header>
 <footer class="footer globalwidth"></footer>
 </body>
 ```
 - BEM: http://getbem.com/introduction/
 
 ```
 <body>
  <header>
    <button class="header__button--red">RED</button>
    <button class="header__button--yellow">YELLOW</button>
  </header>
</body>        

SE MANEJA CON BLOQUE, ELEMENTO Y LEMENTO MODIFICADOR
``` 
- SMACSS: http://smacss.com/
BASE: BOTONES
LAYAOUT
MODULE
STATE
THEME=
SMACSS

- ITCSS:https://www.xfive.co/blog/itcss-scalable-maintainable-css-architecture/

- Atomic Design:http://bradfrost.com/blog/post/atomic-web-design/

## Construcción de componentes

Un componente, tanto en diseño como desarrollo web, es un elemento muy pequeño que tiene la capacidad de ser reutilizado en diferentes partes de una aplicación. Por ejemplo: botones, iconos, cards, entre otras.

https://storybook.js.org/

**Flexbox**
Uno de los trabajos más difíciles en CSS es alinear elementos. Para hacerlo más fácil podemos contar con Flexbox.

Es importante tener presente que tendremos un contenedor y los elementos que queremos organizar dependiendo de nuestras necesidades.
https://darekkay.com/dev/flexbox-cheatsheet.html

https://css-tricks.com/snippets/css/a-guide-to-flexbox/
https://flexboxfroggy.com/#es
Justify-content:
flex-start: Alinea elementos al lado izquierdo del contenedor.
flex-end: Alinea elementos al lado derecho del contenedor.
center: Alinea elementos en el centro del contenedor.
space-between: Muestra elementos con la misma distancia entre ellos.
space-around: Muestra elementos con la misma separación alrededor de ellos.

**Nuestro nuevo sistema de layout: CSS Grid**
Con CSS Grid podemos maquetar todo el layout/estructura general de nuestro sitio para que se adapten a diferentes tamaños de pantalla, lo que conocemos como diseño responsivo.

Al igual que Flebox, tenemos propiedades diferentes, tanto para el contenedor como para los elementos, y podemos usarlos dependiendo de nuestras necesidades.
https://developer.mozilla.org/en-US/docs/Web/CSS/grid

https://labs.jensimmons.com/

**Estructura con HTML y BEM de un menú desplegable**

**Estilizando nuestro menú desplegable con CSS**
https://css-tricks.com/snippets/css/a-guide-to-flexbox/

https://fonts.google.com/
font:muli
``` 
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <link href="https://fonts.googleapis.com/css?family=Muli&display=swap" rel="stylesheet">
  <title>Header</title>
</head>
<style>
  body {
    margin: 0px;
    font-family: 'Muli', sans-serif;
    background-color: #64c4ed;
  }
  header {
    background-color: #207561;
    width: 100%;
    height: 80px;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .header__img {
    width: 200px;
    margin-top: 10px;
    margin-left: 10px;
  }
  .header__menu{
      margin-right: 30px
  }
  .header__menu ul{
      display: none;
      list-style: none;
      padding: 0px;
      position: absolute;
      width: 100px;
      text-align: right;
      margin: 0px 0px 0px -14px;
  }
  .header__menu:hover ul, ul:hover{
    display: block;
  }
  .header__menu li{
    margin: 10px 0px;
  }
  .header__menu li a{
    color: white;
    text-decoration: none;
  }
  .header__menu li a:hover{
    text-decoration: underline;
  }
  .header__menu--profile{
     margin-right: 8px;
     display: flex;
     align-items: center;
  }
  .header__menu--profile img{
      margin-right: 8px;
      color: white;
  }
  .header__menu--profile p{
      margin-right: 0px;
    color: white;
  }
</style>
<body>
  <header class="header">
    <img class="header__img" src="./logo-platzi-video-BW2.png" alt="logo">
    <div class="header__menu">
     <div class="header__menu--profile">
       <img src="./user-icon.png" alt="user">
       <p>Perfil</p>
     </div>
     <ul>
         <li><a href="/">Cuenta</a></li>
         <li><a href="/">Cerrar Sesión</a></li>
     </ul>
    </div>
  </header>
</body>
</html>
```
**Buscador**
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <link href="https://fonts.googleapis.com/css?family=Muli&display=swap" rel="stylesheet">
  <title>Header</title>
</head>
<style>
  body {
    margin: 0px;
    font-family: 'Muli', sans-serif;
    background-color: #ff8a5c;
  }
  header {
    background-color: #207561;
    width: 100%;
    height: 80px;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .header__img {
    width: 200px;
    margin-top: 10px;
    margin-left: 10px;
  }
  .header__menu{
      margin-right: 30px
  }
  .header__menu ul{
      display: none;
      list-style: none;
      padding: 0px;
      position: absolute;
      width: 100px;
      text-align: right;
      margin: 0px 0px 0px -14px;
  }
  .header__menu:hover ul, ul:hover{
    display: block;
  }
  .header__menu li{
    margin: 10px 0px;
  }
  .header__menu li a{
    color: white;
    text-decoration: none;
  }
  .header__menu li a:hover{
    text-decoration: underline;
  }
  .header__menu--profile{
     margin-right: 8px;
     display: flex;
     align-items: center;
  }
  .header__menu--profile img{
      margin-right: 8px;
      color: white;
  }
  .header__menu--profile p{
      margin-right: 0px;
    color: white;
  }
  .main{
    height: 300px;
  }
  .main_title{
    color: white;
    font-size: 25px;
  }
  .input{
    background-color: rgba(255,255,255,0.1);
    border: 2px solid white;
    border-radius: 35px;
    color: white;
    font-family: 'Muli', sans-serif;
    font-size:16px;
    height: 50px;
    padding: 0px 20px;
    width: 70%;
    outline: none;
  }
  ::placeholder{
    color:white;
  }
</style>
<body>
  <header class="header">
    <img class="header__img" src="./logo-platzi-video-BW2.png" alt="logo">
    <div class="header__menu">
     <div class="header__menu--profile">
       <img src="./user-icon.png" alt="user">
       <p>Perfil</p>
     </div>
     <ul>
         <li><a href="/">Cuenta</a></li>
         <li><a href="/">Cerrar Sesión</a></li>
     </ul>
    </div>
  </header>
  <section class="main">
    <h2 class="main_title">¿Qué quieres ver hoy?</h2>
    <input class="input" type="text" placeholder="Buscar...">
  </section>
</body>
</html>
```

**Creación de un carousel de imágenes con CSS: Estructura principal**
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>Carrousel 1</title>
</head>
<style>
  body {
    margin: 0px;
  }
  .carousel {
    width: 100%;
    overflow: scroll;
    padding: 30px;
    position: relative;
  }
  .carousel__container {
    white-space: nowrap;
    margin: 70px 0px;
    padding-bottom: 10px; 
  }
  .carousel__item {
    background-color: palevioletred;
    width: 200px;
    height: 250px;
    border-radius: 20px;
    overflow: hidden;
    margin-right: 10px;
    display: inline-block;
    cursor: pointer;
    transition: 450ms all;
    transform-origin: center left;
  }
  .carousel__item:hover ~ .carousel__item {
    transform: translate3d(100px, 0, 0);
  }
  .carousel__container:hover .carousel__item {
    opacity: 0.3;
  }
  .carousel__container:hover .carousel__item:hover {
    transform: scale(1.5);
    opacity: 1;
  }
</style>
<body>
  <section class="carousel">
    <div class="carousel__container">
      <div class="carousel__item">
      </div>
      <div class="carousel__item">
      </div>
    </div>
  </section>
</body>
</html>
```
**Creación de un carousel de imágenes con CSS: Detalle de cada item**
caruse-2.html
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>Carousel 2</title>
</head>
<style>
  body {
    margin: 0px;
  }
  .carousel {
    width: 100%;
    overflow: scroll;
    padding: 30px;
    position: relative;
  }
  .carousel__container {
    white-space: nowrap;
    margin: 70px 0px;
    padding-bottom: 10px; 
  }
  .carousel-item {
    background-color: palevioletred;
    width: 200px;
    height: 250px;
    border-radius: 20px;
    overflow: hidden;
    margin-right: 10px;
    display: inline-block;
    cursor: pointer;
    transition: 450ms all;
    transform-origin: center left;
    position: relative;
  }
  .carousel-item:hover ~ .carousel-item {
    transform: translate3d(100px, 0, 0);
  }
  .carousel__container:hover .carousel-item {
    opacity: 0.3;
  }
  .carousel__container:hover .carousel-item:hover {
    transform: scale(1.5);
    opacity: 1;
  }
  .carousel-item__img {
    width: 200px;
    height: 250px;
    object-fit: cover;
  }
  .carousel-item__details {
    background: linear-gradient(to top, rgba(0, 0, 0, 0.9) 0%, rgba(0, 0, 0, 0) 100%);
    font-size: 10px;
    opacity: 0;
    transition: 450ms opacity;
    padding: 10px;
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
  }
  .carousel-item__details:hover {
      opacity: 1;
  }
</style>
<body>
  <section class="carousel">
    <div class="carousel__container">
      <div class="carousel-item">
        <img class="carousel-item__img" src="https://images.pexels.com/photos/1438072/pexels-photo-1438072.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940" alt="People">
        <div class="carousel-item__details">
          <div>
            <img src="../iconos/play-icon.png" alt="Play">
            <img src="../iconos/plus-icon1.png" alt="Plus">
          </div>
          <p class="carousel-item__details--title">Título descriptivo</p>
          <p class="carousel-item__details--subtitle">2019 16+ 114 minutos</p>
        </div>
      </div>
      <div class="carousel-item">
      </div>
    </div>
  </section>
</body>
</html>
```
**Visualización de un botón usando storybook para HTML**
https://storybook.js.org/docs/guides/guide-html/

http://localhost:49972/?path=/story/button--with-emoji

## Maquetación y diseño responsivo

**Instalación de SASS y configuración incial
Instalación de SASS con NPM:

npm install -g sass
Si usas Windows puedes usar el gestor de paquetes Chocolatey Package Manager e instalar SASS con el siguiente comando:

choco install sass
Si usas Mac puedes usar Homebrew para instalar SASS con el siguiente comando:

brew install sass/sass/sass

https://github.com/teffcode/sass-workshop

- npm install -g sass
- Al archivo styles.css le renombramos por styles.scss
- ➜  platzivideo git:(master) ✗ pwd
/Users/sandrarairan/Documents/Platzi/Frontend Developed/platzivideo
- ➜  platzivideo git:(master) ✗ sass /Users/sandrarairan/Documents/Platzi/Frontend Developed/platzivideo/iniciar-sesion/styles.sccs /Users/sandrarairan/Documents/Platzi/Frontend Developed/platzivideo/iniciar-sesion/styles.ccs

se crean los archivis scss

**La accesibilidad y nuestra responsabilidad como desarrolladores**
Debemos pensar en esas personas con una discapacidad visual que no tienen la posibilidad de ver lo mismo que la mayoría de nosotros. Estas personas no siempre usan el mouse, sino lectores de pantalla.

Un Lector de Pantalla se encarga de leer toda la aplicación elemento por elemento. Que los lectores de pantalla funcionen es responsabilidad de las y los desarrolladores: debemos tener muy buena semántica, usar las etiquetas y atributos adecuados entre otras.

Lectores de pantalla : NVIDIA
JAWS
VOICEOVER - MAC

**Mejorando la accesibilidad de nuestra página de inicio**
https://support.apple.com/es-lamr/HT202362

https://www.ssa.gov/accessibility/andi/help/install.html

https://developer.mozilla.org/es/docs/Web/HTML/Atributos_Globales/tabindex

