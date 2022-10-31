# Primeros pasos en Git y Github

## Los archivos binarios como imagenes no se deberían agregar a los repositorios.

## En el main solo debería enviarse lo que estamos seguro de que saldrá en producción

Aprenderé Git de manera autónoma a traves de videos, cursos y documentación, ademas los listare a continuación:

> YouTube 
> Canal: HolaMundo, video: Aprende GIT ahora! curso completo GRATIS desde cero
> Canal: Yito on Code, video: Git-GitFlow & Github | Curso práctico utilizando flujo de trabajo (desde cero)

### Apuntes 

Git es el sistema distribuido de control de versiones mas popular.

Usos de Git:

- Historial.
- Almacenar código.
- Trabajar en equipo.
- **Cuando se introdujo un error.**

Git nos permite: 

- Tener un historial completo de todo el código que desarrollemos de una aplicación, a traves de ramas o branch.
- Realizar un callback, es decir, regresar a una version diferente del código.
- Nos permite trabajar nuestro código de manera descentralizada, lo que significa, que cada desarrollador tiene una copia completa del código que se esta trabajando y puede hacer cambios sin que afecte a los demás.

*En este curso utilizaremos git bash para utilizar los comandos de bash*

### Comandos de configuración inicial antes de crear repositorios

+ Ver ayuda:

    - `git -h` 

+ Establecer nombre:

    - `git config --global user.name "nombre"` 
    > *global se utiliza para que la configuración se efectué de manera global y no solo al proyecto*

+ Establecer email:

    - `git config --global user.email email`

+ Establecer que la rama principal sea "main"(esto debido a que github lo toma con ese nombre):

    - `git config --global init.defaultBranch main`

+ Establecer el comando que usaremos para abrir nuestro editor:

    - `git config --global core.editor "code --wait"`

En windows cada vez que utilizamos un salto de linea Windows agrega 2 caracteres especiales
- CR(CARRIAGE RETURN)
- LF(LINE FEED)
En Linux/mac solo se agrega el carácter *LF*, por ello debemos cuando se suba código en github si somos usuarios windows debemos asegurarnos que cuando se suba el código se elimine el carácter ***CR*** y cuando se baje código agregarlo, eso lo logramos con los comandos:

+ Windows
    * `git config --global core.autoclrf true`
+ Linux
    * `git config --global core.autoclrf input`

#### Iniciar git

*primero es ir a la carpeta de nuestro proyecto.*

Ejecutar el comando:

`git init`

> *Este comando crea un area en memoria ram llamada staging*
> *crea el repositorio .git*
> *La  carpeta de .git es siempre ignorada por los repositorios que creamos, no comparte entre desarrolladores y no se envía al servidor central*

#### Agregar repositorio externo 

+ Indicar el servidor remote en el cual guardar los cambios:

    - `git remote add origin "repositorio"`

+ Agregar rama main a un repositorio nuevo:
    
    -`git push -u origin main`

+ Clonar un repositorio remoto a local:

    - `git clone "repositorio"`

+ **Si ya teníamos un repositorio iniciado con README y nos da el problema de historias al hacer pull ejecutamos:**
    - `git pull origin main --allow-unrelated-histories`

+ Ver que repositorio remoto tenemos como vinculado
    - `git remote -v`

### Flujo de trabajo que debemos seguir

![imagenFlujodeTrabajoGit](/frontEnd/imagenes/flujoDeTrabajoGit.jpg)

+ Area Local
    * Working Directory
        - Tenemos los archivos locales, los podemos modificar, agregar o eliminarlos, pero esto no significa que los archivos pasaran a un repositorio instantáneamente.
        - Usaremos un comando para seleccionar los archivos que queremos pasar a la etapa *Stage*:
            - `git add`
            - ***Un archivo se dice que esta tracked o trackeado cuando ejecutamos el comando add y se pasa al staging area o commit y se pasan al repositorio.***
    * Stage/Staging area
        - Es el area en memoria ram donde se almacenan los archivos que están en espera de agregarse al repositorio.
        - Podemos ver el estado de los elementos en stage con el comando:
            - `git status` *-s*
        - Podemos sacar/eliminar elementos que no queremos pasar los archivos al repositorio con:
            - `git rm <archivo>`
        - Podemos recuperar un archivo con el comando:
            - `git restore <archivo>`
        - O bien podemos hacer un commit para pasar los archivos al area de commit o al repositorio local con el comando:
            - `git commit` puede llevar -m para agregar comentario
            - ***cada commit es una nueva version de cambios hacia el repositorio***
    * RepositorioLocal/commitArea
        - La rama tiene un nombre por defecto "main"
        - Se pueden enviar los archivos al repositorio remoto con:
            - `git push`
