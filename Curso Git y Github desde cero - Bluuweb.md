Link al tutorial: https://www.youtube.com/watch?v=PW_A-lOpVV0

##### CMD (terminal) y PowerShell #####
Link al código: https://bluuweb.dev/03-git/
- Son parecidos, pero PowerShell es más moderno y tiene más funciones. 
- CDM es más usado en Linux o en Backend y Hardware. 


### COMANDOS BÁSICOS EN CMD: 

# Desplazamientos y ejecuciones#
CD ==> Ir a una dirección (carpeta) en concreto. En PowerShell se recomienda poner entre comillas si la carpeta tiene espacios.
CD + ARRASTRAR CARPETA ==> Abre una dirección en especifico. 
CMD EN NAVEGADOR DE WINDOWS ==> Poner CMD o Powershell en la dirección de la carpeta (F4) y abre la Terminal en esa ruta. 
CD.. ==> Retrocede a la carpeta anterior. 
DIR ==> Muestra el directorio de ubicaciones disponibles.
PWD ==> Muestra la dirección actual.
CLS ==> Limpiar la terminal.
CTRL + C ==> Detiene una ejecución en curso.

#Gestión de archivos y carpetas# 
MKDIR o MD ==> Crear carpeta
NI + NOMBRE + EXTENSION==> Crear archivo (ni styles.css por ejemplo).
MOVE + NOMBRE ARCHIVO + CARPETA DE DESTINO ==> Mueve un archivo o carpeta

#Visual Studio Code (VSC)#
ARRASTRAR CARPETA A VSC ==> Abre el directorio para trabajar en ella. 
CTLR + SHIFT + Ñ ==> Abre la Terminal integrada en VSC.


##### GIT (20:30) #####
Link al código: https://bluuweb.dev/03-git/02-git.html
- Es un software de control de versiones, para coordinar trabajos en equipos y restaurar versiones previos (sin bugs por ejemplo). 
- Las "branches" (ramas) permiten trabajar con una base de código paralela al proyecto en si. 
- Permite respaldar el proyecto en la nube. 


###Flujo de trabajo en Git ###


# Comandos básicos para deploy ==> ADD ... COMMIT ... PUSH
- GIT VERSION ==> Muestra la versión instalada. 
- GIT HELP ==> Listado de comandos de Git.
- GIT LOG --ONELINE ==> Listado de commits realizados. 

- GIT INIT ==> Inicia un "REPOSITORIO". Se hace UNA SOLA VEZ por proyecto. 
- GIT ADD ==> Hace un escaneo de los archivos nuevos y modificados, y los añade al "staging area" (carpeta tempotal de Git). (Los archivos pasan de "Untracked" naranja a "A" verde).
- GIT COMMIT -M "..." ==> Etiqueta archivos al "local repo", como paso previo al push en el deploy (GitHub por ejemplo). Se usa un -m para poner un mensaje que indique el proceso ejecutado. 
- GIT PUSH ==> "Sube" las modificaciones y archivos nuevos a la nube. 



