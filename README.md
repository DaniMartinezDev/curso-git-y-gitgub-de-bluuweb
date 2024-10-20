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
- GIT VERSION ==> Muestra la versión instalada. 
- GIT HELP ==> Listado de comandos de Git.
- GIT LOG --ONELINE ==> Listado de commits realizados. 
- :Q! ==> Cierra la ejecución de un commit "trabado".


## Flujo de trabajo en Git
- GIT INIT ==> Inicia un "REPOSITORIO". Se hace UNA SOLA VEZ por proyecto. 
- GIT ADD ==> Hace un escaneo de los archivos nuevos y modificados, y los añade al "staging area" (carpeta tempotal de Git). (Los archivos pasan de "Untracked" naranja a "A" verde). Se hace previo a un COMMIT.
- GIT COMMIT -M "..." ==> Etiqueta archivos al "local repo", como paso previo al push en el deploy (GitHub por ejemplo). Se usa un -m para poner un mensaje que indique el proceso ejecutado. 
- GIT PUSH ==> "Sube" las modificaciones y archivos nuevos a la nube. Se debío haber creado el "repositorio" en GitHub previamente (ver abajo).

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

## Git log: Viajar entre versiones
Explicación: Muestra el historial de commits realizados en el proyecto.
- <code> git log --oneline </code> ==> 

## Git x: Viajar entre versiones
Explicación: Sirve para revisar los cambios que se hicieron en los commits (de manera individual).
Muestra la situación de esa "versión" (es decir, la "foto" del proyecto en ese commit).
Importante: NO se usa para hacer cambios, solo para revisar esa versión en concreto. 
- <code> git ckeckout (nombre commit a revisar)</code> ==> Ir a la revisión
- <code> git checkout master o el nombre commit HEAD (última versión) ==> Vuelve al estado actual

## Git x: Viajar entre versiones
Explicación
- 
- 

## Git x: Viajar entre versiones
Explicación
- 
- 

## Git x: Viajar entre versiones
Explicación
- 
- 