+ Area Remota
    * Repositorio Remoto
        - Se pueden sacar los commit con:
            - `git pull`

### Flujo de trabajo estándar

Para poder desarrollar software de manera óptima y ordenada, necesitamos tener un flujo de trabajo profesional, que nos permita trabajar en conjunto sin interrumpir el trabajo de otros desarrolladores. Una buena práctica de flujo de trabajo sería la siguiente:

- Crear ramas
- Asignar una rama a cada programador
- El programador baja el repositorio con `git    pull origin master`
- El programador cambia de rama
- El programador trabaja en esa rama y hace commits
- El programador sube su trabajo con `git push origin #nombre_rama`
- El encargado de organizar el proyecto baja, revisa y unifica todos los cambios

## Flujo de trabajo profesional de con Pull requests

Es una funcionalidad de github (en gitlab llamada merge request y en bitbucket push request), en la que un colaborador pide que revisen sus cambios antes de hacer merge a una rama, normalmente master.

Al hacer un pull request se genera una conversación que pueden seguir los demás usuarios del repositorio, así como autorizar y rechazar los cambios.

+ El flujo del pull request es el siguiente

    - Se trabaja en una rama paralela los cambios que se desean (git checkout -b <rama>)
    - Se hace un commit a la rama (git commit -am '<Comentario>')
    - Se suben al remoto los cambios (git push origin <rama>)
    - En GitHub se hace el pull request comparando la rama master con la rama del fix.
    - Uno, o varios colaboradores revisan que el código sea correcto y dan feedback (en el chat del pull request)
    - El colaborador hace los cambios que desea en la rama y lo vuelve a subir al remoto (automáticamente jala la historia de los cambios que se hagan en la rama, en remoto)
    - Se aceptan los cambios en GitHub
    - Se hace merge a master desde GitHub
    - Importante: Cuando se modifica una rama, también se modifica el pull request.


En un entorno profesional normalmente se bloquea la rama master, y para enviar código a dicha rama pasa por un code review y luego de su aprobación se unen códigos con los llamados merge request.

Para realizar pruebas enviamos el código a servidores que normalmente los llamamos staging develop (servidores de pruebas) luego de que se realizan las pruebas pertinentes tanto de código como de la aplicación estos pasan al servidor de producción con el ya antes mencionado merge request.

Los PR (pull requests) son la base de la colaboración a proyectos Open Source, si tienen pensando colaborar en alguno es muy importante entender esto y ver cómo se hace en las próximas clases. Por lo general es forkear el proyecto, implementar el cambio en una nueva rama, hacer el PR y esperar que los administradores del proyecto hagan el merge o pidan algún cambio en el código o commits que hiciste.

+ Proceso de un pull request para trabajo en producción:
    - Un pull request es un estado intermedio antes de enviar el merge.
    - El pull request permite que otros miembros del equipo revisen el código y así aprobar el merge a la rama.
    - Permite a las personas que no forman el equipo, trabajar y colaborar con una rama.
    - La persona que tiene la responsabilidad de aceptar los pull request y hacer los merge tienen un perfil especial y son llamados DevOps


### Recopilación de comandos de trabajo

+ Eliminar un repositorio local:

    - `rm -rf .git`

+ Añadir archivos a la etapa de stage/staging
    
    - `git add`

+ Ver el estado de los elementos en stage con el comando:
    - `git status` *-s*

+ Sacar/eliminar elementos que no queremos pasar los archivos al repositorio con:
    
    - `git rm <archivo>`

