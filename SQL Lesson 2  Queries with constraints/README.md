# Lección SQL 2: Consultas con restricciones (Parte 1)
Ahora sabemos cómo seleccionar columnas de datos específicas de una tabla, pero si tuviera una tabla con cien millones de filas de datos, leer todas las filas sería ineficiente y quizás incluso imposible.

Para evitar que se devuelvan ciertos resultados, necesitamos usar una WHEREcláusula en la consulta. La cláusula se aplica a cada fila de datos verificando valores de columna específicos para determinar si deben incluirse en los resultados o no.
```sql
SELECT column, another_column, …
FROM mytable
WHERE condition
    AND/OR another_condition
    AND/OR …;
```
Se pueden construir cláusulas más complejas uniendo numerosas ANDpalabras ORclave lógicas (es decir, num_wheels >= 4 AND puertas <= 2). Y a continuación se muestran algunos operadores útiles que puede utilizar para datos numéricos (es decir, enteros o de punto flotante):

| Operador            | Condición                                       | Ejemplo de SQL                  |
|---------------------|-------------------------------------------------|--------------------------------|
| =, !=, <, <=, >, >= | Operadores numéricos estándar                   | nombre_columna != 4            |
| EN MEDIO Y ...      | El número está dentro del rango de dos valores (inclusive) | col_name ENTRE 1.5 Y 10.5  |
| NO ENTRE ... Y ...  | El número no está dentro del rango de dos valores (inclusive) | col_name NO ENTRE 1 Y 10 |
| EN (...)            | El número existe en una lista                   | nombre_columna EN (2, 4, 6)    |
| NO EN (...)         | El número no existe en una lista                | col_name NO EN (1, 3, 5)       |

Además de hacer que los resultados sean más fáciles de entender, escribir cláusulas para restringir el conjunto de filas devueltas también permite que la consulta se ejecute más rápido debido a la reducción de datos innecesarios que se devuelven.


# ¿Sabías?
Como ya habrás notado, SQL no requiere que escribas las palabras clave en mayúsculas, pero como convención, ayuda a las personas a distinguir las palabras clave SQL de los nombres de columnas y tablas, y hace que la consulta sea más fácil de leer.

# Ejercicio
Usando las restricciones correctas, encuentre la información que necesitamos en la tabla Películas para cada tarea a continuación.

# Encuentra la película con una fila id de 6.
```sql
SELECT *
FROM Movies
WHERE Id = 6;
```
# Encuentra las películas estrenadas en la década de 2000 y 2010.
```sql
SELECT *
FROM Movies
WHERE Year BETWEEN 2000 AND 2019;
```
# Encuentra las películas no estrenadas en la década de 2000 y 2010.
```sql
SELECT *
FROM Movies
WHERE Year < 2000 OR Year > 2019;
```
# Encuentra las primeras 5 películas de Pixar y su año de estreno.
```sql
SELECT Title, Year
FROM Movies
WHERE Title LIKE '%Pixar%'
ORDER BY Year
LIMIT 5;
```