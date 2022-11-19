---
title: "aprendiendo HTML"
author: "Ibrain Rodriguez Espinoza"
---
## Primeros pasos en HTML

Estaré subiendo mi aprendizaje de HTMl, los recursos los listare a continuación:

> Iniciare con el curso de Introducción al desarrollo web de Leonidas Esteban

## ¿Qué es html?

Por sus siglas en ingles Hypertext Markup Language o **lenguaje de marcado de hipertexto**, hace referencia al lenguaje de marcado para la elaboración de paginas web.

> *Un lenguaje de marcado maneja etiquetas y representan diferentes cosas como: links, párrafos, video, texto, imagen, etc.*
> *Lenguaje para desarrollar HTML*
> *Indica al explorar qué y como mostrarlo*
> *Es un estándar que sirve de referencias para la elaboración de paginas web y esta a cargo del W3C (World Wide Web Consortium)*
> *index.html se busca como archivo base que se abre por defecto en el navegador*
> *HTML describe la estructura de una página Web*
> *HTML describe la estructura de una página Web, no esta especializado en el diseño*

## Como funciona HTML

HTM funciona como una estructura de árbol nosotros tenemos un nodo principal y de allí se pueden agregar mas nodos.

<img src="/frontEnd/imagenes/arbolEstructura.png" alt="Estructura de árbol html" style="width: 400px;max-width: 100%;">

### DOM

El DOM (Document Object Model) es prácticamente esa estructura de árbol que representara a nuestros proyectos web, es decir la representación jerárquica de los elementos en html en un documento.

```html
<!DOCTYPE html>
<html>
    <head>
        <mate charest="utf-8" />
        <title>Hello world!</title>
    </head>
    <body>
        <h1>Hola mundo!, titulo</h1>
        <section>
        <p>Hola mundo!, párrafo</p>
        <p>Hola mundo!, párrafo 2</p>
        </section>    
    </body>
</html>
```
## ¿Qué es una etiqueta?

Una etiqueta son "códigos" que permiten crear elementos HTML

Nos ayudan a brindar una estructura y semántica al contenido de nuestra pagina web  

Una etiqueta consta de 3 partes
- apertura
- contenido
- cierre

```html
<soy-una-etiqueta>
    Contenido de la etiqueta
</soy-una-etiqueta>
```

## Estructura de HTML

<img src="/frontEnd/imagenes/estructuraHTML.png" alt="Estructura de html" style="width: 400px;max-width: 100%;">

```html
<!DOCTYPE html>
<html>
    <head>
        <title>Hello world!</title>
    </head>
    <body>
        <h1>Hola mundo!, titulo</h1>
        <section>
        <p>Hola mundo!, párrafo</p>
        </section>    
    </body>
</html>
```

- head, va los metadatos, datos que no vera el usuario
- dody, va el contenido que sera visible para el usuario.

## Estructura básica de HTML en una página Web

<img src="/frontEnd/imagenes/estructuraBasicaPagina.webp" alt="Estructura de una pagina web" style="width: 400px;max-width: 100%;">

- Container: contenedor principal
- Header: cabecera de la página. Aquí usualmente encuentras el logo y el menú de navegación del sitio.
- Main content: estructura principal. Por ejemplo, el feed o lista de publicaciones de una red social.
- Sidebar: contenido secundario de una página, que usualmente se encuentra a los lados del contenido principal (o main).
- Footer: pie de página. Esto se encuentra al fondo del sitio web, salvo en casos de sitios web donde el scroll (o navegación hacia abajo) es infinito, por ende, no tendría sentido ponerlo al fondo.

## Etiquetas HTML

+ Existen 2 tipos de etiquetas:
    - Contenedoras
    - De contenido

+ `<!DOCTYPE html>`
    - Indica al explorador web que el contenido es de tipo html5
    > *si la eliminamos entrara en Quirks mode, años 90, código antiguo y errores*

+ `<html></html>`
    - Es la etiqueta raíz de todo documento HTML
    - Atributos:
        * lang="es_MX" - indica al navegador el lenguaje de la pagina   

+ `<head></head>`
    - Dentro de esta etiqueta se agregan más características como, titulo, css, js, metadatos.

    - `<title>Titulo</title>`
        * Especifica el titulo para una pagina HTML
    - `<meta charset="UTF-8">`
        * Para caracteres especiales del idioma y emojis
    - `<meta name="description" content="Esta pagina es un blog">`
        * Para agregar una descripción del sitio web ayuda a que usuario entienda de que es la pagina
    - `<meta name="viewport" content="width=device-width, initial-scale=1.0">`
        * Si el proyecto se abre desde una dispositivo mobile se ve mejor la letra

+ `<body></body>`
    - Aquí se incluye todo el contenido visible de nuestra pagina web.
    - Es un contenedor para todos los contenidos visibles

+ `<h1> Hola </h1>`
    - Encabezado
    > *El encabezado va desde el h1 hasta el h6, solo títulos y subtítulos*

