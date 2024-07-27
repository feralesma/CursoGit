# Document de prova de Markdown

## Introducción a Git - Miguel ángel Florido [The Bridge](https://www.youtube.com/watch?v=Mkd8idNUolM)

### ¿Qué es Git?

- **Git** es un sistema de control de versiones de código. Es como us sistema de copia de seguridad de archivos pero para código, y con una salvedad: si se modifica un archivo en lugar de guardar todo el archivo **Git** sólo guarda los cambios realizados. Además va a servir para colaborar con varios usuarios cada uno con su versión sin romper la versión de los demás.

### ¿Qué es GitHub?

- _GitHub_ es un servicio basado en _Git_.
- Nos da la posibilidad de poder alojar "Repositorios": una carpeta controlada por el sistema de control de versiones _Git_ a la que subir nuestros archivos y proyectos.
- ...

---

### Comandos básicos de la terminal:

- ls
- ls -la
- cd ..
- cd /dir1/dir2
- cd dir3/dir4
- cd
- pwd
- Ctrl+c
- clear ó Ctr+l
- ...

### Comandos para Git:

- git --version  
  `Para conocer la versión instalada de Git`  
  <https://git-scm.com/downloads>  
  <https://learngitbranching.js.org/?locale=es_ES>
- git config --global user.name feralesma  
  `Empezamos a configurar Git con los datos de nuestro usuario (usuario de GitHub, aunque también podemos poner nuestro nombre completo).`
- git config --global user.email feralsal@yahoo.es
- git config --global user.name  
  `Nos dirá el nombre de usuario configurado`
- ...  
  /_ Creación del repositorio en GitHub _/
- ...
- cd Desktop
- git clone https://github.com/MIGUELez11/TallerGit  
  `Descarga el repositorio indicado por la url en la carpeta TallerGit que creará en local (si añadimos "espacio NombreCarpetaNueva" crearía una nueva carpeta en la que descargar el repositorio).`
  ...
- cd TallerGit <!-- Entramos en el repositorio --> <!-- Comentario idem a HTML -->  
  `Entramos en el respositorio local y realizamos cambios en nuestros ficheros con nuestro editor de código favorito.`
- git status  
  `Nos dirá la rama en que estamos y si hay cambios o acciones a realizar en el repositorio`  
  `Cuando se producen cambios hay que agregarlos al "Staging area" que es como una especie de escenario en el que tiene lugar la actuación y que va estar esperando a que se cierre el telón y tenga todo una versión definitiva`
- git add README.md  
  `con git add podemos poner el nombre del archivo a añadir al Staging Area o podemos utilizar el parámetro -A para añadirlos todos (los que aparezcan en rojo que son los pendientes de añadir).`
- git add -A
- git status  
  `Vemos los cambios que se van a tener en cuenta pero que aún no son definitivos (en verde) y también otros posibles cambios posteriores pendientes de añadir al Staging Area (en rojo).`
- git commit -m "Mensaje descriptivo del commit"  
  `Creamos una nueva versión, una copia o versión definitiva que vamos a poder volver a ella en un futuro por si hemos tenido algún tipo de error y hemos de volver atrás. Con -m añadimos un mensaje descriptivo que nos indique lo realizado hasta el momento.`
- git status  
  `Ahora veríamos que nuestro historial de cambios está limpio.`
- git log  
  `Con este comando comprobamos que nuestra versión ha tenido efecto y nos va permitir ver todos los commits que han tenido lugar.`
- git pull
  > Sirve para sincronizar cambios realizados en el repositorio original (servidor remoto) que no tenemos aún en nuestro equipo o repositorio local.  
  > Al hacer esto podría ocurrir que hubieran discrepancias entre los cambios locales y los remotos, entonces tendremos que decidir qué cambios queremos aplicar y cuales no, para lo cual tendremos que modificar el fichero que tenga cambios y eliminar los que no queramos (aparecen en colores diferentes los cambios locales y los remotos). También podremos quedarnos con todos los cambios para lo cuals sólo eliminaremos los códigos que llevan aparejados los cambios.
- git add -A
- git status
- git commit -m "Fixed conflicts"
- git push  
  `"Empujar" o llevar los cambios al servidor.`

