# Introducción a SQL
Una serie de lecciones y ejercicios interactivos diseñados para ayudarle a aprender SQL.

# ¿Qué es SQL?
SQL, o lenguaje de consulta estructurado, es un lenguaje diseñado para permitir a usuarios técnicos y no técnicos consultar, manipular y transformar datos de una base de datos relacional. Y debido a su simplicidad, las bases de datos SQL brindan almacenamiento seguro y escalable para millones de sitios web y aplicaciones móviles.

# ¿Sabías?
Existen muchas bases de datos SQL populares, incluidas SQLite, MySQL, Postgres, Oracle y Microsoft SQL Server. Todos ellos admiten el estándar de lenguaje SQL común, que es lo que enseñará este sitio, pero cada implementación puede diferir en las características adicionales y los tipos de almacenamiento que admite.

# Base de dato a utilizar 
Usaremos una base de datos con datos sobre algunas de las películas clásicas de Pixar para la mayoría de nuestros ejercicios. Este primer ejercicio solo involucrará la tabla Películas y la consulta predeterminada a continuación muestra actualmente todas las propiedades de cada película. Para continuar con la siguiente lección, modifique la consulta para encontrar la información exacta que necesitamos para cada tarea.

```sql
create database MoviesPixar;
use MoviesPixar;

CREATE TABLE Movies (
    Id INT PRIMARY KEY,
    Title NVARCHAR(100),
    Director NVARCHAR(100),
    Year INT,
    Length_minutes INT
);

INSERT INTO Movies (Id, Title, Director, Year, Length_minutes) VALUES
(1, 'Toy Story', 'John Lasseter', 1995, 81),
(2, 'A Bug''s Life', 'John Lasseter', 1998, 95),
(3, 'Toy Story 2', 'John Lasseter', 1999, 93),
(4, 'Monsters, Inc.', 'Pete Docter', 2001, 92),
(5, 'Finding Nemo', 'Andrew Stanton', 2003, 107),
(6, 'The Incredibles', 'Brad Bird', 2004, 116),
(7, 'Cars', 'John Lasseter', 2006, 117),
(8, 'Ratatouille', 'Brad Bird', 2007, 115),
(9, 'WALL-E', 'Andrew Stanton', 2008, 104),
(10, 'Up', 'Pete Docter', 2009, 101),
(11, 'Toy Story 3', 'Lee Unkrich', 2010, 103),
(12, 'Cars 2', 'John Lasseter', 2011, 120),
(13, 'Brave', 'Brenda Chapman', 2012, 102),
(14, 'Monsters University', 'Dan Scanlon', 2013, 110);

```