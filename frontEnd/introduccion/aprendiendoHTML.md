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

## Como funciona HTML

HTM funciona como una estructura de árbol nosotros tenemos un nodo principal y de allí se pueden agregar mas nodos.

![arbolEstructura](/frontEnd/imagenes/arbolEstructura.png)

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

![estructuraHTML](/frontEnd/imagenes/estructuraHTML.png)

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

## Etiquetas HTML

+ `<!DOCTYPE html>`
    - Indica al explorador web que el contenido es de tipo html5
    > *si la eliminamos entrara en Quirks mode, años 90, código antiguo y errores*

+ `<html></html>`
    - Es la etiqueta raíz de todo documento HTML

+ `<head></head>`
    - Dentro de esta etiqueta se agregan más características como, titulo o metadatos.

+ `<title>Titulo</title>`
    - Especifica el titulo para una pagina HTML

+ `<body></body>`
    - Aquí se incluye todo el contenido visible de nuestra pagina web.
    - es un contenedor para todos los contenidos visibles

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
    > *Con la propiedad **target="_blank"** se abre en una nueva pestaña el hipervínculo*

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