+ Hacer un commit para pasar los archivos al repositorio local con el comando:
    
    - `git commit` puede llevar -m para agregar comentario
    > ***cada commit es una nueva version de cambios hacia el repositorio***

+ Subir cambios al repositorio remoto con respecto a la rama que trabajamos:

    - `git push`

+ Sacar los commit del repositorio remoto con:
    
    - `git pull`

    > *Después de hacer un pull y si se solapa código, podemos combinar los archivos*

+ Checar que cambios existen en el repositorio remoto:

    - `git fetch`
    > *Antes de mandar cualquier cosa hacer un fetch*

+ Ver los cambios en texto de los cambios que se agregaran:

    - `git diff`

    solo ver los cambios son:

    - `git diff --staged`

+ Ver los log de git:

    - `git log`

    ver los los de una mejor forma:

    - `git log --oneline`

#### MANERAS DE DESHACER UN COMMIT Y/O VOLVER A OTRO COMMIT ANTERIOR

+ Deshacer commit's:

    * Regresar a un commit especifico, eliminando lo que son posteriores a este:

        - `git reset <idCommit> --hard`

        > ***Nos dara un problema de brach ya que la del repositorio externo tendrá más commit's que el local***

        - Utilizaremos `git push -f` para forzar los cambios al repositorio externo

        > *Eliminara permanentemente los commit posteriores al que seleccionamos **Cuidado***

+ Regresar a un commit sin perder otros commit's (Se creara un commit nuevo con los cambios revertidos):


    * Regresar a un commit especifico, sin eliminar otros commits:

        - Para regresar al commit anterior:
            - `git revert <idCommit>`
            > *Si nos dan un problema de archivos los tenemos que resolver manualmente*
            - Una vez resulto los problemas si es que hay ejecutar `git revert --continue`
        - Si queremos regresar a un commit que no sea el anterior:  
            - Ejecutamos `git revert --no-commit <idCommit>`
            > *Si nos dan un problema de archivos los tenemos que resolver manualmente*
            - Una vez resulto los problemas si es que hay ejecutar `git revert --continue`

    + **Ir la version de un archivo o un proyecto entero de un commit anterior** podemos usar:
        > *Solo podras traer un archivo todo el proyecto no se puede*
        - `git checkout <idCommit> <nombreArchivo>`
        > *Con esto iremos al archivo del commit especificado*
        - Podemos recuperar el archivo actual, es decir recuperar el archivo "actual" con:
            * `git checkout main/master <nombreArchivo> o <idCommit>`
        - Para mantener los cambios debemos ejecutar:
            * `git add .` o `git add archivo`
            * `git commit -m "regresando a commit idCommit"` 

## Tags git

Los tags sirven más que en github o en un repositorio remoto, ya que es la forma en la que los demás pueden ver que versiones ocurrieron o como referencia interna.

+ `alias logGit="git log --all --graph --decorate --oneline"`

    - Crea un alias con el comando de tu preferencia

+ `git tag -a <nombreTag> -m <"comentario"> <hasCommit>`

    - Crear un tag de un commit especifico

+ Ver tags:

    - `git tag o git show-ref --tags`

+ Enviar tag a github:

    - `git push --tag`

+ Borrar tag:

    - `git tag -d <nombreTag>`

    > *después hacer un pull y un push de tags*

    - Eliminarlo de github: `git push origin :mimido`

## Ramas

### Ramas básico

+ Verificar en que rama nos encontramos:

    - `git branch`
    
+ Agregar una rama o cambiar de rama existente:

    - `git checkout -b <nombreRama>`
    > *Usualmente se nombran con feature/Nombre o numerodeticket*

+ Movernos entre ramas solo con:
        
    - `git checkout <nombreRama>`

+ Traer los cambios de una rama a la "main":

    > *Debemos estar en la rama main*

    - `git merge nombreRama`

    > *Si surge un error porque otros modificaron el mismo archivo, se tiene que solucionar manualmente decidiendo si los combinaran o borrar algunos cambios*

+ Enviar ramas al repositorio de github:

    - `git push origin <nombreRama>`
    > *Antes hacer un pull de la rama principal, después situarnos en la rama que queremos enviar*

