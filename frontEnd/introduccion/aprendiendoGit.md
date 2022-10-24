### Primero pasos en Git y Github

Aprenderé Git de manera autónoma a traves de videos y cursos y los listare a continuación:

> YouTube 
> Canal: HolaMundo, video: Aprende GIT ahora! curso completo GRATIS desde cero
> Canal: Yito on Code, video: Git-GitFlow & Github | Curso práctico utilizando flujo de trabajo (desde cero)

#### Apuntes 

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

**Comandos de configuración:**

Ver ayuda:

`git -h` 

Establecer nombre:

`git config --global user.name "nombre"` 
> *global se utiliza para que la configuración se efectué de manera global y no solo al proyecto*

Establecer email:

`git config --global user.email email`

Establecer que la rama principal sea "main"(esto debido a que github lo toma con ese nombre):

`git config --global init.defaultBranch main`

Establecer el comando que usaremos para abrir nuestro editor:

`git config --global core.editor "code --wait"`

En windows cada vez que utilizamos un salto de linea Windows agrega 2 caracteres especiales
- CR(CARRIAGE RETURN)
- LF(LINE FEED)
En Linux/mac solo se agrega el carácter *LF*, por ello debemos cuando se suba código en github si somos usuarios windows debemos asegurarnos que cuando se suba el código se elimine el carácter ***CR*** y cuando se baje código agregarlo, eso lo logramos con los comandos:

+ Windows
    * `git config --global core.autoclrf true`
+ Linux
    * `git config --global core.autoclrf input`

Iniciar git:

*primero es ir a la carpeta de nuestro proyecto.*

Ejecutar el comando:

`git init`

> *Este comando crea un area en memoria ram llamada staging*
> *crea el repositorio .git*

> *La  carpeta de .git es siempre ignorada por los repositorios que creamos, no comparte entre desarrolladores y no se envía al servidor central*

#### Flujo de trabajo que debemos seguir

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

#### Recopilación de comandos de trabajo



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

+ Trabajar con ramas

    * Verificar en que rama nos encontramos:

        - `git branch`
    
    * Agregar una rama o cambiar de rama existente

        - `git checkout -b nombreRama`

        > *Usualmente se nombran con feature/Nombre o numerodeticket*

+ Traer los cambios de una rama a la "main"

    > *debemos estar en la rama main*

    - `git merge nombreRama`

+ Indicar el servidor remote en el cual guardar los cambios:

    - `git remote add origin "repositorio"`

+ Agregar rama main a un repositorio nuevo
    
    -`git push -u origin main`
+ Clonar un repositorio remoto a local_

    - `git clone "repositorio"`
