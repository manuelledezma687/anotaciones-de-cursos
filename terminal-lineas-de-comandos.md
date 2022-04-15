
# CURSO DE TERMINAL Y LINEAS DE COMANDOS.


## DESCRIPTORES DE RUTA.

    / Ruta raíz del sistema.
    . Directorio actual.
    .. Directorio anterior.
    ~ Directorio home del usuario.

## ATAJOS DEL TECLADO.

    CTRL-C Termina el proceso de un comando en la terminal.
    CTRL-D Termina el input de un comando.
    CTRL-A Avanza al inicio de línea.
    CTRL-E Avanza al final de línea.
    CTRL-L Limpia la pantalla de la terminal.

## OPERACIONES CON DIRECTORIOS.

    *pwd* Imprime el directorio actual.
    *mkdir dir1* Crea el directorio con nombre dir1.
    *cd dir1* Cambia al directorio con nombre dir1.
    *cd ../..* Cambia dos directorios anteriores del actual.
    *cd* Cambia al directorio home del usuario.
    *ls* Muestra archivos y directorios.
    *tree /ruta* Muestra todos los archivos y directorios anidados dentro de la ruta a cualquier
    nivel de profundidad.
    *tree -L 2* . Muestra todos los archivos y directorios anidados dentro de la ruta actual a dos niveles
    de profundidad.

## OPERACIONES DE ls.

    -a Muestra todo (incluyendo archivos ocultos).
    -R Muestra una lista de manera recursiva.
    -r Muestra listando de forma inversa.
    -t Muestra los últimos modificados.
    -S Muestra ordenando por tamaño.
    -l Muestra usando un formato largo.

## MANIPULACIÓN DE ARCHIVOS Y DIRECTORIOS.

    *touch newFile* Crea un nuevo archivo llamado newFile.
    *file mi_archivo* Muestra las características de mi_archivo.
    *cp file1 /destino* Copia el archivo file1 a la ruta /destino.
    *cp -r dir1 dir1_cp* Copia el directorio dir1 y su contenido a uno nuevo llamado dir1_cp.
    *mv file1 /destino* Mueve el archivo file1 a la ruta /destino.
    *mv file1 ok_file* Renombra el archivo file1 al nombre ok_file.
    *rm file1* Elimina el archivo file1.
    *rm -ri dir1* Elimina el directorio dir1 y su contenido de forma interactiva.
    *rm -r dir1* Elimina el directorio dir1 y su contenido de forma directa.
    *ln -s file link_name* Crea un link simbólico al archivo.
    *open filename* Abre el archivo con el programa predeterminado (MacOS).
    *xdg-open filename* Abre el archivo con el programa predeterminado (mayoría de sistemas Linux).

## MANIPULACIÓN DE ARCHIVOS DE TEXTO.

    *head file.txt* Muestra las primeras 10 líneas de texto del archivo file.txt.
    *head -n 20 file.txt* Muestra las primeras 20 líneas de texto del archivo file.txt.
    *tail file.txt* Muestra las últimas 10 líneas de texto del archivo file.txt.
    *tail -n 20 file.txt* Muestra las últimas 20 líneas de texto del archivo file.txt.
    *less file.txt* Explora el contenido de archivo con paginación.
    *cat file1 file2* Concatena el contenido de file1 y file2 a la salida de la terminal.

## EXPLORACIÓN DE COMANDOS Y AYUDA DENTRO DE LA TERMINAL.

    *man* command Muestra el manual de usuario del comando.
    *help* command Muestra ayuda para el comando (sólo funciona si la shell es Bash).
    *which* command Muestra la ruta de donde se encuentra el ejecutable del comando.
    *whatis* command Muestra brevemente la función del comando alias aliasname=”command” Crea un alias para el comando.
    *alias l=”ls -la”* Crea un alias para el comando ls con opciones llamado l .

## WILDCARDS.

    * Coincide con cualquier carácter.
    ? Coincide con cualquier carácter individual.
    [caracteres] Coincide con cualquier carácter que sea miembro del conjunto caracteres.
    [!caracteres] Coincide con cualquier carácter que no sea miembro del conjunto caracteres.
    [[:clase:]] Coincide con cualquier carácter de la clase.

