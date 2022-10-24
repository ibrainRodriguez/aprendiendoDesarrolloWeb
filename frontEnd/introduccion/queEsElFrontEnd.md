### ¿Que es FrontEnd?

Cuando hablamos de front nos referimos a la parte de "en frente" de las aplicaciones web, es decir la parte en la que interactúan y visualizan los usuarios.

En el FrontEnd construimos todo el diseño del sitio, desde la estructura, el acomodo, la distribución de contenido, los estilos que se muestran y los flujos que interactúan con los usuarios.

### El usuario

El FrontEnd estará enfocado al usuario, ya que:

> *Esta es la parte que se visualiza en el navegador y es la que manda toda la información al Backend para ser procesada.* 

Por ello existen ***UI/UX*** el cual se refiere a User Interface y User Experience, ***SIEMPRE*** se tienen que realizar antes de empezar a programar.

**estética y utilidad**

> *Se debe hacer una investigación para conocer a los usuarios que utilizaran la aplicación.*

### Patrones de arquitectura de desarrollo Web

#### MVC (Model View Controller)

Uno de los patrones de diseño web más utilizados/seguros y con el cual podremos tener muchísimo más claro el funcionamiento de todo el FrontEnd, la parte a la que nos referimos para el Front es la parte de la "Vista".

MVC se usa inicialmente en sistemas donde se requiere el uso de interfaces de usuario, aunque puede ser utilizado en distintos tipos de aplicaciones.

Su fundamento es la separación del código en tres capas diferentes *Model, Views & Controllers*:
+ View:
* Define las interfaces de usuario
+ Controllers
* Contienen diferentes tipos de lógica
+ Model
* Backend, Define estructura de datos

> *Así como este patrón de diseño arquitectónico existen algunos otros como MVM (Model View View Model), MVP (Model View Presenter), RMR (Resource Method Representation) y se recomienda que utilices el que sea mejor para tu aplicación.*

### SDLC (Software Development Life Cycle)

El Ciclo de Vida del desarrollo de software es parte fundamental al momento de hacer una aplicación, ya que las fases de este modelo harán que el desarrollo sea mucho mas controlado, escalable y mantenible.

Las faces de este modelo son las siguientes:
- Fase 1: Requerimientos --> Fase donde se presentan las necesidades de la aplicación.
- Fase 2: Diseño --> En esta fase los requerimientos se convierten en un plan y en lo que debería de parecer la aplicación o producto final.
- Fase 3: Desarrollo --> En esta fase se hace la programación de las aplicaciones, aquí es donde metemos el código con las mejores prácticas y con las reglas de las guías de desarrollo seguro.
- Fase 4: Verificación --> En esta fase revisarás y confirmarás que las buenas prácticas se aplicaron en el código. En esta parte se integran las pruebas de CI/CD e integración de pruebas unitarias.
- Fase 5: Mantenimiento y evaluación --> Los sistemas son un ente vivo y por lo tanto tiene que mantenerse en continuo movimiento.

### ¿Qué tecnologías se usan en FrontEnd?

El FrontEnd tiene muchísimos sabores y existen cientos de formas de hacer que tengas una página o aplicación web.

En mi caso, por el cuso que estoy tomando por parte de INNOVACCION y para comenzar en este mundo del desarrollo web utilizare HTML, CSS y JS

+ ### HTML
* Este lenguaje nos permite tener el "esqueleto" de nuestra aplicación, es lo que define la estructura del sitio y lo que nos da la pauta y el inicio de nuestra aplicación web.
+ ### CSS
* Este lenguaje nos da la posibilidad de estilizar y de insertarle toda la parte de visual y estética a tu sitio como si fuera la "piel" de nuestra aplicación. Se utilizan clases y selectores para poder definir las propiedades y características de cada uno de los elementos que nosotros definamos en la aplicación web.
+ ### JavaScript
* Es el "cerebro" de nuestra plataforma, una vez que nosotros utilizamos JS en el sitio le damos la capacidad de escalar las funcionalidades de forma exponencial, ya que pasamos de las propiedades que tienen las etiquetas (Que también tienen algo de JS) a tener una cantidad virtualmente infinita de posibilidades.Podemos considerar a JS como el sistema nervioso que controla toda nuestra aplicación web y la que manejará todos los músculos y huesos de nuestro sitio.

