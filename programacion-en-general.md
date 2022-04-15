
# APUNTES DE PROGRAMACIÓN A NIVEL GENERAL.

## PROGRAMACIÓN ORIENTADA A OBJETOS.


### PRINCIPIOS DE LA POO.

    *Herencia* Compartir métodos y/o clases.
    *Abstracción* Aislar, separar.
    *Poliformismo* Mismo elemento, pero diferente comportamiento.
    *Modularidad* Separar en módulos.
    *Encapsulamiento* Se garantiza la integridad del código al ser separado.

### LAS CLASES.

    Los objetos se transforman en clases, las cuales pueden ser publicas, privadas y protegidas.
    En el caso de JAVA también existen las clases abstractas de las cuales se pueden extender otras (herencia).

    La solución estandar a los problemas de escalabilidad son los patrones de diseño.

### INTERFACE.

    Mientras la clase define el como se va a hacer, la interface define que se va a hacer y es la que establece 
    el contrato con la primera.

### EL CODESMELL.

    Es la sensación cuando un código que estamos leyendo no nos convence en un todo que esté bien estructurado, ya 
    que puede poseer errores de diseño.

### VARIABLES.

    $this -Variable reservada por el lenguaje que podemos usar para acceder a elementos propios.
    new -Palabra clave para un nuevo objeto.


### PROTOCOLOS Y PETICIONES AL SERVIDOR.

    *GET* Solicitar al servidor.
    *POST* Enviar al servidor.
    *HEAD* Encabezado.
    *PUT* Reemplazar información.
    *DELETE* Borrar información.

### CÓDIGO DE PETICIONES.

    *1XX* El servidor ha recibido la solicitud.
    *2xx* Solicitud Exitosa.
    *3xx* Acciones adicionales (redirecciones).
    *4xx* Errores en el cliente.
    *5xx* Errores en el servidor.

### CÓDIGOS MÁS USADOS.

    *200* Todo ok.
    *201* Solicitud Post Ok.
    *204* Ok, pero no devuelve información.
    *400* Algo está mal en la solicitud.
    *401* Error de Autenticación.
    *403* Parecido al 404.
    *404* No se encuentra la información.
    *500* Error interno del server.

### QUÉ ES UN CRUD.

    *C* Create, crear.
    *R* Read, leer.
    *U* Update, Actualizar.
    *D* Delete, borrar.


## INGENIERIA DE SOFTWARE.


### CÓDIGO BINARIO.

    Un bit son 8 bytes.
    1 byte --> Código binario.

    |--|--|--|--|-|-|-|-|   ----> IBM EN 1.956.
    128 64 32 16 8 4 2 1

    Ejemplos:
    *55* 110111
    *48* 110000

### IMPULSOS ELÉCTRICOS.

    *GPU* ---- > *CPU* ---> *ROM*
    La comunicación entre la GPU y la CPU se conoce como PCI express.

    Sistemas de Anillos:
    Kernel ) Drivers ) Apps.
    + o - permisos.


### APUNTES DE JENKINS.

    *jobs* Crear new job, existe el freestyle y el pipeline.
    *build* Ejecución de un Job.

