#Comandos de Git

**git init** --> inicializar un repositorio de git.

**ls -al** --> ver archivos oclutos en la carpeta (archivo .git). 

**git add [nombre archivo]** --> Agrega archivo al repositorio.

**git status** --> Revisa el estado de los archivos que estan dentro del repositorio.

**git rm --cached [nombre del archivo]** --> Desadjunta el archivo del repositorio, mas no lo elimina.

**git rm [nombre del archivo]** --> Si el archivo no esta en cache, desadjunta el archivo del repositorio, mano lo elimina.

**git commit -m "Aqui val el mensaje"** --> Envia los cambios al repositorio local.

**git config** --> lista la configuracion de git.

**git config --list** --> list la configuracion por defecto que tiene git.

**git config --list --show-origin** --> lista donde estan guardadas las configuraciones que tiene git.

**git config --global user.name "Nombre de usuario"** --> asigna el nombre de usuario al repositorio.

**git config --global user.email "correo electronico"** --> asigna el correo electronico al usuario al repositorio.

**git add .** --> guardar los cambios de todos los archvios que han sufrido modificaciones.

**git log [nombre del archivo]** --> muestra el historial de modificaciones del archivo.

**git show** --> muestra los cambios que han existido en el repositorio.

**git diff [id commit] [id commit]** --> realiza la comparacion entre dos commits.

**git reset [id commit] --hard** --> vuelve a la version indicada, borrando todos cambios lo que tenga.

**git reset [id commit] --soft** --> vuelve a la version indicada, mantiene los cambios que esten en staging.

**git diff** --> muestra la diferencias entre los archivos stage y archivos unstage.

**git rm** --> elimina archivos de Git sin eliminar su historial del sistema de versiones.

**git branch [nombre de la rama]** --> Crea una rama.

**git checkout [nombre de la rama]** --> Cambia a la rama.

**git commit -am** --> hace git commit + git add si los archivos han sido previamente creados.

**git branch [name branch]** --> crea una rama apartir de la rama donde estamos ubicados.

**git merge [nombre de la rama]** --> hace una fusion entre dos ramas. 
Normalmente se trae los cambios de la rama mencionada hacia la rama donde estamos ubicados.
 (E.g. si estoy en master trae los cambios de la rama mencionada hacia master).

**git branch** --> lista las ramas que estan creadas.
# **configurar tus llaves ssh en local**
- las llaves son por usuario.
- es recomendable crear las llaves en el home (~).
- es necesario que el email del usuario de github sea el mismo que esta en la configuracion local de git.

**ssh-keygen -t rsa -b 4096 -C "[correo electronico]"** --> comando para crear la llave ssh en el ambiente local.
- la llave public tiene como extension .pub
- la llave public se ebe de llevar a github

**eval $(ssh-agent -s)** --> comando para verificar que el servidor de ssh este corriendo (aplica para entornos windows).

**eval "$(ssh-agent -s)"** --> comando para verificar que el servidor de ssh este corriendo (aplica para entornos Mac).

- para ambientes Mac es necesario que exista un archivo .config en la carpeta donde estan las llaves. 
Sino existe se debe de crear. El archivo debe de contener lo siguiente:

**
Host *
        AddKeysToAgent yes
        UseKeychain yes
        IdentityFile [ruta donde estan las llaves + nombre de la llave privada]
**
- guardar sin extension.

**ssh-add [ruta donde esta la llave privada]** --> comando para agregar la llave (aplica para entorno windows).

**ssh-add -K [ruta donde esta la llave privada]** --> comando para agregar la llave (aplica para entorno MacOs).

**git remote set-url origin [url en https or ssh]** --> comando para cambiar la url de los repositorios remotos.

**git log --all --graph** --> comano para pintar los todos los commits de manera grafica.

**git log --all --graph --decorate --oneline** --> commando para visualizar la historia de los commits en una sola linea de manera grafica.

**alias [nombre] ["comando git"]** --> se usa para dar alias a comandos largos en git.

**git log --all --graph** --> se usa para mostrar graficamente como funciona los branches.

**git log --all --graph --decorate --onleline** --> muestra toda la historia del branch de manera grafica con commits.

**git tag -a [nombre version] -m "Mensaje del tag" [#id commit]** --> comando para crear tags basados en versiones.

**git tag** --> mustra un listado de todos los tags configurados en el branch.

**git show-ref --tags** --> muestra que commit esta asociado a un tag especifico.

**history** -- muestra el historial de comandos digitados en la consola.

**git push origin --tags** --> enviar cambios de los tags a la branch remoto.

**git tag -d [nombre del tag]** --> comando para borrar un tag local.

**git push origin :refs/tags/[nombre del tag]** --> comando para eliminar un tag a nivel remoto.

**git show-branch** --> muestra las ramas existentes y su historia.

**git show-branch --all** --> muestra las ramas existentes y su historia con mas detalles.

**gitk** --> abre un IDE grafico para la gestion y manejo de ramas.

**git clone [url del proyecto de github]** --> comando que sirve para clonar los repositorios desde github. 
Unicamente funciona para proyecto publicos.

**space + shift + z + z** --> comando para salir ddel editor de la consola.

**git remote add upstream [url repositorio original]** --> comando para agregar los repositorios remotos 
(cuando se trabaja con forks)

**git remote remove upstream** --> comando para remover los upstream.

