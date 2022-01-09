# Apuntes

## ¿Qué es una Base de Datos?

En un nivel muy básico, usamos las bases de datos para almacenar información. Tomamos un montón de datos de alguna fuente, la cual sera persistida dentro de la base de datos ya sea en memoria (RAM) o en disco. Eventualmente recuperaremos esos datos en algún momento en el futuro.

Para trabajar con una base de datos como Postgre, debemos conectarnos con un "cliente", un cliente puede ser cualquier pieza de software, puede ser una API, una aplicación de escritorio, una aplicación móvil, una aplicación web, etc. Para conectar el cliente con la base de datos, escribimos SQL. SQL es similar a un lenguaje de programación, con la diferencia de que SQL es usado para interactuar con bases de datos.

Para ilustrar un poco mejor que es SQL, podemos usar los siguientes ejemplos:

Para añadir datos:

```sql
INSERT INTO
    cities(name, lat, lng, country, iso3, population)
VALUES
    ('san Francisco', 37.7, 122.4, 'United States', 'USA', 883305);
```

Leer datos:

```sql
SELECT name FROM cities;
```

Actualizar datos:

```sql
UPDATE
    cities
SET
    population = 19354921
WHERE
    name = 'New York';
```

Eliminar datos:

```sql
DELETE FROM
    cities
WHERE
    id = 300;
```

Cuando hablamos de SQL, estamos hablando de algo independiente de Postgres, SQL es un lenguaje de comunicación, es el estándar y es usado por muchos otras bases de datos como Oracle, MySQL, MS SQL Server, PostgreSQL, etc.

Cuando aprendemos SQL podemos usar ese conocimiento para aplicarlo en cualquier base de datos, no siempre es lo mismo, pero en general se sigue el estándar.

## Retos de Trabajar con Postgres

- Escribir consultas eficientes para recuperar datos.
- Diseñar el esquema o estructura de la base de datos.
- Entender cuando usar las características avanzadas de Postgres.
- Saber como gestionar la base de datos en un entorno de producción.