+ `<p> Hola </p>`
    - Párrafo:
    - si quieres agregar párrafos separados debes agregar otra etiqueta p.

+ `<hr></hr>`
    - agrega una linea para separar texto o secciones

+ `<!-- -->`
    - Esta es la etiqueta de comentario

+ `<spam></spam>`
    - Nos sirve para referenciar silenciosamente texto dentro de otras etiquetas

+ `<br>`
    - Agrega un salto de linea o un espaciado

+ `<a href="direccion">ir a link</a>`
    - la etiqueta ancore se usa para insertar hipervínculos, a sitios externos o internos
    > *Con la propiedad **target="_blank"** se abre en una nueva pestaña el hipervínculo.*
    > ***href="mailto:ibrain@correo.com"*** abre una ventana del cliente de correo para enviar un mail. 
    > ***href="#idelemento"*** envía a el elemento con ese id

+ `<img></img> o <img />`
    - mostrar imágenes al usuario

+ `<video src="direccion">  </video>`
    - Video

+ `<form></form>`

```html
<form id="formulario" action="/registrar" method="POST"> 
    <label for="nameForm">Nombre</label>
    <input id="nameForm" name="nameForm" placeholder="Nombre" />
    <label for="edadForm">Edad</label>
    <input type="" id="edadForm" name="edadForm" placeholder="Edad" />
    <br>
    <label for="comentario">Comentario</label>
    <textarea rows="10" cols="20" id="comentario" name="comentario" placeholder="Inserte un comentario"></textarea>
    <br>
    <button type="submit">Registrar</button>
</form>
```
- Nos sirve para agregar un formulario
- label e input son etiqueta y métodos de entrada respectivamente
- etiqueta ***name*** es la llave y lo que escriba en el input es el valor de la llave, es decir, nombreForm=Eduardo Sabala
- Propiedad ***value*** es para asignar valor por defecto
- Métodos de envió de datos en formulario:
    - GET
    - POST
- Propiedad ***type*** sirve para que input se comporte de manera diferente dependiendo de la propiedad de type
    * Valores de type:
        - summit-boton
        - text-texto
        - email
        - password
        - radio-boton radio
        - checkbox-maradorcheck
        - file-selesccionar archivo

+ `<ul><li></li></ul>`

    - Agrega una lista no ordenada

+ `<ol><li></li></ol>`

    - Agrega una lista ordenada
    > *Con value asignas el numero de comienzo de una lista*
    - anidar listas>
        * ```html
            <ol>
                <li>Elemento 1</li>
                <li>Elemento 2</li>
                <li>Elemento 3</li>
                <li>Elemento 4
                    <ol style="list-style-type:lower-latin;">
                        <li>Subelemento 1</li>
                        <li>Subelemento 2</li>
                        <li>Subelemento 3</li>
                    </ol>
                </li>
            </ol>
        ```
+ Agregar tabla:

    - ```html
        <table style="width: 500px;">
            <thead>
                <tr>
                    <th>Producto</th>
                    <th>Precio</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>Jamón</td>
                    <td>Gratis</td>
                </tr>
                <tr>
                    <td>Piña</td>
                    <td>Gratis</td>
                </tr>
                <tr>
                    <td>lechón al horno bañado en salsa negra</td>
                    <td>19,99</td>
                </tr>
            </tbody>
            <tfoot>
                <td></td>
                <td>Total: 19,99</td>
            </tfoot>
        </table>
    ```
+ `<header></header>`

    - Puede contener algunos elementos de encabezado, así como también un logo o un menu

+ `<footer></footer>`
    
    - La etiqueta define un pie de página para un documento o sección.
    - Normalmente contiene:
        * Información de autoría
        * Información sobre derechos de autor
        * Información de contacto
        * mapa del sitio
        * volver al principio enlaces
        * Documentos relacionados

+ `<section></section>`

    - Representa una sección genérica de un documento. Sirve para determinar qué contenido corresponde a qué parte de un esquema.

+ `<div></div>`

    - Representa una sección genérica de un documento. Sirve para determinar qué contenido corresponde a qué parte de un esquema. **Ya no se utiliza mucho** 
    - solo dejar un div si esta anidado y no tienen clases.

+ `<article></article>`

    - Se utiliza para definir contenido independiente, ejemplo post de un articulo, enmarcar publicación o imagen(de Facebook, twitter, Instagram)

## Atributos

+ id="nombreElemento"

    - Se utiliza para identificar a un elementos especifico
    > *Los id no se deben repetir entre elementos*

+  class="nombreDeConjuntoDeElementos"

    - Se utiliza para identificar a **más** de un elemento (o agruparlos). 

> ***Estos elementos id y class nos sirven para identificar elementos para posteriormente ser seleccionados con CSS o JS***

## Entidades HTML

+ Agregar tildes:
    
    - `&<letra>acute` ejemplos: `&iacute` 

