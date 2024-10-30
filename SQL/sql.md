\c db_name;                         -- Переключает активную базу данных на ITM_task013_TaskHibernate_Task_2_db;

# NТипичный запросы для операций над БД

> ### PostgreSQL
> ```postgresql
> DROP TABLE IF EXISTS users;                           -- Удаляю таблицу users если она существует;
> DROP DATABASE IF EXISTS db_name;                      -- Удаляю базу db_name если она существует;
> 
> CREATE DATABASE IF NOT EXISTS db_name;                -- Создаю базу db_name если она не существовала до этого;
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


> ### MySQL
> ```mysql 
> USE db_name;       -- Переключает активную базу данных на db_name;
> 
> ```


> ```sql 
> 
> ```
