## Examples

```
SELECT \*
FROM customers
WHERE NOT customerId > 3
ORDER BY CITY
LIMIT 5 --One of the few that goes after ORDER BY
```

```
-- Foreign Key Constraint == > Primary Key
SELECT \*
FROM [Orders] AS o
JOIN [Customers] AS c
ON o.customerId = c.customerId
LIMIT 3
```

## Notes

knexjs.org

Access to RDB from Node

- raw or native driver
- query builder ..KNEX
- Object Relational Mapper (ORM)

KNEX

- SQL Injection attack protection
- connection pooling
- supports promises, callbacks
- schema builder. use DDL statements like create table, drop table
- query builder with a clean js api
- standardization normalizes the DB dialects

INSTALL

- `yarn add knex`
- `yarn add sqlite3`

How to use it

- install knex globally on system once
- install knex
- install driver
- initialize knex (`knex init`)

## Project Specific Notes

Zoos Table should have the following columns:

- id: primary key, automincrements.
- name: unique, alphanumeric up to 255 characters long.
- created_at: should automatically default to the current date and time.

Bears Table should have the following columns:

- id: primary key, automincrements.
- zooId: an integer that relates this table to the zoos table. Enforce data integrity.
- species: unique, alphanumeric up to 80 characters long.
- latinName: alphanumeric up to 80 characters long.
- createdAt: should automatically default to the current date and time.