---

### Comandos para un ejemplo <https://www.youtube.com/watch?v=DuYjcOZw11s>

- git config --global user.name "Rafa Gómez"
- git config --global user.mail "rafa.gomez@codely.tv"
- head -n 3 ~/.gitconfig
- mkdir git-examples
- cd git-examples
- git init
  `Inicializamos esta carpeta como repositorio local para que el gestor de sepa sepa que está "versionada". El repositorio de Git es distribuido, descentralizado.`
- ls -la
  `Buscamos el directorio .git que almacena toda la configuración.`
- touch Readme.md
- ls
- git status
- ...
- git add Readme.md //Trackear fichero
- git commit ...
- git status
- ...
- git log
- ...  
  `Sourcetree es una herramienta gráfica para Git`
- ...
- git remote add origin git@github.com:CodelyTV/example-git.git  
  `origin es el nombre que se le da al repositorio remoto de nuestro equipo por convención`
- git remote -v
- git push -u origin master
- vim Readme.md
- ...
- git commit -am "Add some message"
- git push origin master
- ...

---

---

## Curso Git & GitHub.

Video 1 [pildorasinformaticas](https://www.youtube.com/watch?v=ANF1X42_ae4&list=PLU8oAlHdN5BlyaPFiNQcV0xDqy0eR35aU)

### ¿Qé es Git?

- Software de control de versiones creado por Linus Torvalds.
- Es un software libre.

### ¿Para qué sirve?

- Facilitar el desarrollo y mantenimiento de aplicaciones tanto de forma individual como sobre todo al trabajar en equipo.

### ¿Cómo?

- Guardadndo un registro de todos los cambios que sufran los archivos.
- Git toma una instantánea del estado actual del archivo según se lo vamos pidiendo. A cada instantánea se le asigna un código y una posible descripción.
- Esto nos permite revertir el estado de un archivo en un momento concreto en el tiempo, lo que nos permite ir a un estado concreto del archivo.
- Git es capaz de realizar esto no de un sólo archivo sino de muchos archivos. Por tanto, Git toma una "foto" de todos los archivos de una aplicación.
- Además Git es capaz de trabajar con "Ramas" o flujos de trabajo, para que cada programador que trabaje en equipo en un mismo proyecto tenga su propia versión del proyecto y puedan trabjar en partes diferenciadas del proyecto.
- Finalmente Git es capaz de fusionar distintas "Ramas" para unificar todo el proyecto, y además también es capaz de detectar conflictos entre archivos de varios programadores que han trabajado en los mismos archivos.

### Creando repositorio.

Vídeo 2 [pildorasinformaticas](https://www.youtube.com/watch?v=qk-GWtcdQek&list=PLU8oAlHdN5BlyaPFiNQcV0xDqy0eR35aU&index=2)

- Crear repositorio

  - git init  
    `Sólo se ejecuta una vez, cuando queremos que Git comience a realizar el siguimiento de un proyecto.`
    Crea dos áreas:
    - Área de ensayo (staging area): es una área temporal, en la que podemos ver qué archivos tienen seguimiento por parte de Git y cuales no, en qué estado se encuentra cada uno de esos archivos, etc.
    - Repositorio local: donde se almacenan las instantáneas de Git de los archivos y que después podremos recuperar.
  - git add
    `Le indicamos a Git los archivos de los que hacer seguimiento, bien sean todos o algunos en conreto.`
    `Lleva el archivo/s indicado/s desde nuestro directorio de trabajo al al área de ensayo`
  - git commit
    `Traslada el archivo/s que tengamos en el área de ensayo al repositorio local que es donde se tomará la instantánea del arvhivo/s, es ahí donde se crea el respaldo propiamente dicho.`
  - [Git commands](https://git-scm.com/docs/git#_git_commands)

- Agregar archivos y directorios a repositorio

  - git status -s
    `Nos da un listado con todos los archivos y directorios que tenemos en la carpeta de proyecto. Si aparecen interrogantes en rojo antes de los nombres de archivo/carpeta significa que Git advierte de la aparición de archivos/carpetas pero __no__ les está haciendo siguimiento.`
  - git add index.html
    `Ahora Git hará el siguimiento  sólo del archivo index.html.`
  - git status -s
    `Ahora podemos ver que index.html ha cambiado su estado. Ha pasado al staging area, área de ensayo y se va estar monitoreando.`

- Respaldar archivos y directorios en repositorio

  - git commit -m "Comienzo del proyecto"
    `Con este comando pasarían los archivos del staging area al repositorio local y comenzarían a realizarse las instantáneas o respaldos de dichos archivos. Pero si es la primera vez que se usa la consola de Git nos dará error y nos perdirá que introduzcamos un nombre de usuario y un email. Nos dará instrucciones para registrar el usuario y mail y también de como corregirlos.`
    _ ...
    _ Committer: Fernando Alemany Salvà <ifernando@ajupego.local>
    Your name and email address were configured automatically based
    on your username and hostname. Please check that they are accurate.
    You can suppress this message by setting them explicitly. Run the
    following command and follow the instructions in your editor to edit
    your configuration file:
    _ git config --global --edit
    _ After doing this, you may fix the identity used for this commit with:
    _ git commit --amend --reset-author
    _ ...
  - También hubiéramos podido inicializar el nombre de usuario y mail para el repositorio con los comandos siguientes previos al commit:
    - git config --global user.name "Fernando Alemany Salvà"
    - git config --global user.email "servimatic@gmail.com"
  - git status -s
    `Ahora podremos ver que sólo aparecen los archivos sin seguimiento, y los que lo tenían han pasado al repositorio y ya no aparecen en el staging area.`
  - Si realizamos modificaciones en algún fichero, al volver a resisarlo con `git status -s` podremos observar que nos indica los ficheros modificados (M en rojo) junto a los ficheros a los que no realiza seguimiento (?? en rojo) si los hay.
  - Para tener en cuenta los cambios realizados, primero habrá que enviar los ficheros modificados al staging area y después realizar el commit para que se realice una nueva instantánea:
    - `git add index.html` ó tb. `git add -A para enviarlos todos`
    - `git commit -m "Agregando título al archivo y primer párrafo"`
  - Para saber todas las copias, es decir todos los commits realizados hasta el momento y poder ver un listado usaríamos el comando:
    - `git log --oneline` o simplemente `git log`
  - Si queremos restaurar un archivo a una versión anterior podemos utlizar el comando:
    - `git reset --hard código_de_instantánea_indicado_por_git_log`
  - Habrá que tener en cuenta que si restauramos a una versión inicial saltándonos las copias realizadas posteriormente a ella, perderemos los cambios de las últimas copias no pudiendo volver a ellas.

### Subiendo a GitHub.

Vídeo 3 [pildoras](https://www.youtube.com/watch?v=0UlqvTJzOL4&list=PLU8oAlHdN5BlyaPFiNQcV0xDqy0eR35aU&index=3)

- Algunos comanados más.

  - `git add .`
    - Para hacer seguimiento de todos los archivos.
  - `git commit -am "párrafo y tamaño de fuentes"`
    - Hacemos un add + commit para cuando tengamos que hacer las dos operaciones contiguas.
  - `git commit --amend`
    - Podemos abrir el editor establecido en Git en su instalación (por defecto vim) para realizar modificaciones como por ejemplo el mensaje agregado a un commit.
  - La propia consola nos ofrece algunos consejos sobre lo que podemos hacer ...
    > ...  
    > Changes to be committed:  
    > (use "git restore --staged <file>..." to unstage)  
    > Changes not staged for commit:  
    > (use "git add <file>..." to update what will be committed)  
    > (use "git restore <file>..." to discard changes in working directory)  
    > ...

- Subir respositorio a GitHub
  - Primero hay que registrarse en GitHub y una vez registrados crearemos un repositorio.
  - Una vez creado nos ofrece un "Quick setup" con varias opciones y los comandos que deberíamos utilizar para cada una de las opciones.
    - Get started by creating a new file or uploading an existing file. We recommend every repository include a README, LICENSE, and .gitignore.
    - …or create a new repository on the command line:
      ```
      echo "# CursoGit" >> README.md
      git init
      git add README.md
      git commit -m "first commit"
      git branch -M main
      git remote add origin https://github.com/feralesma/CursoGit.git
      git push -u origin main
      ```
    - …or push an existing repository from the command line:
      ```
      git remote add origin https://github.com/feralesma/CursoGit.git
      git branch -M main
      git push -u origin main
      ```
  - Nosotros usaremos el segundo bloque puesto que partimos de un repositorio existente en local.
  - ...

### Clonación y tags.

Video 4 [pildoras](https://www.youtube.com/watch?v=axXlYdyDD3I&list=PLU8oAlHdN5BlyaPFiNQcV0xDqy0eR35aU&index=4)

- Editar desde GitHub

  - Si realizamos cambios en los ficheros desde GitHub podremos sincronizarlos con el respositorio local con el comando:
    - `git pull ` desde la consola del respositorio local
  - ...

- Crear tags
  - Supongamos que "nuestro proyecto" está acabado y funciona y que por tanto tenemos nuestra "versión 1.0" preparada para poder descargar. Esto lo podemos hacer gracias a las "Tags".
  - ` git tag 15-09-20v1 -m "Versión 1 del proyecto"` creamos la versión 1 del proyecto.
  - `git log --oneline` para ver lo realizado por el comando anterior.
  - `git pusth --tags` con esto subiremos las tags al repositorio remoto.
  - Ahora desde **GitHub** podemos ver que ya hay tags creadas y al hacer clic sobre la opción **Tag** nos dará la opción de descargar el proyecto en versión zip o tar.gz.
  - Una utilidad es que si una versión no funciona bien podremos volver a la versión anterior también desde las tags.
- Clonación de repositorio en local
  - Si por algún motivo, como un error o borrado accidental, perdemos la carpeta del proyecto en nuetro ordenador podemos recuperar toda la carpeta desde GitHub:
    - En el repositorio de GitHub vamos al botón **"Code"** y al desplegarse vemos que nos ofrece una url para clonar el repositorio a través de https (también por ssh ??), o descargando un zip del proyecto, en definitiva tenemos varias opciones. Desde la consola podremos utilizar (pegar) la url para utilizar el comando y clonar el repositorio en local desde GitHub:
      - `git clone https://github.com/feralesma/CursoGit.git`
  - ...

### Ramas o Branches.
Video 5 [pildoras](https://www.youtube.com/watch?v=q9LJIHDgJtE&list=PLU8oAlHdN5BlyaPFiNQcV0xDqy0eR35aU&index=5)

- Ramas o branch

  - Son ramas o líneas de tiempo de nuestro proyecto compuestas por todos loc "commits" que se han ido creando. Las ramas tienen un nombre que por defecto es la rama "Master".
  - En los proyectos en los que participan varias personas y que son complejos, a partir de cierto "commit" podríamos volver a otro commit anterior porque no nos convence la situación actual del proyecto (y esto puede pasar varias veces) o tal vez porque se decide probar como quedaría el proyecto al hacer ciertas pruebas. Otro caso que podría darse es que cada persona se encargue de una parte del proyecto (una para html, otra para css y otra para js). Las ramas o branches sirven para ayudarnos en todos estos casos.
  - Inicialmente se trabaja en la rama "Master" pero adicionamente se pueden crear otras ramas paralelas. Esto es como si tuvieras el original y una copia en las que se puede trabajar simultáneamente, trabajando cada copia de forma independiente (pudiéndose fusionar en cierto momento del proyecto) para lo cual hay que tener en cuenta los posibles conflictos de concurrencia (modificación del mismo archivo o código) que puedan existir.
  - `git branch javascript` crea la rama "javascript"
  - `git branch` vemos las ramas que hay y en que rama estamos trabajando
  - `git checkout javascript`para moverse a la rama "javascript"
  - Si ahora realizamos cambios en los archivos estos tendrán lugar en la rama "javascript":
    * `git add .`
    * `git commit -m "saludo javascript agregado`
    * `git log --oneline`
  - Si ahora nos volvemos a la rama "master" en esta rama no tendremos los cambios realizados en la otra rama.
    * `git checkout master`
  - De vuelta a la rama javascript deberíamos volver a tener los últimos cambios realizados.
  - 