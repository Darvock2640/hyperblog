# Comando para GIT 

* Crear git en el directorio actual
    ```
    git init
    ```
* Verificar el estado del git (archivos sin guardar, archivos sin tracking etc ...)
    ```
    git status
    ```
* Agregar un archivo al git
    ```
    git add	<archivo>
	```
* Eliminar el archivo del tracking de git
    ```
    git rm --cached <archivo>
	```
* Guardar los cambios en el repositorio y adicionar un mensaje
    ```
    git commit -m "mesage"
	```
* Mostrar la configuración de git
    ```
    git config --list
    ```
* Configurar el nombre de la persona para git
    ```
    git config --global user.name "nombre"
	```
* Configurar el correo de la persona para git
    ```
    git config --global user.email "su.correo@correo.co"
	```
* Adicionar todos los cambios al tracking del git
    ```
    git add .
	```
* Mostrar todos los cambios al archivo
    ```
    git log <archivo>
    ```
* Mostrar los cambios al repositorio con detalles
    ```
    git log --stat
	```
* Volver a la versión identificada por el log id, todo cambio posterior es eliminado
    ```
    git reset <log id> --hard
	```
* volver a la versión identificada por el log id, todo cambio posterior es eliminado pero queda una version en stage
    ```
    git reset <log id> --soft
    ```
* Ver el archivo en la versión especificada por el log id
    ```
    git checkout <log ID> <archivo>
	```
* Moverse entre branhces y master
    ```
    git checkout <branch/master>
	```
* Traer el archivo del ultimo master
    ```
    git checkout master <archivo>
    ```
* Crear una copia de un repositorio remoto en el pc local
    ```
    git clone <url>
	```
* Después de hacer add y commit, git push sube al repositorio remoto todos los cambios del PC local
    ```
    git push
    ```
* Actualizar el repositorio local pero sin moopdificar los archivos locales del directorio de trabajo
    ```
    git fetch
    ```
* Toma el estado actual del repositorio (versiones de archivos) y los aplica al directorio local
    ```
    git merge 
	```
* Para unificar los cambios de un branch al master, debes estar en el master y hacer un merge con el nombre del branch
    ```
    git merge <branch>
	```
* Para realizar un git fetch y merge al mismo tiempo
    ```
    git pull
	```
* Permite hacer un commit sin hacer add (unicamente a archivos a los que una ves ya se les hizo add)
    ```
    git commit -am
	```
* Mostrar los ultimos cambios del head
    ```
    git show 
    ```
* Mostrar los ultimos cambios de <archivo> 
    ```
    git show <archivo>
    ```
* Mostrar las diferencias en el ultimo cambio al head
    ```
    git diff
	```
* Mostrar las diferencias en el ultimo cambio a <archivo>
    ```
    git diff <archivo>
    ```
* Mostrar las diferencias entre los commits
    ```
    git diff <commit_ID> <commit_ID>
    ```
* Crear un branch con el <nombre> asignado
    ```
    git branch <nombre>
	```
* Ver todos los branchs tanto remotos como locales 
´´´
git branch -a
´´´
* Traer los elementos del repo en github como origin
    ```
    git remote add origin <url del repo en github>
    ```
* Mostrar que acciones puedo o tengo pendientes con un repo remoto
    ```
    git remote -v 
    ```
* Hacer pull desde el repositorio remoto para poder integrarlo con el repositorio local
    ```
    git pull origin master
    ```
* Si el comando anterior pone problema por la historia
    ```
    git pull origin master --allow-unrelated-histories
    ```
* Llevar los cambios del repositorio local al repositorio remoto
    ```
    git push origin master
    ```
* Mostrar el log de los cambios del repo con detalles
    ```
    git log --all 
    ```
* Mostrar el log de los cambios del repo con detalles y una grafica de los branches
    ```
    git log --all --graph
    ```
* Mostrar el log de los cambios del repo con detalles y una grafica de los branches de manera más comprimida
    ```
    git log --all --graph --decorate --oneline	
	```
* Agregar tags a un commit especifico del proyecto
    ```
    git tag -a <"nombre_del_tag"> -m <"mensaje del tag"> <hash - numero del commit>
	```
