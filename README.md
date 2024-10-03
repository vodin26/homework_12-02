## Домашнее задание к занятию «SQL. Часть 1» "Воронин Владислав"


### Задание 1

```mysql
SELECT DISTINCT district AS Уникальные_районы
FROM address
WHERE district REGEXP '^[kK].*a$' AND district NOT LIKE '% %';
```

### Задание 2

```mysql
SELECT 
    rental_id,
    customer_id,
    staff_id,
    payment_date AS Дата_оплаты,
    last_update AS Последнее_обновление,
    amount AS Стоимость
FROM payment
WHERE DATE(payment_date) BETWEEN '2005-06-15' AND '2005-06-18'
AND TIME(payment_date) BETWEEN '00:00:00' AND '23:59:59'
AND amount > 10.00;
```

### Задание 3

```mysql
SELECT *
FROM rental
ORDER BY rental_id DESC
LIMIT 5;
```

### Задание 4

```mysql
SELECT 
    LOWER(CONCAT(first_name, ' ', last_name)) AS имя,
    last_name,
    first_name,
    email,
    address_id
FROM customer
WHERE first_name IN ('Kelly', 'Willie')
AND active = 1;
```