\c ITM_task013_TaskHibernate_Task_2_db;                         -- Переключает активную базу данных на ITM_task013_TaskHibernate_Task_2_db;

### DROP
>
> ```sql 
> DROP TABLE IF EXISTS users;
> ```
> 
> ```sql 
> DROP DATABASE IF EXISTS db_name;                  -- Удалить базу `db_name` если она существует;
> ```
> ``                -- Удалить базу `db_name` если она существует;
> 

### CREATE
> `CREATE DATABASE db_name;`                          -- Создаю базу `db_name`;
> 
> `CREATE DATABASE IF EXISTS db_name;`                -- Создаю базу `db_name` если она не существовала до этого;
> 
> GRANT ALL PRIVILEGES ON DATABASE db_name TO user1;  -- Даём пользователю `user1` права на базу данных `db_name`
> 
> ```sql
> CREATE TABLE IF NOT EXISTS users (
>       user_id BIGSERIAL PRIMARY KEY,           -- Поле id с автоинкрементом (эквивалент LONG в Java);
>       user_name VARCHAR(50) NOT NULL,          -- Поле name с максимальной длиной 50 символов;
>       user_lastName VARCHAR(70) NOT NULL,      -- Поле lastName с максимальной длиной 70 символов;> 
>       user_age SMALLINT NOT NULL               -- Поле age, хранящее возраст как целое число;
> );
> ```

> ```sql 
> 
> ```




CREATE TABLE IF NOT EXISTS users (
user_id BIGSERIAL PRIMARY KEY,           -- Поле id с автоинкрементом (эквивалент LONG в Java);
user_name VARCHAR(50) NOT NULL,          -- Поле name с максимальной длиной 50 символов;
user_lastName VARCHAR(70) NOT NULL,      -- Поле lastName с максимальной длиной 70 символов;
user_age SMALLINT NOT NULL               -- Поле age, хранящее возраст как целое число;
);
SELECT * FROM users;

DROP TABLE IF EXISTS users;
DROP DATABASE IF EXISTS ITM_task013_TaskHibernate_Task_2_db;    -- Удаляю базу если она существует;



-- ***** ***** *****    а теперь по прошлой задаче:     ***** ***** *****
\c ITM_task012_TaskJDBC_Task_1_db;                         -- Переключает активную базу данных на ITM_task012_TaskJDBC_Task_1_db;

DROP TABLE IF EXISTS users;
DROP DATABASE IF EXISTS ITM_task012_TaskJDBC_Task_1_db;     -- Удаляю базу если она существует

CREATE DATABASE ITM_task012_TaskJDBC_Task_1_db;             -- Создаю базу если она еще не существует
CREATE TABLE users (
user_id BIGSERIAL PRIMARY KEY,       -- Поле id с автоинкрементом (эквивалент LONG в Java)
user_name VARCHAR(50) NOT NULL,      -- Поле name с максимальной длиной 50 символов
user_lastName VARCHAR(70) NOT NULL,  -- Поле lastName с максимальной длиной 70 символов
user_age SMALLINT NOT NULL           -- Поле age, хранящее возраст как целое число
);
SELECT * FROM users;

DROP DATABASE IF EXISTS ITM_task012_TaskJDBC_Task_1_db;     -- Удаляю базу если она существует;

