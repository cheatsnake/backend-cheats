# Шпаргалка по SQL

<div align="right"><a href="https://github.com/cheatsnake/backend-cheats#%D1%80%D0%B5%D0%BB%D1%8F%D1%86%D0%B8%D0%BE%D0%BD%D0%BD%D0%B0%D1%8F-%D0%B1%D0%B0%D0%B7%D0%B0-%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D1%85">Вернуться на главную страницу ⬆️</a></div>

 - Создание новой БД
	```sql
	CREATE DATABASE db_name;
	```
- Создание новой таблицы
	```sql
	CREATE TABLE users ( 
	    id SERIAL PRIMARY KEY, # Уникальный id
	    firstName VARCHAR(100), # Строка
	    lastName VARCHAR(100), # Строка
	    age INT, # Число
	    gender VARCHAR(10), # Строка 
	    isMarried BOOLEAN # true/false
	);        
	```
- Основные типы данных
    > - INT (целые числа от -2^32 до +2^32)
    > - FLOAT / DOUBLE / DECIMAL (дробные числа)
    > - CHAR / VARCHAR / TEXT (строки)
    > - DATA / DATETIME / TIME (дата и время)
    > - ENUM (перечисления - списки допустимых значений)
    > - [И другие](https://sql-language.ru/osnova-sql/tipy-dannykh-sql.html)
- Добавление данных в таблицу
	```sql
	INSERT INTO users(
	    firstName, lastName, age, gender, isMarried
	) VALUES (
	    'Alex', 'Manson' 25, 'male', false
	);
	```
- Выборка данных из таблицы
	```sql
	# SELECT
	## Получить всю таблицу users
	SELECT * FROM users; 
	## Получить только столбцы firstName и age из таблицы users
	SELECT firstName, age FROM users; 

	# LIMIT
	## Получить первых 20 записей таблицы users
	SELECT * FROM users LIMIT 20;

	# DISTINCT
	## Получить только уникальные значения из столбца firstName
	SELECT DISTINCT(firstName) FROM users;

	# WHERE
	## Записи, где столбец gender = 'male'
	SELECT * FROM users WHERE gender = 'male'; 
	## AND, OR 
	SELECT * FROM users WHERE age = 25 AND isMarried = falsel
	SELECT * FROM users WHERE age = 20 OR age = 50;

	# BETWEEN
	## Записи, где значения столбца age находятся в промежутке от 20 до 30
	SELECT * FROM users WHERE age BETWEEN 20 AND 30;

	#NULL
	## Записи, где столбец lastName не пуст
	SELECT * FROM users WHERE lastName IS NOT NULL;
	```
- Поиск данных по шаблону
	```sql
	# IN, LIKE, NOT LIKE
	## % - подстановочный знак, который указывает на любое кол-во символов
	## _ - подстановочный знак, который указывает на один символ

	## Записи, где firstname равен 'John', 'Mike' или 'Kane'
	SELECT * FROM users WHERE firstName IN ('John', 'Mike', 'Kane');
	## Записи, где firstname начинается c буквы 'A'
	SELECT * FROM users WHERE firstName LIKE 'A%';
	## Записи, где первая буква в firstName равна 'A', 'B' или 'C'
	SELECT * FROM users WHERE firstName LIKE '[ABC]%';
	## Записи, где вторая буква в firstname не равна 'o'
	SELECT * FROM users WHERE firstName NOT LIKE '_o%';
	```
- Сортировка и фильтрация данных таблиц
	```sql
	# ORDER BY
	## ASC - по возрастанию (по умолчанию)
	## DESC - по убыванию
	SELECT * FROM users ORDER BY firstName ASC;
	SELECT * FROM users ORDER BY age DESC;
	SELECT * FROM users ORDER BY lastName DESC, isMarried ASC;

	# HAVING
	## Фильтрация результатов группировки
	```
- Использование псевдонимов
	```sql
	# AS
	SELECT firstName AS name FROM users WHERE name = "Alex";
	```
- Изменение таблиц
	```sql
	# ALTER TABLE
	## Добавить новую колонку city к таблицe users
	ALTER TABLE users ADD COLUMN city VARCHAR(50); 
	## Удалить колонку isMarried из таблицы users
	ALTER TABLE users DROP COLUMN isMarried;
	## Переименовать колонку firstName в fName в таблицe users
	ALTER TABLE users RENAME COLUMN firstName TO fName;
	## Переименовать таблицу users в consumers
	ALTER TABLE users RENAME TO consumers;
	```
- Изменение данных в таблице
	```sql
	# UPDATE
	## Изменить в таблицe users записать с id = 1
	UPDATE users SET firstName = 'Kale', age = 33 WHERE id = 1;
	## Изменить записи, где gender = 'female'
	UPDATE users SET city = 'Paris' WHERE gender = 'famale';
	```
- Удаление данных из таблицы
	```sql
	# DELETE
	# Удалить запись в таблице users, где id = 2
	DELETE FROM users WHERE id = 2;
	# Удалить все записи в таблице users, где gender = 'male'
	DELETE FROM users WHERE gender = 'male';
	```
-   [Агрегатные функции](https://codetown.ru/sql/agregatnye-funkcii/)
	> Используются для обобщения/подсчёта данных.
	```sql
	# COUNT
	## Возвращает количество элементов в таблице users
	SELECT COUNT(*) FROM users;
	## Возвращает количество не повторяющихся значений столбца firstName
	SELECT COUNT(DISTINCT(firstName)) FROM users;

	# MAX, MIN
	SELECT MAX(age) FROM users;
	SELECT MIN(age) FROM users;

	# SUM
	# Сумма всех значений столбца age
	SELECT SUM(age) FROM users;

	# AVG
	## Среднее значение столбца age
	SELECT AVG(age) FROM users;
	```