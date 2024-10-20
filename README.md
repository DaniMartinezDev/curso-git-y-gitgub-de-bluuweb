# CURSO DE CMD, GIT & GITHUB DE BLUUWEB 
Link al tutorial: https://www.youtube.com/watch?v=PW_A-lOpVV0

# CMD (terminal) y PowerShell
Link al código: https://bluuweb.dev/03-git/
- Son parecidos, pero PowerShell es más moderno y tiene más funciones. 
- CDM es más usado en Linux o en Backend y Hardware. 


## COMANDOS BÁSICOS EN CMD: 

### Desplazamientos y ejecuciones
- CD ==> Ir a una dirección (carpeta) en concreto. En PowerShell se recomienda poner entre comillas si la carpeta tiene espacios.
- CD + ARRASTRAR CARPETA ==> Abre una dirección en especifico. 
- CMD EN NAVEGADOR DE WINDOWS ==> Poner CMD o Powershell en la dirección de la carpeta (F4) y abre la Terminal en esa ruta. 
- CD.. ==> Retrocede a la carpeta anterior. 
- DIR ==> Muestra el directorio de ubicaciones disponibles.
- PWD ==> Muestra la dirección actual.
- CLS o CLEAR ==> Limpiar la terminal.
- CTRL + C ==> Detiene una ejecución en curso.

### Gestión de archivos y carpetas
- MKDIR o MD ==> Crear carpeta
- NI + NOMBRE + EXTENSION==> Crear archivo (ni styles.css por ejemplo).
- MOVE + NOMBRE ARCHIVO + CARPETA DE DESTINO ==> Mueve un archivo o carpeta

### Visual Studio Code (VSC)
- ARRASTRAR CARPETA A VSC ==> Abre el directorio para trabajar en ella. 
- CTLR + SHIFT + Ñ ==> Abre la Terminal integrada en VSC.



# GIT (20:30)
Link al código: https://bluuweb.dev/03-git/02-git.html
- Es un software de control de versiones, para coordinar trabajos en equipos y restaurar versiones previos (sin bugs por ejemplo). 
- Las "branches" (ramas) permiten trabajar con una base de código paralela al proyecto en si. 
- Permite respaldar el proyecto en la nube. 

## Comandos básicos para deploy ==> ADD ... COMMIT ... PUSH #
- <code>GIT VERSION</code> ==> Muestra la versión instalada. 
- <code>GIT HELP</code> ==> Listado de comandos de Git.
- <code>GIT LOG --ONELINE</code> ==> Listado de commits realizados. 
- <code>:Q!</code> ==> Cierra la ejecución de un commit "trabado".
- <code>K</code> ==> Cierra el git log --oneline que figura con "ESC"


## Flujo de trabajo en Git
- <code>GIT INIT</code> ==> Inicia un "REPOSITORIO". Se hace UNA SOLA VEZ por proyecto. 
- <code>GIT ADD</code> ==> Hace un escaneo de los archivos nuevos y modificados, y los añade al "staging area" (carpeta tempotal de Git). (Los archivos pasan de "Untracked" naranja a "A" verde). Se hace previo a un COMMIT.
- <code>GIT COMMIT -M "..."</code> ==> Etiqueta archivos al "local repo", como paso previo al push en el deploy (GitHub por ejemplo). Se usa un -m para poner un mensaje que indique el proceso ejecutado. 
- <code>GIT PUSH</code> ==> "Sube" las modificaciones y archivos nuevos a la nube. Se debío haber creado el "repositorio" en GitHub previamente (ver abajo).

## Uso del Source Control de VSC (CTRL + SHIFT + G)
 Simplifica el procedimiento visto antes, con botones directos:
- Boton "+" (Stage Change) => Reemplaza el git add .
- Boton "Commit" + texto => Reemplaza el git commit -m



# GITHUB (43:20)
- Alojamiento en la nube del repositorio.

## Mecanismo de alojamiento del repositorio
- NEW REPOSITORY ==> Crea un repositorio desde cero.
- Elegir la segunda opción (... OR PUSH AN EXISTING).
- Copiar la primera linea de código con el comando <code>git remote add origin ...</code>
- Pegar el comando elegido en la terminal de VSC
- Ejecutar <code> git branch -M main </code> o <code> git branch -M master </code> (segun como se venga trabajando en local).
- Ejecutar <code> git push -u origin main </code> o <code> git push -u origin master </code>.

Con este procedimiento, se "subió" el repositorio a GitHub y ya los proximos cambios se subiran con <code>GIT PUSH</code> o COMMIT & PUSH (Source Version VSC).

