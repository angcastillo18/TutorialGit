# TutorialGit
####  Git es un sistema de control de versiones:

- 	Graba cambios de nuestros archivos todo el tiempo.
- 	Recuerda las versiones específicas de nuestros archivos en cualquier tiempo.
- 	Mucha gente puede fácilmente colaborar en un proyecto y tiene su propia versión de los proyectos de su archivo en su computadora. 

#### ¿Por qué usar git?

- 	Trabaja en nuevas características sin perder el código base de tu código.
- 	Regresa a cualquier versión de tu proyecto que quieras.
- 	Fácil colaboración con otros programadores.
- 	Almacena revisiones en un historial de proyecto en un directorio.

#### Estados:

- 	Modified(Modificado): Cambios en los archivos no commiteados.
- 	Staging(preparado): Preparado significa que has marcado un archivo modificado en su versión actual para que vaya en tu próxima confirmación.
- 	Commited(confirmado): Todos los cambios que ya se añadieron al commit.

#### El flujo de trabajo básico en Git es algo así:
1.	Modificas una serie de archivos en tu directorio de trabajo.
2.	Preparas los archivos, añadiéndolos a tu área de preparación.
3.	Confirmas los cambios, lo que toma los archivos tal y como están en el área de preparación, y almacena esas instantáneas de manera permanente en tu directorio de Git.

######  Configurar por primera vez git (Identidad):
    git config –global user.name “angelo”
    git config –global user.email pepito@gmail.com
######  Comprobando tu configuración:
    git config --list 
######  Inicializando git localmente: 
        $ git init
###### Inicializando un repositorio en un proyecto existente localmente y recién creado en github, sin sincronizarlo (eliges que branch poner):
`$ git push git://github.com/schacon/grit.git master`
###### Clonando un repositorio existente: 
    $ git clone git://github.com/schacon/grit.git
###### Comprobando el estado de tus archivos:
    $ git status
###### Seguimiento de nuevos archivos: 
    $ git add “nombre de archivo”
    $ git add .
###### Removerlo del estado stage:
    $ git rm –cached <file>
###### Ver el historico de commits:
    $ git log
	$ git log --oneline
###### Hacer un commit: 
    $ git commit -m 'initial commit'
###### Pedir ayuda:
    $ git help <comando>
    $ git <comando> --help
    $ man git-<comando>
###### conectar nuestro repositorio local con un repositorio en github:
    $ git remote add origin git://github.com/paulboone/ticgit.git
###### Compartir a tus archivos remotos:
    $ git push origin master
###### Traer cambios remotos al local:
    $ git pull origin master
 **Git pull** is actually equivalent to the following two steps:
 
     git fetch
     git merge origin/master

###### Deshacer commits (De forma seguro a no tan segura):
###### 	Volver a un commit de atras pero no deshacer :  
    $ git checkout #codigocommit#
###### - Volver al último commit: 

    $ git checkout master

###### - 	Revertir el efecto hasta un determinado commit, y al hacerlo lo guarda en un nuevo commit: 

    $ git revert #codigocommit#

###### - 	Deshacer el cambio hasta un commit por completo (sin el hard, solo lo saca del stage pero en el editor no se actualiza):  

        git reset #codigocommit# --hard
###### Crear branch: 
    $ git branch “nombre”
###### Listar Branches:
    $ git branch -a
###### Cambiar a un branch: 
    $ git checkout “nombrebranch”
###### Eliminar branch local: 
    $ git branch –D “nombrebranch”
###### Eliminar branch remoto:
    $ git push origin :”nombre-rama”
###### Crear e ir al branch creado: 
    $ git checkout –b “nombrebranch”
###### Traer los cambios de una rama al master: 
    $ git merge “nombreramaafusionar”

###### * Pasar el contenido del branch al master:--------->*
    git checkout rama
    git merge -s ours master
    git checkout master
    git merge rama
    
###### Ignorando archivos:
A menudo tendrás un tipo de archivos que no quieras que Git añada automáticamente o te muestre como no versionado. Estos arhivos se guardan en .gitignore.

*EN CASO DE CONFLICTO, SOLUCIONAR CON LA HERRAMIENTA DE SOLUCION DE CONFLICTOS Y GUARDAR EL COMMIT SIN MENSAJE . PARA SALIR DEL EDITOR DE MENSAJE = :WQ*
###### Comandos extras de cmd:
    Cd “dirección” = Mover entre carpetas
    Cd .. = retroceder un nivel
    Ls = listar archivos en una ruta
    Rm “archivo” = remover archivo
    Rmdir “test” = remover directorio
