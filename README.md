# Frontend-Developer
Escuela JS- Curso Platzi
# TABLA DE CONTENIDO
- [¿Qué son y para qué nos sirven HTML y CSS?](#¿Qué-son-y-para-qué-nos-sirven-HTML-y-CSS?)
- [DOM, CSSOM, Render Tree y proceso renderizado Web](#DOM,-CSSOM,-Render-Tree-y-proceso-renderizado-Web)
- [Conceptos iniciales de HTML](#Conceptos-iniciales-de-HTML) 
- [](#)
- [](#)
- [](#) 
- [](#) 
- [](#)
- [](#)
- [](#) 
- [](#)
- [](#)
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
  
