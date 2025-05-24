
# EXAM

Напишите тренировочный код для задания. Код (ВЕСЬ) в одном файле: Выберите из таблицы orders 5 самых дорогих заказов за всё время. Данные нужно отсортировать в порядке убывания цены. Отмененные заказы не учитывайте.


CREATE TABLE orders (
 id INT PRIMARY KEY,
 user_id INT,
 products_count INT,
 sum INT,
 status VARCHAR(50)
);

INSERT INTO orders (id, user_id, products_count, sum, status) VALUES
(1, 1, 2, 1300, 'new'),
(2, 18, 1, 10000, 'cancelled'),
(3, 11, 1, 2140, 'in_progress'),
(4, 145, 5, 6800, 'new'),
(5, 23, 1, 999, 'new'),
(6, 1, 2, 7690, 'cancelled'),
(7, 17, 1, 1600, 'new'),
(8, 5, 4, 400, 'delivery'),
(9, 2355, 1, 1450, 'new'),
(10, 13, 7, 13000, 'cancelled');

![image](https://github.com/user-attachments/assets/40f08e34-3291-448a-98d2-7e740d6e6307)

SELECT *
FROM orders
WHERE status != 'cancelled'
ORDER BY SUM DESC
LIMIT 5;

![image](https://github.com/user-attachments/assets/6a78af84-4d50-4de0-8f86-8825bd305de2)


