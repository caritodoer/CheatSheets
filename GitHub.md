GIT : Sistema de control de versiones (distribuido)
!==
GITHUB : plataforma de hosting de repositorios donde pueden ser compartidos

Tres estados:
1. working directory. Donde entrn lo archivos al inicio
2. staging area. Area de preparacion del archivo antes de ser incluido
3. git directory (repository). cuando se hace el Commit y se incluye al proyecto.


## Pasos para inicializar Git
posicionarse en la carpeta en la que voy a trabajar:

git config --global user.email "caritodoer@gmail.com"
git config --global user.name caritodoer


# Para subir repositorio
#### desde la terminal del equipo donde esta el proyecto que queremos subir a github
git init
git add .
git commit -m "first commit"
git remote add origin https://github.com/NOMBRE_USUARIO/NOMBRE_PROYECTO.git
git push -u origin master

### Si el repositorio ya existe en git, para bajar el proyecto
git clone https://github.com/caritodoer/rompecocos.git

### Para saber el estado de los archivos en mi compu en relacion con GIT
git status

# Cada vez que quiero subir cambios:

* para descargar actualizaciones y ver los conflictos de merge
git pull origin master

-- si hay errores de merge se genera en el archivo algo asi:

>>> HEAD
... (lo que yo modifique en mi PC)
===
... (lo que esta en la web)
>>> FINAL

esto es un conflicto y se soluciona eliminando ya sea lo que esta en el head o debajo.

* para agregar modificaciones o archivos, arma el "paquete" que va a subir:
git add .

* para que agregue un comentario rel. con las modificaciones.
git commit -m "comentario de modificaciones hechas"

* para subir archivos
git push origin master


#############
## ERRORES ##
#############

* fatal: remote origin already exists
git remote set-url origin https://github.com/caritodoer/rompecocos.git
