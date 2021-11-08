#Comandos de Git

**git init** --> inicializar un repositorio de git
**ls -al** --> ver archivos oclutos en la carpeta (archivo .git)
**git add [nombre archivo]** --> Agrega archivo al repositorio
**git status** --> Revisa el estado de los archivos que estan dentro del repositorio
**git rm --cached [nombre del archivo]** --> Desadjunta el archivo del repositorio, mas no lo elimina.
**git rm [nombre del archivo]** --> Si el archivo no esta en cache, desadjunta el archivo del repositorio, mano lo elimina.
**git commit -m "Aqui val el mensaje"** --> Envia los cambios al repositorio local
**git config** --> lista la configuracion de git
**git config --list** --> list la configuracion por defecto que tiene git
**git config --list --show-origin** --> lista donde estan guardadas las configuraciones que tiene git
**git config --global user.name "Nombre de usuario"** --> asigna el nombre de usuario al repositorio
**git config --global user.email "correo electronico"** --> asigna el correo electronico al usuario al repositorio
**git add .** --> guardar los cambios de todos los archvios que han sufrido modificaciones
**git log [nombre del archivo]** --> muestra el historial de modificaciones del archivo
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
**git merge [nombre de la rama]** --> hace una fusion entre dos ramas. Normalmente se trae los cambios de la rama mencionada hacia la rama donde estamos ubicados. (E.g. si estoy en master trae los cambios de la rama mencionada hacia master).
**git branch** --> lista las ramas que estan creadas.