+ Obtener ramas de un repositorio de github:

    - `git pull origin <nombreRama>`

////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

+ comandos "especial"

    - `git reset <idCommit>`: Nos lleva a cualquier commit no importa la rama, ya que identificamos el id del tag., eliminando el historial de los commit posteriores al tag seleccionado.

    - `git checkout <rama-o-id-commit>`: Nos lleva a cualquier commit sin borrar los commit posteriores al tag seleccionado.


Una rama o branch es una versión del código del proyecto sobre el que estás trabajando. Estas ramas ayudan a mantener el orden en el control de versiones y manipular el código de forma segura.

No afectan el código de otras ramas

En otras palabras, un branch o rama en Git es una rama que proviene de otra. Imagina un árbol, que tiene una rama gruesa, y otra más fina, en la rama más gruesa tenemos los commits principales y en la rama fina tenemos otros commits que pueden ser de hotfix, devlopment entre otros.

![imagenDeRamasGit](/frontEnd/imagenes/brach.webp)

### Cómo crear un branch o rama en Git

El comando git branch permite crear una rama nueva. Si quieres empezar a trabajar en una nueva función, puedes crear una rama nueva a partir de la rama master con git branch new_branch. Una vez creada, puedes usar git checkout new_branch para cambiar a esa rama.

Recuerda que todas tus versiones salen de la rama principal o Master y de allí puedes tomar una versión específica para crear otra rama de versiones.

### Cómo hacer merge

Producir una nueva rama se conoce como Checkout. Unir dos ramas lo conocemos como Merge.

Cuando haces merge de estas ramas con el código principal, su código se fusiona originando una nueva versión de la rama master (o main) que ya tiene todos los cambios que aplicaste en tus experimentos o arreglos de errores.

Podemos generar todas las ramas y commits que queramos. De hecho, podemos aprovechar el registro de cambios de Git para producir ramas, traer versiones viejas del código, arreglarlas y combinarlas de nuevo para mejorar el proyecto.

Solo ten en cuenta que combinar estas ramas (hacer “merge”) puede generar conflictos. Algunos archivos pueden ser diferentes en ambas ramas. Git es muy inteligente y puede intentar unir estos cambios automáticamente, pero no siempre funciona. En algunos casos, somos nosotros los que debemos resolver estos conflictos a mano.

## Llaves publicas y privadas

Las llaves públicas y privadas, conocidas también como cifrado asimétrico de un solo camino, sirven para mandar mensajes privados entre varios nodos con la lógica de que firmas tu mensaje con una llave pública vinculada con una llave privada que puede leer el mensaje.

Las llaves públicas y privadas nos ayudan a cifrar y descifrar nuestros archivos de forma que los podamos compartir sin correr el riesgo de que sean interceptados por personas con malas intenciones.

Cómo funciona un mensaje cifrado con llaves públicas y privadas
Ambas personas deben crear su llave pública y privada.
Ambas personas pueden compartir su llave pública a las otras partes (recuerda que esta llave es pública, no hay problema si la “interceptan”).
La persona que quiere compartir un mensaje puede usar la llave pública de la otra persona para cifrar los archivos y asegurarse que solo puedan ser descifrados con la llave privada de la persona con la que queremos compartir el mensaje.
El mensaje está cifrado y puede ser enviado a la otra persona sin problemas en caso de que los archivos sean interceptados.
La persona a la que enviamos el mensaje cifrado puede emplear su llave privada para descifrar el mensaje y ver los archivos.


### Cómo generar tus llaves SSH

1. Generar tus llaves SSH**
Recuerda que es muy buena idea proteger tu llave privada con una contraseña.

`ssh-keygen -t rsa -b 4096 -C "tu@email.com"`

2. Terminar de configurar nuestro sistema.
En Windows y Linux:

Encender el “servidor” de llaves SSH de tu computadora:
`eval $(ssh-agent -s)`

Añadir tu llave SSH a este “servidor”:

`ssh-add ruta-donde-guardaste-tu-llave-privada`

En Mac:

Encender el “servidor” de llaves SSH de tu computadora:

