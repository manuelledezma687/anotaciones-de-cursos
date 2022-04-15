
#CURSO DE DOCKER | APUNTES I PARTE.


##GRANDES PROBLEMAS DEL SOFTWARE.
    -Construir, Distribuir y ejecutar.
    -Virtualización es la versión virtual de algún recurso físico. Permite atacar los 3 problemas del software.
    -Los contenedores son de flexibles, escalables, ligeros, de bajo acoplamiento, portables y seguros.

##EL CORAZÓN DE DOCKER.
    Componentes DENTRO del circulo de Docker:

    *Docker daemon* Es el centro de docker, el corazón que gracias a el, podemos comunicarnos con los servicios de docker.
    *REST API* Como cualquier otra API, es la que nos permite visualizar docker de forma “gráfica”.
    *Cliente de docker* Gracias a este componente, podemos comunicarnos con el corazón de docker (Docker Daemon) que por 
    defecto es la línea de comandos.

    Dentro de la arquitectura de Docker encontramos:

    *Contenedores* Es la razón de ser de Docker, es donde podemos encapsular nuestras imagenes para llevarlas a otra computadora, 
    o servidor, etc.
    *Imagenes* Son las encapsulaciones de x contenedor. Podemos correr nuestra aplicación en Java por medio de una imagen, podemos 
    utilizar Ubuntu para correr nuestro proyecto, etc.
    Volumenes de datos: Podemos acceder con seguridad al sistema de archivos de nuestra máquina.
    *Redes* Son las que permiten la comunicación entre contenedores.

##ESTRCUTURA DE UN CONTENEDOR.
   | CONTAINER ID | IMAGE | COMAND | CREATED | STATUS | PORTS | NAMES 

##DOCKER COMANDOS BASICOS.
    docker --version . para ver la version de docker.
    docker run hello-world . correr la imagen de hello world (si no la tiene l descarga).
    docker ps . muestra los contenedores activos. 
    docker ps -a . (all) muestra todos los contenedores.APAGADOS O NO.
    docker inspect <name>. muestra detalle de los contenedores.(tipo json).
    docker run --name helllo-platzi hello-word . ejemplo para renombrar un contenedor.No se pueden tener 2 contenedores con la misma 
        instalación.
    docker rename hello-platzi hola-platzi. renombrar
    docker rm <id o name> . borrar contenedor.
    docker container prune . Borrar todos los contenedores, te devuelve los id de los contenedores borrados.
    --name . bandera del nombre
    -f . follow
    -d . detach

##DOCKER EJEMPLO PARA CORRER UBUNTU.
    docker run ubuntu. correr ubuntu. (lo corre y lo descarga si no está)
    docker run -it ubuntu (o cualquier otro os) . corre ubuntu en forma interactiva.
    exit . salir del contenedor

    Bonus.
    cat /etc/lsb-release
    Ver información del OS en unix/linux

##CICLO DE VIDA DE UN CONTENEDOR.
    docker run --name alwaysup -d ubuntu tail -f /dev/null . me escupe el id del container y me corre su proceso (seguirá prendido 
        hasta que se detenga manualmente)
    docker exec . en un contenedor existente ejecutar un comando o proceso.
    docker exec -it alwaysup bash . estoy dentro de ubuntu (ejemplo)
    docker inspect --format '{{.State.Pid}}' alwaysup .saber el process id de un proceso, escupe el id.
    kill -9 <id> . matar proceso en linux (sudo)
    docker stop alwaysup  . ejemplo para parar el container

##EXPONIENDO CONTENEDORES.
    docker run -d -name proxy nginx . (detach no vincula el contenedor)
    docker stop proxy . apaga el contenedor (en torno a los puertos el primer puerto corresponde a la remota y pueden haber varios 
        contenedores apuntando al mismo pero uno solo puede entrar)
    docker rm proxy . borra el proxy
    docker run -d -name proxy -p 8080:80 nginx .expone en mi puerto 8080 el nginx y en la terminal salen los logs.
    docker run --name proxy -d -p 8080:80 nginx . escupe el id corre pero no toma la terminal.
    docker logs proxy . para ver los logs. (con -f se veran todos "follow")
    docker logs -tail 10 -f proxy . ejemplo para ver los ultimos 10 logs.

