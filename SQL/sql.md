\c db_name;                         -- Переключает активную базу данных на ITM_task013_TaskHibernate_Task_2_db;

# NТипичный запросы для операций над БД

> ### PostgreSQL
> ```postgresql
> \l                                                    -- или
> SELECT datname FROM pg_database;                      -- Показать все имеющиеся базы данных
> 
> \dn                                                   -- или
> SELECT schema_name FROM information_schema.schemata;  -- Показать все имеющиеся схемы
> 
> \c db_name                                            -- или
> \dt                                                   -- или
> SELECT table_name 
> FROM information_schema.tables 
> WHERE table_schema = 'public';                        -- Показать все таблицы в базе данных db_name
> 
> \d table_name;                                       -- Просмотр структуры таблицы table_name (В psql)
> 
> \dt;                                                  -- Показать все таблицы в текущей схеме (В psql)
> 
> \c db_name                                            -- переключиться на другую БД в PostgreSQL, используйте команду \c в psql
> -- в SQL-запросе (например, в коде), напрямую переключиться на другую БД в PostgreSQL нельзя. Вместо этого установите новое подключение к нужной БД.
> 
> ALTER TABLE table_name ADD COLUMN new_column_name data_type;  -- Добавление нового столбца в таблицу
> ALTER TABLE table_name DROP COLUMN column_name;               -- Удаление столбца column_name из таблицы // Изменение структуры таблицы (например, добавление или удаление столбца):
>
> 
> --  Основные операции с данными (CRUD)
> INSERT INTO table_name (column1, column2) VALUES (value1, value2);    -- Вставка  данных в таблицу
> SELECT * FROM table_name WHERE condition;                             -- Выборка данных
> UPDATE table_name SET column1 = value1 WHERE condition;               -- Обновление данных в таблице
> DELETE FROM table_name WHERE condition;                               -- Удаление данных из таблицы
>
> 
>  
> DROP TABLE IF EXISTS users;                           -- Удаляю таблицу users если она существует;
> DROP SCHEMA schema_name CASCADE;                      -- Удаляю схему schema_name вместе с содержимым;
> DROP DATABASE IF EXISTS db_name;                      -- Удаляю базу db_name если она существует;
> 
> CREATE DATABASE IF NOT EXISTS db_name;                -- Создаю базу db_name если она не существовала до этого;
> CREATE SCHEMA schema_name;                            -- Создаю схему schema_name;
> CREATE USER user1 WITH PASSWORD '1234';               -- Создаем пользователя user1 с паролем 1234
> GRANT ALL PRIVILEGES ON DATABASE db_name TO user1;    -- Даём пользователю `user1` права на базу данных `db_name`
> 
> CREATE TABLE IF NOT EXISTS users (
>       user_id BIGSERIAL PRIMARY KEY,                  -- Поле id с автоинкрементом (эквивалент LONG в Java);
>       user_name VARCHAR(50) NOT NULL,                 -- Поле name с максимальной длиной 50 символов;
>       user_lastName VARCHAR(70) NOT NULL,             -- Поле lastName с максимальной длиной 70 символов;> 
>       user_age SMALLINT NOT NULL                      -- Поле age, хранящее возраст как целое число;
> );
> 
> SELECT table_name FROM information_schema.tables WHERE table_schema = 'public';   -- Показать все таблицы из базы данных
> SELECT * FROM users;                                  -- Показывает ВСЁ содержимое таблицы users;
> 
> ```

\l
-- или
SELECT datname FROM pg_database;







> ### MySQL
> ```mysql 
> USE db_name;       -- Переключает активную базу данных на db_name;
> 
> ```


> ```sql 
> 
> ```