`eval "$(ssh-agent -s)"`

Si usas una versión de OSX superior a Mac Sierra (v10.12), debes crear o modificar un archivo “config” en la carpeta de tu usuario con el siguiente contenido (ten cuidado con las mayúsculas):
Host *

    AddKeysToAgent yes
    UseKeychain yes
    IdentityFile ruta-donde-guardaste-tu-llave-privada


Añadir tu llave SSH al “servidor” de llaves SSH de tu computadora (en caso de error puedes ejecutar este mismo comando pero sin el argumento -K):
ssh-add -K ruta-donde-guardaste-tu-llave-privada

## Github pages

GitHub Pages es un servicio de GitHub que nos permite alojar nuestros proyectos y mostrarlos en vivo en una página web estática sin necesidad de pagar por hosting o siquiera tener conocimientos en servidores o DevOps. 

### Pasos para alojar nuestro proyecto:

- Crear un repositorio nuevo en Github
    > *Dicho repositorio forzosamente debe de empezar con nuestro nombre de usuario u organización seguido de github.io.*
    - Por ejemplo: `nombreDeUsuario.github.io`
- Clonar nuestro repositorio creado o agregarlo como vinculación
    - `git clone <repositorio>`
    - `git remote add origin <repositorio>`
- Enviar el proyecto al repositorio
    - `git add --all`

    - `git commit -m "Initial commit"`

    - `git push -u origin main`
- Ir a setting
    - pages
    - Source > seleccionar main branch 

## Git stash

El stashed nos sirve para guardar cambios para después, Es una lista de estados que nos guarda algunos cambios que hicimos en Staging para poder cambiar de rama sin perder el trabajo que todavía no guardamos en un commit

Ésto es especialmente útil porque hay veces que no se permite cambiar de rama, ésto porque tenemos cambios sin guardar, no siempre es un cambio lo suficientemente bueno como para hacer un commit, pero no queremos perder ese código en el que estuvimos trabajando.

El stashed nos permite cambiar de ramas, hacer cambios, trabajar en otras cosas y, más adelante, retomar el trabajo con los archivos que teníamos en Staging, pero que podemos recuperar, ya que los guardamos en el Stash.

+ Comandos:

    - Guardar el trabajo actual del Staging en una lista diseñada para ser temporal llamada Stash, para que pueda ser recuperado en el futuro. 
        * `git stash`
        > **Nos regresa al ultimo commit antes de los cambios**.
    
    - Podemos poner un mensaje en el stash, para asi diferenciarlos en git stash list por si tenemos varios elementos en el stash. Ésto con:
        * `git stash save "mensaje identificador del elemento del stashed"`

    - Ver los stash que tenemos:
        * `git stash list`
        
    - Recuperar los últimos cambios desde el stash a tu staging area utiliza el comando:
        * `git stash pop`

    - Para aplicar los cambios de un stash específico y eliminarlo del stash:

        * `git stash pop stash@{<num_stash>}`

    - Para retomar los cambios de una posición específica del Stash puedes utilizar el comando:

        * `git stash apply stash@{<num_stash>}`
    
    - Para crear una rama y aplicar el stash más reciente podemos utilizar el comando

        * `git stash branch <nombre_de_la_rama>`

    - Eliminar los cambios más recientes dentro del stash (el elemento 0), podemos utilizar el comando:

        * `git stash drop`

    - Pero si, en cambio, conoces el índice del stash que quieres borrar (mediante git stash list) puedes utilizar el comando:

        * `git stash drop stash@{<num_stash>}`

    - Si, en cambio, deseas eliminar todos los elementos del stash, puedes utilizar:

        * `git stash clear`

### Consideraciones:
- El cambio más reciente (al crear un stash) SIEMPRE recibe el valor 0 y los que estaban antes aumentan su valor.
- Al crear un stash tomará los archivos que han sido modificados y eliminados. Para que tome un archivo creado es necesario agregarlo al Staging Area con git add [nombre_archivo] con la intención de que git tenga un seguimiento de ese archivo, o también utilizando el comando git stash -u (que guardará en el stash los archivos que no estén en el staging).
- Al aplicar un stash este no se elimina, es buena práctica eliminarlo.