##BIND MOUNTS Y VOLUMENES.
    *Bind Mounts* compartir la ruta de un directorio con un contenedor, se hacen colocando la bandera -v luego el path : y luego la ruta
    dentro del contenedor y luego el nombre del contenedor.
    y  volumenes (no son visibles para nosotros)
    docker volume ls (listo los volumes)
    docker volume create <volume> . crear un volumen
    docker run -d --name db --mount src=dbdata,dst=/data/db mongo .Creamos un contenedor con este volumen

    docker exec -it db bash
    # mongo
    > use platzi
    > db.users.insert({"nombre": "Boris"})
    > db.users.find()
    > exit
    # exit
    docker rm -f db
    *Ejemplo de insertar datos*


    docker run -d --name db --mount src=dbdata,dst=/data/db mongo
    docker exec -it db bash
    # mongo
    > use platzi
    > db.users.find()
    *Ejemplo de verificar*

    docker exec -it copytest bash . ejeplo para entrar a la bash y copiar datos.

    docker cp . copiar en docker. Ejemplo:
    docker cp prueba.txt copytest:/ejemplo.txt  // COPIAR UN ARCHIVO AL CONTENEDOR
    docker cp copytest:/ejemplo.txt localtesting . al reves (se pueden copiar archivos y directorios)
    /*Contenedor tiene dos formas de acceder a los datos la primera es Bind Mount la cual  vincula el sistema de archivos 
    con el contenedor, volume es lo mismo pero el area del filesystem esta manejada por docker, y temporaly file system es
     de linux es un volumen pero que solo existe en memoria del contenedor*/

##CURSO DE DOCKER | APUNTES II PARTE.
       
##IMÁGENES.
    Son Piezas de software (plantilla)que tienen todo lo necesario para replicar el funcionamiento del mismo.
    docker image ls . listas las imágenes en Docker.
    docker pull <image>:<tag_version> . descargar desde docker-hub.

##CREAR UNA IMAGEN (PRÁCTICA).
    mkdir images .Se crea un directorio.
    cd imagenes . se accede al directorio.
    touch Dockerfile .se crea un archivo llamado Dockerfile (code)

    //////
    Contenido del Dockerfile:
    FROM ubuntu:latest 
    RUN touch /ust/src/hola-platzi.txt        # este comando se ejecutará en tiempo de build
    ///////

    docker build -t ubuntu:platzi . /Se crea una imágen, se le pasa el contexto de build, de ultimo se coloca la ruta en este caso se coloco un punto
    porque estamos en la ruta parados. cada id es una capa (cada instrucción)
    docker run -it ubuntu:platzi  .Iniciamos una conexión por terminal al contenedor de ubuntu
    docker run --rm -p 3000:3000 <imagen>.lo ejecuta pero al final que termina borra el container.
    EXPOSE  . EXPONER EN EL PUERTO
    CMD .  EL PRINCIPAL COMANDO

    Publicar una imagen (push pull parecido a git)
    docker login . loguearse con las credenciales de dockerhub.
    docker tag ubuntu:platzi miusuario/ubuntu:platzi .Para poder publicar nuestro contenedor, es necesario cambiar el tag ubuntu, 
        dado que el mismo ya existe como un contenedor oficial y no tenemos permisos para modificarlo.
    docker push miusuario/ubuntu:platzi .comando para hacer la publicación de nuestra imágen en docker hub.


//Ejemplo de Dockerfile:
    FROM node:current
    WORKDIR/usr/app/server
    COPY["package.json", "package-lock.json", "."]
    RUNnpm install
    COPY[".", "."]
    RUNnpm run build
    COPY[".env", "./build"]
    EXPOSE3500
    CMD node src/index.js   //CMD se utiliza para ejecutar un comando por defecto, cuando se crea el contenedor. Es bastante versátil, 
    ya que podemos pasarle argumentos al correr el contenedor y podemos sobreescribirlo con facilidad.

##CAPAS EN LAS IMÁGENES EN DOCKER.
    EL sistema de capas es muy parecido al de git.Cada capa almacena un cambio.
    docker history <image> . consultar las capas de abajo hacia arriba, util para entender las capas.
    docker pull .traerse la imagen del repositorio.
    docker commit . hacer un commit con nuevos cambios. (previo docker run -it .Ejemplo: docker run -it cf0f3ca922e0 bin/bash)
    dive <nombre_de_imagen> . (instalarlo previamente) vision mas estructurada y visible de nuestras imagenes.

