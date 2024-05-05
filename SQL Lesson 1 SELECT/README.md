# Lección SQL 1: consultas SELECT 101
Para recuperar datos de una base de datos SQL, necesitamos escribir SELECTdeclaraciones, a las que a menudo se hace referencia coloquialmente como consultas . Una consulta en sí misma es solo una declaración que declara qué datos estamos buscando, dónde encontrarlos en la base de datos y, opcionalmente, cómo transformarlos antes de que se devuelvan. Sin embargo, tiene una sintaxis específica, que es la que aprenderemos en los siguientes ejercicios.
Como mencionamos en la introducción, puede pensar en una tabla en SQL como un tipo de entidad (es decir, perros), y cada fila de esa tabla como una instancia específica de ese tipo (es decir, un pug, un beagle, un pug de diferentes colores, etc.). Esto significa que las columnas representarían las propiedades comunes compartidas por todas las instancias de esa entidad (es decir, color del pelaje, longitud de la cola, etc.).

Y dada una tabla de datos, la consulta más básica que podríamos escribir sería una que seleccione un par de columnas (propiedades) de la tabla con todas las filas (instancias).

# Seleccionar consulta para columnas específicas
```sql
SELECT column, another_column, …
FROM mytable;
```
El resultado de esta consulta será un conjunto bidimensional de filas y columnas, efectivamente una copia de la tabla, pero solo con las columnas que solicitamos.

Si queremos recuperar absolutamente todas las columnas de datos de una tabla, podemos usar la *taquigrafía asterisco () en lugar de enumerar todos los nombres de las columnas individualmente.

# Seleccionar consulta para todas las columnas
```sql
SELECT * 
FROM mytable;
```
Esta consulta, en particular, es realmente útil porque es una forma sencilla de inspeccionar una tabla volcando todos los datos a la vez.

# RESULTADOS EJERCICIOS
```sql
--1-Find the title of each film ✓
	SELECT title  FROM movies;
--2-Find the director of each film ✓
	SELECT director  FROM movies;
--3-Find the title and director of each film ✓
	SELECT title,director FROM movies;
--4-Find the title and year of each film ✓
	SELECT title,year  FROM movies;
--5-Find all the information about each film
	SELECT title,year  FROM movies;	
```
