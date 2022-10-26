# Primeros pasos Figma

Aprenderé Figma de manera autónoma a traves de videos, cursos y documentación, ademas los listare a continuación:

> Curso de https://leonidasesteban.com 
> Nombre: Curso de Figma para frontEnd

link de Figma: https://www.figma.com/

En este curso no aprenderé a diseñar, sino a utilizar las herramientas que la plataforma nos ofrece para Frontend e interpretar diseños.

Agradezco a Leonidas Esteban por brindar estos cursos gratuitos en los cuales puedo aprender.

## Duplicar proyectos

Teniendo un archivo de figma podemos importarlo ya sea en la aplicación o en el sitio web.

## Selección de elementos

Se puede saber las propiedades de un elemento en figma se lo seleccionamos, inclusive nos brinda un aproximado de como se vería en código CSS los elementos, sin embargo, no se debe seguir al pie de la letra ya que los tamaños y propiedades puede variar o diferir de la implantación en código.

> *Es importante tener una comunicación con el equipo de diseño y no solo hacer cambios o seguir el diseño tal cual*

> *En el mundo de CSS existen más matemáticas que buen gusto*

## Margenes

Seleccionando un elemento podemos saber las medidas en pixeles de la distancia de los elementos con respecto a otros.

Selección especifica con 

- `ctrl+clickIzq`

## Exportar Assets

Es importante ver el tamano del elemento que exportemos

> *Exportar imágenes transparentes serian png o svg (si es imagen por dentro la imagen la pondrá en base64)*

> *svg es recomendable para iconos*

> *Es mejor exportar el icono o vector junto con la caja/contenedor que contiene el vector, ay que es realmente donde obtiene las propiedades*

> *Para mover componentes hago click derecho sobre el componente que deseo mover, selecciono la opción (Move to page), elijo la pagina donde lo quiero envíar.*

> *Justo estuve en una charla ayer sobre UI-UX y mencionaron esto: Cuando estén comenzando lo mejor para su flujo de trabajo es, primero, identifiquen donde y para que se va a usar su diseño (UX), de ahí busquen referencias de diseños ya hechos relacionados a su tema y con esas referencias ya hechas, van a identificar sus componentes-elementos, pregúntense ¿Por qué están ahí?. Para las referencias recomendaron figma Community(https://www.figma.com/community/explore), son proyectos open-source que puedes usar sin ningún problema.*


## Componentes

+ Los componentes son una capa o un grupo de capas que podemos reutilizar en nuestro diseño. Por ejemplo:
- El pie de página —que normalmente se repite en todas las páginas de una web—
- Iconos que podemos volver a utilizar.

> *Los componentes se distinguen por el icono de rombo compuesto por 4 rombos en morado*

+ Las instancias son objetos derivado de los componentes, copia sus propiedades sin modificar el componente base.

> *Las instancias se identifican con rombo morado vació*

> *La ventaja de los componentes es que una vez que los tienes creados, si modificas una propiedad del componente principal, se modifica "automágicamente" esa propiedad en todas las instancias que hayas creado.*

## Desing System

Todo debe estar documentado.

Se puede crear estilos los cuales no estén documentados y agregarlos, para posteriormente agregarlos a variables CSS

## Grids Figma

Los grid nos dan la guía de donde deben ir nuestro elementos

Los grids se diseñan.

> ***El tamaño 1366px (1920px fullhd) es un area muy común en laptop osea pantalla, mientras que en mobiles es de 360px***

El grid nos dice también las fronteras/contenedores de nuestro diseño.

> ***Un estándar de columnas de grind son 12 columnas y su tamaña seria múltiplo de 16 (16+1.4)***

> ***El area legible para trabajar es de 1110***

## Auto Layout, grupos y frames

Modulo mas potente de Figma (modulo flexbox de CSS)

Se pueden agregar a flexbox y tener una mejor organización