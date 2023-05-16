# Домашнее задание к занятию  "`Работа с данными (DDL/DML)`" - `Чесноков Александр`

---
### Задание 1
1.1. Поднимите чистый инстанс MySQL версии 8.0+. Можно использовать локальный сервер или контейнер Docker.

1.2. Создайте учётную запись sys_temp. 

1.3. Выполните запрос на получение списка пользователей в базе данных. (скриншот)

![alt text](https://github.com/requeiem/sys-pattern-homework-git-8.03-hw/blob/main/img/my-sql1.jpg)

1.4. Дайте все права для пользователя sys_temp. 

1.5. Выполните запрос на получение списка прав для пользователя sys_temp. (скриншот)

![alt text](https://github.com/requeiem/sys-pattern-homework-git-8.03-hw/blob/main/img/my-sql2.jpg)

1.6. Переподключитесь к базе данных от имени sys_temp.

Для смены типа аутентификации с sha2 используйте запрос: 
```sql
ALTER USER 'sys_test'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
```

![alt text](https://github.com/requeiem/sys-pattern-homework-git-8.03-hw/blob/main/img/my-sql3.jpg)

1.6. По ссылке https://downloads.mysql.com/docs/sakila-db.zip скачайте дамп базы данных.

1.7. Восстановите дамп в базу данных.

![alt text](https://github.com/requeiem/sys-pattern-homework-git-8.03-hw/blob/main/img/my-sql4.jpg)

1.8. При работе в IDE сформируйте ER-диаграмму получившейся базы данных. При работе в командной строке используйте команду для получения всех таблиц базы данных. (скриншот)

*Результатом работы должны быть скриншоты обозначенных заданий, а также простыня со всеми запросами.*

![alt text](https://github.com/requeiem/sys-pattern-homework-git-8.03-hw/blob/main/img/my-sql5.jpg)
![alt text](https://github.com/requeiem/sys-pattern-homework-git-8.03-hw/blob/main/img/my-sql6.jpg)

### Задание 2
Составьте таблицу, используя любой текстовый редактор или Excel, в которой должно быть два столбца: в первом должны быть названия таблиц восстановленной базы, во втором названия первичных ключей этих таблиц. Пример: (скриншот/текст)
```
Название таблицы | Название первичного ключа
customer         | customer_id
```

[Excel файл по 2 заданию](https://github.com/requeiem/sys-pattern-homework-git-8.03-hw/blob/main/img/%D0%97%D0%B0%D0%B4%D0%B0%D0%BD%D0%B8%D0%B52.xlsx)
