#CURSO DE GIT Y GITHUB.


##COMANDOS BÁSICOS.
    *git init* lo usamos para determinar la carpeta en la que vamos a trabajar.
    *git status* lo usamos para saber si tenemos un archivo añadido o borrado en nuestro
    proyecto, para saber en la rama en la que estamos y si tenemos commits.
    *git add* es para añadir un archivo a nuestra rama seguidamente ponemos entre
    comillas el nombre de nuestro archivo o poner un punto para añadir todos los
    archivos de nuestra carpeta.
    *git rm* lo usamos para borrar un archivo que hayamos añadido, para eliminarlo por
    completo de nuestra rama usamos git rm --cached. Otros casos:
    - git rm --force: Elimina los archivos de Git y del disco duro. Git guarda el
    registro de la existencia de los archivos, por lo que podremos recuperarlos si
    es necesario (pero debemos usar comandos más avanzados).
    *git commit* se usa para añadir un commit a nuestra rama, también podemos ponerle un
    -m (MENSAJE)seguidamente ponemos entre comillas nuestro mensaje.
    *git config* muestra configuraciones de git también podemos usar –list para mostrar la
    configuración por defecto de nuestro git y si añadimos --show-origin inhales
    nos muestra las configuraciones.
    *git config -- global user.name:* cambia de manera global el nombre del usuario, 
    seguidamente ponemos entre comillas nuestro nombre.
    *git config --global user.email:* cambia de manera global el email del usuario, seguidamente 
    ponemos entre comillas nuestro nombre.
    *git log:* se usa para ver la historia de nuestros archivos, los commits, el usuario que lo
    cambió, cuando se realizaron los cambios etc. seguidamente ponemos el
    nombre de nuestro archivo.
    *git show* nos muestra los cambios que han existido sobre un archivo
    *git nombre-del-archivo-o-carpeta* para añadir archivos y carpetas individuales o git add -A para 
    mover todos los archivos de nuestro proyecto (tanto Untrackeds como unstageds).
    *git reset HEAD* nos ayuda a sacar archivos del estado Staged para devolverlos a su estado
    anterior. Si los archivos venían de Unstaged, vuelven allí. Y lo mismo se venían
    de Untracked.
        git reset --hard: Borra todo. Todo todito, absolutamente todo. Toda la información de los
        commits y del área de staging se borra del historial.

        git reset --soft: Borramos todo el historial y los registros de Git pero guardamos 
        los cambios que tengamos en Staging, así podemos aplicar las últimas actualizaciones a
        un nuevo commit.
    *git checkout rama* Cambiar de rama en git para ver últimos commits etc.
    *git pull* traerse cambios de una rama remota.
    *git push* subir cambios a una rama remota. Ejemplo: git push origin master.

##LLAVES SSH.
    *Generar tus llaves SSH.* ssh-keygen -t rsa -b 4096 -C "tu@email.com"
    *Encender el "servidor" de llaves SSH de tu computadora* eval $(ssh-agent -s)
    *Añadir tu llave SSH a este "servidor"* ssh-add ruta-donde-guardaste-tu-llave-privada

##COMANDOS PARA TRABAJAR CON ETIQUETAS.
    *git tag o git show-ref --tags* Listar los tags de nuestro repositorio local.
    *git tag -a nombre-del-tag id-del-commit* Crear un nuevo tag y asignarlo a un commit.
    *git tag -d nombre-del-tag* Borrar un tag en el repositorio local.
    *git push origin --tags* Publicar un tag en el repositorio remoto.
    *git tag -d nombre-del-tag y git push origin :refs/tags/nombre-del-tag* Borrar un tag del repositorio remoto.


##OTROS COMANDOS ÚTILES.
    *git commit --amend* amend en inglés es remendar y lo que hará es que los cambios que
    hicimos nos los agregará al commit anterior.
    *.gitignore Documento para "ignorar archivos".*
    *git clean --dry-run* Para saber qué archivos vamos a borrar tecleamos.
    *git clean -f* Para borrar todos los archivos listados (que no son carpetas) tecleamos-

##MALAS PRÁCTICAS EN GIT
    *git rebase master* Aplicamos rebase para traer los cambios de la rama que queremos
    *git cherry-pick IDCommit* Existe un mundo alternativo en el cual vamos avanzando en una rama
    pero necesitamos en master uno de esos avances de la rama, para eso
    utilizamos el comando
    *cherry-pick* es una mala práctica porque significa que estamos reconstruyendo la
    historia, usa cherry-pick con sabiduría. Si no sabes lo que estás
    haciendo ten mucho cuidado.

##GIT COMANDOS Y RECURSOS COLABORATIVOS.
    *git shortlog -sn* muestra cuantos commit han hecho cada miembros del equipo.
    *git shortlog -sn --all* muestra cuantos commit han hecho cada miembros del equipo
    hasta los que han sido eliminado.
    *git shortlog -sn --all --no-merge* muestra cuantos commit han hecho cada miembros quitando
    los eliminados sin los merges
    *git blame ARCHIVO* muestra quien hizo cada cosa linea por linea.
    *git COMANDO --help* muestra como funciona el comando.
    *git branch -r* se muestran todas las ramas remotas.
    *git branch -d <branch>* se borra la rama enunciada(-D borrado fuerte).
    *git branch -a* se muestran todas las ramas tanto locales como remotas.
    *git blame ARCHIVO* -linea_inicial,linea_final= muestra quien hizo cada cosa linea
    por linea indicándole desde que linea ver ejemplo -L35,50.





