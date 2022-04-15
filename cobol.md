##CURSO DE COBOL.

##ORÍGENES.
    - Grace Hooper y el departamento de Defensa.
    - Mainframe de **IBM**.

##ESTRUCTURA DE UN PROGRAMA EN COBOL.
    Se mantuvo la longitud de 80 columnas desde las tarjetas perforadas:

    - Columna 1 a 6 Se refiere a la posición al número de linea en el que te encuentras
    - Columna número 7 “*” los asteriscos son comentarios.
    - Area A (columna 8 a 11) divisiones y niveles jerarquicos, nombres de parrafos, etc…
    - Area B (Columna 12 a 72) se definen a los subniveles, sentencias, estructuras de control, etc…
    - Columnas 72 a la 80 (Originalmense usaban para poner comentarios referentes al programa)

##LAS DIVISIONES DE COMPONENTES.
    - Idenfication division: Incluye varios datos:
    Nombre de programa, instalación, fechas, etc…
    Es obligatorio el “program ID” y Sección de división.

    - Enviroment division:
    Contiene todos los ficheros de entrada y salida.

    - Data division:
    Contiene datos relacionados con los archivos de entrada y salida (longitudes, tamaños, variables, etc…)

    - Procedure division:
    Se declaran todas las sentencias en parrafos, siempre debe finalizar con un punto cada bloque de código.

