
# APUNTES DEL CURSO DE BASE DE DATOS.

## LENGUAJE DDL.

    - Create: Nos ayuda a crear bases de datos, tablas, vistas, índices, etc.
    - Alter: Ayuda a alterar o modificar entidades.
    - Drop: Nos ayuda a borrar. Hay que tener cuidado al utilizarlo.

    - 3 objetos que manipularemos con el lenguaje DDL:
        • Database o bases de datos
        • Table o tablas. Son la traducción a SQL de las entidades.
        • View o vistas: Se ofrece la proyección de los datos de la base de datos de forma entendible.

## LENGUAJE DML (MANIPULAR DATOS).

    - SELECT (FROM). Seleccionar campos.
    - WHERE. Buscar campo "donde" coincida el valor tal.
    - LIMIT (OFFSET). Establecer límite en la query.
    - GROUP BY. Agrupar campos en una tabla. Ejemplo: SELECT Categoria, SUM(Stock) FROM productos GROUP BY Categoria.
    - INNER JOIN. Unir tablas.
    - ORDER BY. Ordenar ASC o DSC.
    - HAVING. Ccnsulta teniendo tal valor incluido.
    - UPDATE. Actualizar.
    - INSERT INTO. Insertar en una tabla.

## INSERT INTO EJEMPLOS.

'
    INSERT INTO productos (xx, xx) values
    (“xx”,”xx”);
    INSERT INTO productos
    SET
    XX = “XX”,
    XX = “XX2;


'

## UPDATE EJEMPLO.

    - UPDATE Tabla SET Campo1 = Valor1 WHERE Campo = 'Valor';

## RENAME TABLE TO EJEMPLO. 

    - RENAME TABLE articulos TO productos;

## ALIAS EJEMPLOS.

    - AS */-+El As como tupla o como resultado final

## BETWEEN EJEMPLO.

    - WHERE precio BETWEEN 200 AND 2000

## BOOLEANOS AND Y OR IN EN EJEMPLOS.

    - Where marca IN (“XX”,”XX”);

## LIKE EJEMPLO.

    - Nombre like F% / EJEMPLO FACUNDO %A% (JUAN)

## DELETE.

    - La sentencia DELETE se puede utilizar para eliminar todos los registros de una tabla 
    pero tiene la desventaja de no ser tan eficiente ya que por ejemplo (entre otras limitaciones), 
    no resetea los valores de los campos auto_increment, por este motivo si se opta por vaciar completamente 
    la tabla es recomendable utilizar la sentencia.

## TRUNCATE TABLE.

    - la cual elimina los registros en su totalidad dejando vacía la tabla y de manera menos costosa 
    (en términos de rendimiento) para el servidor de base de datos.
    TRUNCATE TABLE Productos;

## COUNT EJEMPLO.
    
    - SELECT COUNT(*) FROM Productos WHERE Nombre LIKE "%iPhone%";

## HAVING EJEMPLO.

    - SELECT Categoria, SUM(Stock) FROM Productos GROUP BY Categoria HAVING
    SUM(Stock) > 250;

## ALTER TABLE EJEMPLOS.

    - ADD. ALTER TABLE articulos ADD COLUMN Observaciones VARCHAR(50) NULL;
    - CHANGE. ALTER TABLE articulos CHANGE observaciones observaciones VARCHAR(40) NULL;
    - DROP. ALTER TABLE articulos DROP COLUMN observaciones;
    - RENAME. ALTER TABLE Articulos RENAME Productos;

## FUNCIONES EN LA BASE DE DATOS.

    - SUM() Retorna la suma de los valores que contiene el campo especificado. 
    Por ejemplo, si se quiere saber el stock de
    productos que hay en la tabla Productos:
    SELECT SUM(Stock) FROM Productos;

    - MIN() Para averiguar el valor mínimo de un campo usamos la función Min(). 
    Por Ejemplo, se quiere saber cuál es el
    menor precio de todos los Artículos:
    SELECT MIN(Precio) FROM Productos;

    - MAX() Para averiguar el valor máximo de un campo usamos la función Max(). 
    Ejemplo, se quiere saber cuál es el mayor
    precio de todos los Productos:
    SELECT MAX(Precio) FROM Productos;

    - AVG() Retorna el valor promedio de los valores del campo especificado. 
    Por ejemplo, si se quiere saber el promedio
    del precio de los Productos.
    SELECT AVG(Precio) FROM Productos;

## GROUP_CONCAT Unir grupos.

    - Ejemplo de consultar a más de 1 tabla:
    - SELECT * FROM Productos, Marcas WHERE Productos.Marca = Marcas.idMarca;

## INNER JOIN: TIPOS Y EJEMPLOS.

    - [INNER] JOIN Este JOIN devuelve solamente los registros que coinciden:
    SELECT * FROM tabla1 JOIN tabla2 ON tabla1.codigo = tabla2.codigo;
    SELECT * FROM tabla1 INNER JOIN tabla2 ON tabla1.codigo = tabla2.codigo;

    - LEFT [OUTER] JOIN Este JOIN devuelve todos los registros de la tabla de
    la izquierda y los registros que coinciden de la tabla de la derecha:
    SELECT * FROM tabla1 LEFT JOIN tabla2 ON tabla1.codigo = tabla2.codigo;

    - RIGHT [OUTER] JOIN Este JOIN devuelve todos los registros de la tabla de
    la derecha y los registros que coinciden de la tabla de la izquierda:
    SELECT * FROM tabla1 RIGHT JOIN tabla2 ON tabla1.codigo = tabla2.codigo;

    - CROSS JOIN Combina cada registro de la tabla de la izquierda con cada registro 
    de la tabla de la derecha, sin hacer coincidir un campo en particular:
    SELECT * FROM tabla1 CROSS JOIN tabla2;

## UNION.

    - La sintaxis para combinar dos consultas mediante la cláusula UNION es la siguiente 
    (Los corchetes ([]) indican que el elemento es opcional):
    Ejemplo: consulta1 UNION [ALL] consulta2;

## MANERAS DE INGRESAR A MYSQL.

    - Workbech. la manera tradicional por el binario.
    - phpmyadmin. interfaz gráfica por el navegador.
    - windows+r. terminal de linea de comandos de Windows --> ejecutar cmd ---> 
    c:/xamp/mysql/bin/mysql ... --> show databases, etc.