### Frameworks

Un framework es el esquema o estructura que se establece y que se aprovecha para desarrollar y organizar un software determinado

Ahora bien existen diversos frameworks variantes de JS que nos ayudan a que nuestra programación sea mucho mas rápida y/o nos ofrecen funcionalidades adicionales.

El hecho de que un Framework te permita programar de forma más sencilla NO SIGNIFICA que puedes saltarte toda la parte fundamental de JS, esto es porque al ser la base de muchos de los Frameworks web, es bastante útil conocer como funciona desde el fondo.

Algunos de los frameworks de JS para FrontEnd mas famosos son:
- React JS
- Vue JS
- Angular
- Ember JS
- entre otros

Mientras que para Backend uno de estos puede ser **NODE JS**.

### Setup de un programador FrontEnd

En cual profesión en la que nos dediquemos necesitaremos utilizar herramientas que nos ayuden a realizar nuestro trabajo.

En caso de la programación web y específicamente del FrontEnd utilizare las siguientes:
- Herramienta de diseño de aplicación
- IDE de programación
- Navegador Web
- Herramienta de documentación

Algunas de las herramientas podrían ser opcionales o en un ámbito profesional podrían ser utilizadas por otras áreas de la empresa, sin embargo, es importante que ustedes las conozcan para que en el flujo operativo de la empresa, su aporte sea mucho más valioso. *Es decir que launch x propone la utilización de estas herramientas para tener el conocimiento del flujo operacional de una empresa*.

#### Herramienta de diseño

Esta herramienta es la que nos da la capacidad de tener un prototipo de la aplicación sin poner NI UNA línea de código.

En el flujo de programación, basándonos en el SDLC (Software Development Life Cycle) siempre es necesario empezar con el diseño de la solución antes de irnos a la parte de la programación, ya que en caso de presentarse un cambio o modificación es mucho más fácil y rápido cambiarla en el lado de diseño que volver a programar el módulo completo.

> El diseño tiene como objetivo poder aterrizar los requerimientos de quien nos esté pidiendo el software y para eso existen diferentes técnicas como por ejemplo: Desing Thinking, Visual Thinking, diagramas de flujo, o la que mejor se te acomode para poder entender lo más cercano posible a lo que tu cliente esté pidiendo.

Existen muchas herramientas de diseño como:
- Paint
- Canva
- Photoshop
- Illustrator
- Pusblisher
- entre otros

**No obstante deberíamos usar herramientas especializadas y enfocadas al diseño de wireframes e interfaces gráficas**

En la fase de diseño de **flujo y de WireFrame**, lo que haremos en esta fase es entender las necesidades y empezar a dibujar como funciona la aplicación sin darle diseño gráfico aún, esta es una fase completamente funcional para darnos cuenta de las interacciones, los botones necesarios, el número de clicks y los diferentes movimientos de la aplicación y nos dará muchísima información para que nuestra aplicación sea lo más fluida posible.

+ Para esta fase de flujos y Wireframe existen herramientas como las siguientes:

* Miro (https://miro.com/es/) Esta herramienta te permitirá crear flujos de información y flujos de negocio.
* Balsamic mockups (https://balsamiq.com/wireframes/) Nos da elementos para poder crear interfaces rápidas y que nos dejan representar la idea.
* Dibujos a mano alzada --> a veces un wireframe también puede ser en una servilleta o en cualquier forma escrita.

Una vez realizado tu wireframe pasaremos a la parte de **UI/UX**, en este momento comenzaremos con toda la parte gráfica, de identidad y de uso de colores, formas e interacciones a lo largo de nuestra aplicación. 

+ Para eso podemos usar cualquiera de las siguientes herramientas:

* Sketch (https://www.sketch.com/) Esta herramienta solo aplica si tienes una computadora MacOS, pero cuenta con una amplia gama de características enfocadas a diseñadores, lo que hace que se puedan crear cosas muy grandes y escalables.

* Figma (https://www.figma.com/) Esta herramienta es gratuita en muchas de sus características y permite colaboración entre usuarios, lo que es muy útil cuando se trabaja en equipo, tanto en equipos de diseño como en equipos de desarrollo.

* Adobe XD (https://www.adobe.com/mx/products/xd.html) Existe su versión de prueba gratuita que te dejará ocupar la herramienta completa para crear todos tus diseños y el costo para tener un plan pro no es muy alto, tiene la ventaja de estar basado en las herramientas de Adobe, por lo que si ya tienes experiencia con alguna de estas herramientas, la curva de aprendizaje podría ser más corta.

#### IDE de programación

Un IDE (Integrated Development Environment) es un software que nos ayuda a los desarrolladores a poder construir aplicaciones de forma más sencilla, esto es porque combina diferentes herramientas de desarrollo en una sola interfaz gráfica. Algunas de estas herramientas son:

- Editor de código.
- Automatización.
- Depuración.
- Integración.

Existen muchos IDE pero los más populares son:

- VS Code
- Atom
- Sublime Text

#### Navegador web

Al ser programadores web todo lo que programemos se desplegará en un navegador web, aquí hay que tener mucho cuidado y revisar que la tecnología que estemos utilizando es compatible y se despliega de forma igual o similar en todos los navegadores.

No obstante debemos siempre revisar la compatibilidad. Para eso existen plataformas como:

- "Can I use" https://caniuse.com/ - la cual nos dice en que navegadores podemos utilizar la tecnología de HTML, CSS y JS que queramos utilizar.

#### Developer tool

Son herramientas que nod darán información adicional sobre nuestra aplicación y mejoras que podemos implementar, como:

- Lighthouse de Google (https://developers.google.com/web/tools/lighthouse?hl=es)
-  axe DevTools (https://www.deque.com/axe/devtools/) ayuda a personas ciegas o de debilidad visual.

#### Documentación

Una de las fallas más grandes que me ha tocado ver a lo largo de mi carrera es que no se documentan los desarrollos. ya que en caso de que se cambie de desarrollador o de que sea un programa que tiene mucho tiempo que no mueves, necesitas conocer y entender como fue desarrollado.

La falta de documentación hace que la mantenibilidad del código sea mucho más complicada y que muchas veces se tenga que reprogramar los módulos ya que en promedio si no usas el código en aproximadamente 6 meses, dejarás de comprender su funcionalidad.

existen librerías como:
-  API Doc (https://apidocjs.com/)
- rails Admin (https://github.com/railsadminteam/rails_admin)

Lo que es importante considerar al momento de documentar tu código es lo siguiente:

Definir tu audiencia: A quien va a ir dirigida tu documentación, si es para otros desarrolladores, de que nivel o si es para alguien administrativo o si incluso es para ti mismo en un futuro.
Qué problemática soluciona tu código: Todo lo que programamos tiene una funcionalidad por módulo y necesitamos definir que parte de la aplicación afecta, en que forma y cuales son las opciones de entrada y salida de nuestras funciones.
Estructura de aplicación: Cuando documentamos todo un proyecto tendremos diferentes secciones, funcionalidades, páginas o incluso otros sitios que se conecten al nuestro, para esto es recomendable documentar desde lo más general a lo particular, un ejemplo muy bueno lo podemos encontrar en la documentación de Firebase (https://firebase.google.com/docs/build)

### GIT

Como parte de mi aprendizaje empezare este camino aprendiendo Git para tener un control de las versiones de mis proyectos, contar con un respaldo de mis archivos y lo más importante la creación de mi portafolio.

> [Aprendiendo GIt](aprendiendoGit.md)