* ver los tags creados
    ```
    git show-ref --tags
	```
* Enviar los tags al repo remoto
    ```
    git push origin --tags
	```
* Ver los tags existentes
    ```
    git tag
	```
* Eliminar un tag
    ```
    git tag -d <nombre_del_tag>
	```
* Eliminar un tag definitivamente en github
    ```
    git push origin :refs/tags/<nombre_del_tag>
	```
* Mostrar en detalle todas las ramas del repo
    ```
    git show-branch --all
	```
* Realiza un rebase (una copia forzada - modificación de la historia) de la rama actual a la rama <branch>
siempre primero hacer el rebase desde la rama que quiero a la rama que voy a desaparecer de la historia
    ```
    git rebase <branch>
	```
* Hace un guardado temporal de cambios que no quiero realizar commit aun
    ```
    git stash
	```
* Muestra todos los stash 
    ```
    git stash list 
	```
* Reactiva los cambios temporales del stash
    ```
    git stash pop 
	```
* Guarda el stash en la rama <nombre de la nueva rama>
    ```
    git stash branch <nombre de la rama>
	```
* Borra el stash
    ```
    git stash drop
	```
* Hace un listado de los elementos que se pueden eliminar del repositorio
    ```
    git clean --dry-run
	```
* Forza la eliminación de archivo (los que git considera se pueden borrar, de acuerdo con el comando de arriba)
    ```
    git clean -f
	```
* Trae al header los cambios de commit idetificado por <commit_ID>
    ```
    git cherry-pick <commit_ID>
	```
* Muestra absolutamente todos los heads que han ido muriendo con el tiempo (realmente muestra todo)
    ```
    git reflog
	```
* Hace un hard reset al commit identificado por <commit_ID>
    ```
    git reset --hard <commit_ID>
	```
* Busca coincidencias de <texto> en el proyecto y muestra en que archivo está
    ```
    git grep <texto>
	```
* Busca coincidencias de <texto> en el proyecto y muestra en que archivo y en que línea está
    ```
    git grep -n <texto>
	```
* Busca coincidencias de <texto> en el proyecto y muestra en que archivo está y cuantas veces sse repite
    ```
    git grep -c <texto>
	```
* Busca las coincidencias de <"texto"> en el log del proyecto y los muestra
    ```
    git log -S <"texto">
	```
* Muestra todos los commits hechos por los miembros del grupo de trabajo
    ```
    git shortlog
	```
* Muestra quienes del grupo de trabajo han hecho commits y cuantos han hecho
    ```
    git shortlog -sn
	```
* Muestra todo de shortlog
    ```
    git shortlog -sn --all
	```
* Muestra todo lo de shortlog excepto los merges
    ```
    git shortlog -sn --all --no-merges
	```
* Muestra quien ha hecho los cambios en <archivo>
    ```
    git blame <archivo>
	```
* Muestra quien ha hecho los cambios en <archivo> de forma más organizada
    ```
    git blame -c <archivo>
	```
* Muestra quien ha hecho los cambios en <archivo> desde la linea #1 hasta la linea #2
    ```
    git blame <archivo> -L#1,#2
	```
* Muestra la ayuda del commando
    ```
    git <command> --help
	```
* Ver las ramas remotas
    ```
    git branch -r
	```
* Ver todas las ramas (locales en blanco, remotas en rojo)
    ```
    git branch -a
	```
## Que hacer cuando quiero corregir un commit?
Si por ejemplo olvide hacer un cambio que dije que si lo había hecho en el commit primero debo corregir el cambio y realizar un add con el siguiente comando

	git add <archivo>

y Luego "remendar" el commit con el comando 

	git commit --amend

## Acciones dentro de git
"q" para salir de los list o logs

## Alias
```
git config --global alias.<nombre_alias> <"command">
```
Crea un alias pero no dentro de la consola si no en la configuración de git ejemplo:
    
	git config --global alias.stats "shortlog -sn --all --no-merges"
    
El comando anterior crea el alias **"git stats"** para el comando 

    
    "git shortlog -sn --all --no-merges"
    
por lo tanto para ejecutar el alias solo deberia hacer
   
    git stats
