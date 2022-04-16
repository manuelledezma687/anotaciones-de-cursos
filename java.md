
# CURSO DE JAVA SE.

## GETTER Y SETTERS.

    - Los getters son un tipo de función que nos devuelve el valor asignado por una variable.
    - Los setters son un tipo de función que nos establece el tipo de valor de una variable.

## LAS VARIABLES EN JAVA.

    -las variables en java deben tener nombre unicos
    -las variables string son en "".
    -las variables pueden ser int , string
    -las variables pueden ser alteradas o actualizadas.

    Una convención de nombres es un patrón que deben seguir los nombres de las variables 
    para que el código esté organizado, entendible y sin repetidos.
    Java es sensible a mayúsculas y minúsculas, este punto es clave al seguir una convención.
    Las variables siempre deben comenzar con un simbolo de letra, $ o _.


    No puedes usar el simbolo - en ninguna parte de la variable.

    Las variables constantes son variables cuyo valor nunca va a cambiar, por lo que se deben 
    escribir completamente en mayúsculas y usando el caracter _.

    char: Ocupa 2 bytes y solo puede almacenar 1 dígito, debemos usar comillas simples en vez de comillas dobles.
    boolean: Son un tipo de dato lógico, solo aceptan los valores true y false. También ocupa 2 bytes y almacena 
    únicamente 1 dígito.

    Pero esto cambia a partir de Java 10: solo debemos escribir la palabra reservada var y Java definirá el tipo 
    de dato de nuestras variables automáticamente.

## TIPOS DE DATOS PARA NÚMEROS ENTEROS.

    byte: Ocupa 1 byte de memoria y su rango es de -128 hasta 127.
    short: Ocupa 2 bytes de memoria y su rango es de -32,768 hasta 32,727.

    int: Ocupa 4 bytes de memoria y su rango es de -2,147,483,648 hasta 2,147,483,647. 
    Es muy cómodo de usar, ya que no es tan pequeño para que no quepan nuestros números 
    ni tan grande como para desperdiciar mucha memoria. 
    Puede almacenar hasta 10 dígitos.

    long: Ocupa 8 bytes de memoria y su rango es de -9,223,372,036,854,775,808 hasta 
    9,223,372,036,854,775,807. Para diferenciarlo de un tipo 
    de dato long debemos terminar el número con la letra L.
    Por ejemplo:

    // Int:
    int n = 1234567890;

    // Long:
    long nL = 123456789012345L;
    Tipos de datos para números flotantes (con decimales):

    float: Ocupan 4 bytes de memoria y su rango es de 1.40129846432481707e-45 
    hasta 3.40282346638528860e+38. Así como long, debemos colocar una letra F al final.
    double: Ocupan 8 bytes de memoria y su rango es de 4.94065645841246544e-324d hasta 1.79769313486231570e+308d.
    Por ejemplo:

    // Double:
    double nD = 123.456123456;

    // Float
    float nF = 123.456F;


## OPERADORES DE ASIGNACIÓN.

    +=: a += b es equivalente a a = a + b.
    -=: a -= b es equivalente a a = a - b.
    *=: a *= b es equivalente a a = a * b.
    /=: a /= b es equivalente a a = a / b.
    %=: a %= b es equivalente a a = a % b.
    Operadores de incremento:

    ++: i++ es equivalente a i = i + 1.
    --: i-- es equivalente a i = i - 1.
    
    Podemos usar estos operadores de forma prefija (++i) o postfija 
    (i++). La diferencia está en qué operación se ejecuta primero:


    Math.PI // 3.141592653589793
    Math.E // 2.718281828459045

    Math.ceil(2.1) // 3.0 (redondear hacia arriba)
    Math.floar(2.1) // 2.0 (redondear hacia abajo)

    Math.pow(2, 3) // 8.0 (número elevado a una potencia)
    Math.sqrt(3) // 1.73... (raíz cuadrada)

    Math.max(2, 3) // 3.0 (el número más grande)

    // Área de un círculo (PI * r^2):
    Math.PI * Math.pow(r, 2)

    // Área de una esfera (4 * PI * r^2):
    4 * Math.PI * Math.pow(r, 2)

    // Volumen de una esfera ( (4/3) * PI * r^3):
    (4/3) * Math.PI * Math.pow(r, 3)


## CASTEO DE DATOS.

    En la programación hay situaciones donde necesitamos cambiar el 
    tipo de dato de nuestras variables, esto lo conocemos como Cast.

    CONVERSIONES ENTRE TIPOS

    NO PERDEMOS INFORMACIÓN
    De char —> int.
    De byte —> short —> int —> long
    De int —> double
    De float —> double
    PERDEMOS INFORMACIÓN
    De int —> float
    De long —> float
    De long —> double

## ARCHIVOS JAR.

    Los archivos JAR (Java Archive) son archivos de Java con el código compilado de los 
    archivos .class y comprimido con el formato ZIP para que más adelante sean interpretados 
    y ejecutados por la máquina virtual de Java (JVM).

## VARIABLES SEGÚN SU ALCANCE.

    Las variables globales: Se definen antes de entrar a una funcion o proceso y que como su nombre indica pueden ser 
    llamadas a procesos en cualquier lugar ya que fueron previamente declaradas. (USO PUBLICO PODRIA DECIRSE)
    Las variables locales: Son las que se definen para un proceso en especifico en un funcion especifica y solo van 
    a ser reconocidas para esa funcion o proceso, es decir que si intentamos hacer la llamada a una variable local en otra 
    funcion que no sea la de origen no la reconocera como declarada.(USO PRIVATIZADO).

## FUNCIONES EN JAVA.

    Funciones: nos ayudan a organizar, modularizar y evitar el código repetido.
    • Return: palabra clave cuando una función tiene un valor de regreso.
    • Void: palabra clave cuando una función no tiene un valor de regreso.
    Nota: si nuestras funciones van a devolver argumentos, lo mejor es que especifiques el tipo de dato que serán. 
    Para utilizar nuestras funciones solo debemos asignar el resultado de la función y sus parámetros a una 
    variable con el mismo tipo de dato de la función.

## PRINCIPIOS SOLID.

    - Responsabilidad única: Cada clase debe tener una única responsabilidad.
    - Open Close: Clases y funciones deberian ser pensadas para ser extendidas desde afuera pero no modificables desde adentro.
    - Principios de sustitución de Liskov: Sustituir una clase derivada de una clase principal, sin que esta última se rompa.  
    Los objetos deberían ser reemplazables por instancias de sus subtipos. 
    - Segregación de interfaces: No tener una interfaz con todas las responsabilidades, sino varias interfaces limpias y simples.
    - Inversión de dependencias: Separar las interfaces entre componentes high level de los low levels, una mezcla de Open close con segregación de interfaces.