##EL CACHÉ EN DOCKER.
    Docker aprovecha las capas que ya tiene para no repetir descargar algo sino aprovechar el caché.
    La clave está en estructurar nuestro Dockerfile de manera de que primero se copien todas las 
    dependencias y posteriormente nuestro código fuente, que es el mas suceptible a cambios.

##COLABORACIÓN ENTRE COLABORADORES Y NETWORK.
    docker network ls . listar networks.
    docker network inspect <name_container>
    docker network connect <contenedornuevo_receptora> <contenedorparaconectar>  . conectar red.
    docker run -d --name app -p 3000:3000  --env <nombre_variable_de_entorno EJEMPLO "MONGO_URL=mongodb://db:27017/test platziapp"> 
        test = base de datos
        platziapp = nombre de la imagen
    
##DOCKER COMPOSE.
    Docker compose es una herramienta que nos permite describir de forma declarativa la arquitectura de nuestra aplicación, 
    utiliza compose file (docker-compose.yml).
    Un servicio es una parte de una aplicacion puede tener 1 o 2 contenedores de la misma imagen.
    //Ejemeplos de un Docker compose

    Se debe especificar las versiones en los yamels (no colocar lastest)
    
    version: "3.8"

    services:
        app:
            image: platziapp
            environment:
              MONGO_URL: "mongobd://db:27017/test"
            depends_on:
              -db
              ports:
                -"3000:3000"
              volume:
                -.:/usr/src
                -/usr/src/node_modules
              command: (para renombrar entrypoint override)

        db:
          image: mongo


    ///////
    IMPORTANTE DOCKER COMPOSE TRABAJA CON SERVICIOS, NO CON CONTAINERS.

##COMANDO DOCKER COMPOSE.
    docker compose up .levantar docker compose
    docker compose up -d .levantar pero con detach para no ocupar con los logs.
    docker-compose logs (veo todos los logs)
    docker-compose logs app (solo veo el log de “app”)
    docker-compose logs -f app (hago un follow del log de app)
    docker-compose exec app bash (entro al shell del contenedor app) en docker compose no hace falta la flag -it
    docker-compose ps (veo los contenedores generados por docker compose)
    docker-compose down (borro todo lo generado por docker compose)
    docker-compose build (crea las imágenes o rebuild)
    $ docker-compose up -d --scale app=2 (escalo dos instancias de app, previamente tengo que definir un rango de puertos en el archivo compose)

##OVERRIDE.
    docker-compose.override.yml es un archivo que se encarga de sobreescribir tu configuración de docker-compose.yml , 
    se puede usar para tener segura tu configuración y para no guardar los cambios en el repositorio de git.
    Un equivalente podría ser los archivos de declaración de variables de entorno, donde hay un archivo .env declarando su 
    nombre y valor, y hay una copia .env.example con solo las variables sin valor. En .gitignore se declara que los cambios 
    en .env no serán guardados, pero mandamos el archivo de ejemplo al repositorio.

##ADMINISTRACIÓN DEL AMBIENTE EN DOCKER.
    docker rm -f $(docker ps -aq) (borra todos los contenedores que estén corriendo o apagados)
    docker system prune (borra todo lo que no se esté usando)
    docker run -d --name app --memory 1g platziapp (limito el uso de memoria)
    docker stats (veo cuantos recursos consume docker en mi sistema)
    //prune para networks, volume, container, system
    docker ps -l muestra el último contenedor creado incluyendo todos los estados.

##SHELL VS EXEC.
    EXEC FORM : ANOTAR LOS COMANDOS CON LOS CORCHETES Y LAS COMILLAS
    SHELL FORM: QUEDA COMO UN SUBCOMANDO EN LA SHELL
    docker build -t loop . (construyo la imagen)
    docker run -d --name looper loop (corro el contenedor)
    docker stop looper (le envía la señal SIGTERM al contenedor)
    docker ps -l (muestra el ps del último proceso)
    docker kill looper (le envía la señal SIGKILL al contenedor)
    docker exec looper ps -ef (veo los procesos del contenedor)
                
##ENTRYPOINT VS CMD.
    El ENTRYPOINT es el comando que se va a ejecutar por defecto, y en CMD va el parametro del comando.
    Este parametro se puede modificar desde el run del contenedor.



























 

    









