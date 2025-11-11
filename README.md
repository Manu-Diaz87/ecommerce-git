## Git: Sistema de administración de repositorios locales.

Es un sistema de control de versiones nos permite administrar los repositorios locales de nuestra computadora. Brindandonos diferentes comandos para interactuar con ellos.

Un repositorio (o repo) es una carpeta/directorio que contiene todos los archivos de un proyecto (ej, un proyecto web), junto con un historial de todos los cambios y versiones que se realizaron sobre ese archivo (si los hay, si no es nuevo).

Al inicializar Git en esa carpeta, podemos comenzar a gestionar y administrar el repo local. A medida que avanzamos se van generando diferentes versiones del código porque el proyecto evoluciona.

A través de Git, vamos guardando o 'commiteando' estas diferentes versiones, generando el historial que nos permite navegar entre ellas (volver hacía atrás o adelantarse.)


## Github - Almacenamiento de repositorios en la nube

Github, no tiene los comandos de git, pero nos sirve para que trabajen en conjunto, dandonos la posibilidad de almacenar nuestro repo LOCAL, en un repo REMOTO (la nube), esto nos habilita la posibilidad de poder compartir nuestro proyecto con:

    - un equipo de trabajo
    - un compañero
    - cualquier persona que tenga el link del repo (si nuestro repo es público).

### Ramas en github.

Además entra otras cosas, nos la posibilidad de trabajar en diferentes ramas. Las ramas son como copias secundarias de lo que se denomina como rama 'principal'. Para que sirve? nos dan la posibilidad de hacer cambios tranquilamente, sin generar conflictos el código/version original/principal. Luego una vez que comprabamos que nuestros cambios funcionan de forma correcta, recién podríamos vincular los cambios de esta rama 'secundaria' con la rama principal.

## Comandos básicos de GIT: trabajando en nuestro repo local.
**Los comandos se ejecutan sobre la terminal**

- git -v: nos devuelve de la versión actual de nuestro Git.

- git config --global user.name "nombre de usuario": Establecer tu nombre usuario para el sistema de Git.

- git config --global user.email "correo@gmail.com". Establece tu emal para el sistema de Git.

**Se recomienda que tanto el username, como el email, sean los mismo que utilizamos en nuestra cuenta de github**

## Manejo de Repositorios

    - git init: Inicializar un nuevo repositorio local (se ejecua solamente una vez.)

    - git status: Meustra el estado general de los archivos del repositorio, es decir, cuales son nuevos, modificados, y si estan preparados para su confirmación (commit), entre otros datos.

    - git add . : Añade todos los archivos nuevos y modificados, al Staging Area, 'Area de Preparación', esta area es la encargada de 'preparar' los archivos para ser incluidos en el próximo commit (confirmación de los cambios). En este punto podemos restablecer de forma sencilla los archivos a como estaban antes de ser modificados.

    - git commit -m "Mensaje/comentario de los cambios realizados": Confirmar definitivamente los cambios preparados en el Staging Area, generando una nueva versión del proyecto/repo. Cada commit forma parte de un historial de versiones.


### Area de trabajo en GIT

    1. Directorio de trabajo (Working Directory): los archivos que estamos modificando.
    2. Staging Area (Area de Prepración): Donde seleccionamos los archivos y sus cambios para incluirlos en el proximo commit.
    3. Repositorio Local (.git): Almacena el historial de commits.


## Administración de commits
 
- git log --oneline: Nos muestra el historial de commits, incluyendo el código (identificador) de cada commit.


### Deshacer y Editar Commits.
***El proceso varía si el commit ya fue publicado o no (si fue pusheado al repo remoto)**

#### Deshacer el último Commit (NO publicado):

Si queremos deshacer un commit, podemos ejecutar el comando:

- git reset --soft (Identificador del commit): Deshace el commit especificado, pero mantiene los cambios en el Staging Area.

- git reset --hard (Identificador del commit): Deshace el commit y descarta TODOS los cambios realizados. Importante: se pierden TODOS los cambios de esa versión.


## ⛓️‍💥 Vincular repo local con el repo REMOTO (github)
Una vez que ya generamos alguna confirmación (commit) y tenemos ya el historial con al menos una versión del repo local, podemos proceder a vincular el repo remoto para poder subir los cambios a la nube.

**Recomendación cambiar el nombre de la rama master a main, con el comando: git branch -M main**

- git remote add origin <url_repo_remoto>: Nos permite vincular el repo local con el repo remoto, a ese vinculo se le da el nombre de 'origin'.

- git remote --v: Nos sirve para verificar si el vinculo/conexión se realizo correctamente.

- git push -u origin main: Sube/envía los cambios commiteados desde la rama local (main) al repo remoto.



## Ramas - Branchs - Github


- git branch: nos muestra todas las ramas del repositorio local

- git branch [nombre_rama]: Crea una nueva rama.

- git switch [nombre_rama]: Nos permite movernos hacia la rama especificada. * Primero es recomendable guardar todos los cambios realizados en la rama donde estamos posicionados actualmente

- git branch -D [nombre_rama]: Elimina la rama especificada.

- git branch -M [nombre_rama]: Renombrar la rama sobre la cual estoy posicionado.

- git merge [nombre_rama]: Fusiona la rama especificada con la rama donde estamos posicionados actualmente.










