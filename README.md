# Домашнее задание к занятию "Базы данных" "Воронин Владислав"

### Задание 1

1 Сотрудники: 
 
 id (первичный ключ, serial)
 Фамилия (VARCHAR(50) )
 Имя (VARCHAR(50) )
 Отчество (VARCHAR(50) )
 id Тип подразделения (внешний ключ, INTEGER)
 id Структурное подразделения (внешний ключ, INTEGER)
 id Должность (внешний ключ, INTEGER)
 id Проект (внешний ключ, INTEGER)
 id Адрес филиала (внешний ключ, INTEGER)
 Дата найма (DATA)
 Оклад (FLOAT)

2 Должность: 
id (первичный ключ, serial)
Должность (VARCHAR(40) )

3 Тип подразделения:
id (первичный ключ, serial)
Тип подразделения (VARCHAR(12) )
  
4 Структурное подразделение:
id (первичный ключ, serial)
Структурное подразделение (VARCHAR(60) )

5 Область:
id (Первичный ключ serial)  
Область, Край (VARCHAR(50) )

6 Город 
id (первичный ключ, serial)
Город, посёлок (VARCHAR(30))