## Git clean
***Solo puede borrar los archivos no indexados***

Mientras estamos trabajando en un repositorio podemos añadir archivos a él, que realmente no forma parte de nuestro directorio de trabajo, archivos que no se deberían de agregar al repositorio remoto.

El comando clean actúa en archivos sin seguimiento, este tipo de archivos son aquellos que se encuentran en el directorio de trabajo, pero que aún no se han añadido al índice de seguimiento de repositorio con el comando add.

+ Revisar que archivos no tienen seguimiento.
    - `git clean --dry-run`

+ Eliminar los archivos listados de no seguimiento.
    - `git clean -f`

## Git reflog y reset para recuperar datos

Git guarda todos los cambios aunque decidas borrarlos, al borrar un cambio lo que estás haciendo sólo es actualizar la punta del branch, para gestionar éstas puntas existe un mecanismo llamado registros de referencia o reflogs…La gestión de estos cambios es mediante los hash’es de referencia (o ref) que son apuntadores a los commits…Los recoges registran cuándo se actualizaron las referencias de Git en el repositorio local (sólo en el local), por lo que si deseas ver cómo has modificado la historia puedes utilizar el comando:

- `git reflog`

- Moverte sin realizar ningún cambio al commit exacto de la ref

    - `git checkout <idCommit>`

- git reset: Hará que el último commit sea el pasado por la ref, usar este comando sólo si sabes exactamente qué estás haciendo

    - `git reset --hard <idCommit>` # Perderá todo lo que se encuentra en staging y en el Working directory y se moverá el head al commit eff544f
    - `git reset --soft <idCommit>` # Te recuperará todos los cambios que tengas diferentes al commit eff544f, los agregará al staging area y moverá el head al commit eff544f

- git merge: Puedes hacer merge de un commit en específico, funciona igual que con una branch, pero te hace el merge del estado específico del commit mandado

    - `git checkout master`
    - `git merge <idCommit>` # Fusionará en un nuevo commit la historia de master con el momento específico en el que vive

## Agregar cambios a un commit anterior por si se nos olvido

#### Mala practica

- `git add` # Para hacer uso de amend los archivos deben de estar en staging
- `git commit --amend` # Remendar último commit

## Buscar en archivos y commits de Git con Grep y log

#### grep para los archivos log para los commits

A medida que nuestro proyecto en Git se hace más grande, vamos a querer buscar ciertas cosas.

Por ejemplo: ¿cuántas veces en nuestro proyecto utilizamos la palabra color?

Para buscar, empleamos el comando git grep color y nos buscará en todo el proyecto los archivos en donde está la palabra color.

- git grep -n color nos saldrá un output el cual nos dirá en qué línea está lo que estamos buscando.
- git grep -c color nos saldrá un output el cual nos dirá cuántas veces se repite esa palabra y en qué archivo.

Si queremos buscar cuántas veces utilizamos un atributo de HTML lo hacemos con `git grep -c "<p>"`.

## Comandos colaborativos

A continuación veremos una lista de comandos colaborativos para facilitar el trabajo remoto en GitHub:

- `git shortlog -sn`: muestra cuantos commit han hecho cada miembro del equipo.
- `git shortlog -sn --all`: muestra cuantos commit han hecho cada miembro del equipo, hasta los que han sido eliminados.
- `git shortlog -sn --all --no-merge`: muestra cuantos commit ha hecho cada miembro, quitando los eliminados sin los merges.
- `git blame ARCHIVO`: muestra quien hizo cada cosa línea por línea.
- `git COMANDO --help`:muestra como funciona el comando.
- `git blame ARCHIVO -Llinea_inicial,linea_final`: muestra quien hizo cada cosa línea por línea, indicándole desde qué línea ver. Ejemplo -L35,50.
- `git branch -r`: se muestran todas las ramas remotas.
- `git branch -a`: se muestran todas las ramas, tanto locales como remotas.

## Comando alias en git

Podemos asignar varias alias a comandos de dit con:

- `git config --global alias.<nombreDelAlias> "<comandoAEjecutar>"`