## CLASES DENTRO DE LAS WILDCARDS.

    [:alnum:] Coincide con cualquier carácter alfanumérico.
    [:alpha:] Coincide con cualquier carácter alfabético.
    [:digit:] Coincide con cualquier número.
    [:lower:] Coincide con cualquier letra minúscula.
    [:upper:] Coincide con cualquier letra mayúscula.

## REDIRECCIONES I/O Y OPERADORES DE CONTROL.

    *comando < archivo* Redirige el input de un comando hacia un archivo.
    *comando > archivo* Redirige la salida de un comando a un archivo (usarse con cuidado porque 
    sobrescribe el sistema).
    *comando >> archivo* Concatena la salida de un comando a un archivo. Si no existe lo crea.
    *comando 2> error.txt* Redirige la salida de error de un comando al archivo error.txt.
    *comando1 | comando2* Redirige la salida del comando1 a la entrada del comando2.
    *comando1; comando2* Ejecuta de manera consecutiva.
    *comando1 & comando2* Ejecuta de manera asíncrona.
    *comando1 && comando2* Ejecuta el comando2 si y solo si el comando1 se ejecutó de manera exitosa.
    *comando1 || comando2* Ejecuta el comando1 o el comando2.

## MANEJO DE PERMISOS Y USUARIOS.

    Tipo de modo:
    Dueño Grupo World
    rwx   r-x   r-x
    1 1 1 1 0 1 1 0 1

    Modo octal:
    Octal Binario Permisos
    0 000 ---
    1 001 --x

    2 010 -w-
    3 011 -wx

    4 100 r--
    5 101 r-x

    6 110 rw-
    7 111 rwx

    *Modo simbólico:*
    Simbolo Significado
    u Solo para el usuario
    g Solo para el grupo
    o Solo para otros (es el world)
    a Aplica para todos

    *chmod 755 mitexto* Cambia los permisos del archivo a 755.
    *chmod u-r mitexto* Quita el permiso de lectura al archivo.
    *chmod u=rwx,go=r mitexto* Agrega permiso de lectura, escritura y ejecución al usuario y solo de lectura al grupo y otros.
    *id* Muestra el ID del usuario.
    *whoami* Muestra el nombre del usuario logueado su username Cambia de usuario.
    *sudo comando* Ejecuta un comando como superusuario.

## VARIABLES DE ENTORNO.

    *env* Imprime las variables de entorno actuales.
    *echo $VAR* Imprime la variable de entorno VAR.
    *$PATH* Variable donde están las rutas de los ejecutables.
    *$HOME* Directorio home del usuario.
    *export $VAR=val* Asigna la variable $VAR con el valor val.

## COMANDOS DE BÚSQUEDAS.

    *find <ruta> -name <nombre>* Busca en una ruta y con un nombre de archivo.
    *find . -name* agenda Busca el archivo con el nombre agenda en el directorio actual.
    *grep <regex> file* Busca con expresiones regulares dentro de un archivo o salida de terminal.
    *grep -i hola mensaje.txt* Busca la palabra hola ignorando minúsculas y mayúsculas.

## UTILIDADES DE RED.

    *ifconfig* Muestra información de red.
    *ping ip_domain* Consulta la disponibilidad del recurso.
    *curl ip_domain* Consulta un recurso ya sea por dirección IP o por dominio y lo y lo muestra en terminal.
    *wget ip_domain* Descarga un recurso ya sea por dirección IP o por dominio.
    *traceroute ip_domain* Muestra la ruta del paquete a una IP o dominio.
    *netstat -i* Muestra las interfaces de red y su estado.

## COMPRIMIR ARCHIVOS.

    tar -czvf <nombre>.tar.gz <nombre_directorio>

    Ejemplo:
    tar -czvf mis_archivos.tar.gz Documentos

## DESCOMPRIMIR ARCHIVOS.

    tar -xzvf <nombre>.tar.gz <nombre_directorio>

    Ejemplo:
    tar -xzvf mis_archivos.tar.gz Documentos