## Clonar un repositorio de GitHub
### Mecanismo de clonación 
Pulsar el boton de arriba del repositorio llamado "<>code" y seleccionar CLONE. Existen tres metodos para clonar. 
- Github Desktop (PREFERIDA) ==> Se abre la app de escritorio y se debe seleccionar la carpeta de destino de la clonación. 
- URL ==> Copiar el link que figura y luego, ejecutar la terminal en la carpeta de destino, con el comando <code>git clone + link copiado</code>. 
- Descargar Zip ==> Se descargan las carpetas y archivos, pero sin los commits. Por eso se recomiendan las anteriores.



# GIT INTERMEDIO (58:30)
## Ignore, Log, Checkout, Reset, Reverb, Branch & Merge, Conflictos, Tags y Pull.
Link al código: https://bluuweb.dev/03-git/03-git-intermedio.html#recursos

## Git Ignore: Ignorar archivos o carpetas en Git
Se utiliza para carpetas o archivos privados que no pueden ser mostrados al público, como por ejemplo, los archivos ".env" o la carpeta node_modules (entorno de Node JS).
- CREAR ARCHIVO ".gitignore" ==> Ir agregando la lista de archivos a ser ignorados por Git (por ejemplo, ".env"). Los archivos y carpetas quedan en un color gris oscuro.

## Git log: Viajar entre versiones (1:03:00)
Explicación: Muestra el historial de commits realizados en el proyecto.
- <code> git log --oneline </code>
- Si hay algun error con ESC ==> Pulsar tecla <code> K </code>
- <code> git reflog </code> ==> Muestra el historial completo de los cambios (incluidos resets). Sirve para deshacer algun reset -- hard por ejemplo. 

## Git checkout: Viajar entre versiones (1:07:00)
Explicación: Sirve para revisar los cambios que se hicieron en los commits (de manera individual).
Muestra la situación de esa "versión" (es decir, la "foto" del proyecto en ese commit).
Importante: NO se usa para hacer cambios, solo para revisar esa versión en concreto. 
- <code> git ckeckout + nombre commit a revisar</code> ==> Ir a la revisión indicada.
- <code> git checkout master/main (o el nombre commit HEAD (última versión)) ==> Vuelve al estado actual.

## Git master a main: Renombrar ramas (1:13:00)
- <code> git branch -m master main </code> ==> Renombra solo en el proyecto.
- <code>  git config --global init.defaultBranch main ==> Setea a Main como rama de origen por defecto.

## Git Reset: Retroceder eliminando los cambios realizados (1:15:30)
Explicación: Se "rescata" una versión anterior, eliminando los cambios de los commits posteriores. Pero si se quiere ir a la ultima versión, tambien se puede hacer usando el reset con el último commit.
- <code> git reset + nombre commit a resetear</code> ==> Recupera la versión anterior pero conserva los archivos (sin seguimiento, con la "U").
- <code> git reset --hard + nombre commit a resetear</code> ==> Recupera la versión anterior pero tambien borra todo el contenido de los commits posteriores. Se deshace con un reset -- hard a la última versión (se visualiza con git reflog).

ADVERTENCIA: Posibles conflictos de versiones en GitHub, sobre todo en trabajo colaborativo, ya que hace commits de versiones anteriores en el repositorio remoto, y entonces, se eliminan tambien los commits de GitHub. Se soluciona con: 
<code>git pull origin YOUR_BRANCH_NAME</code> ==> Restaura la última versión remota.

## Git Revert: Borrar un commit concreto (1:29:00)
Explicación: Deshace los cambios realizados por un commit anterior creando un commit completamente nuevo, todo esto sin alterar el historial de commits.
- <code>git revert + ID commit</code> ==> Revertir un commit.
- 

## Git Branch (ramas) & Merge (fusión): ... (1:32:15)
### Branch
Explicación: Uso en trabajo colaborativo, ya que no se suele trabajar en la rama MAIN. 
- <code>git branch</code> ==> Muestra la rama actual en donde se esta trabajando.
- <code>git branch + ID nuevo branch</code> ==> Crea una rama. 
- <code>git checkout + ID branch de destino</code> ==> Desplazamiento entre ramas. 
- <code>git log --oneline --graph</code> ==> Muestra el tree (arbol) de commits. 
- <code>git push --set-upstream origin + ID Branch</code> ==> Sube a GitHub los cambios en la rama. Si se pone solo <code>git push</code> sale un error, porque eso solo se usa para la rama main.

### Merge (1:38:00)
Explicación: Fusión de branch (ramas). 
- <code>git merge + ID branch "absorbente"</code> =>

## Git x: -
Explicación:
- 
- 

## Git x: -
Explicación:
- 
- 
