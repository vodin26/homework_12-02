## Домашнее задание к занятию «Репликация и масштабирование. Часть 1» "Воронин Владислав"


### Задание 1

**Master-Slave:**

Это самая простая модель репликации, где один сервер ( **master**) управляет данными, а другой сервер ( **slave**) дублирует эти данные. Master отвечает за изменения, а Slave просто копирует информацию.  

* **Плюсы:**
    * Простота и легкость внедрения
    * Высокая доступность, поскольку в случае сбоя мастера можно переключиться на Slave.
* **Минусы:**
    * Мастер всегда главный, Slave не имеет возможности влиять на базу данных самостоятельно.
    * Мастер загружен обновлением информации для всех Slaves, что может стать проблемой при большом количестве Slaves.

**Master-Master:**

Эта модель использует два сервера ( **мастера**) для синхронизации данных между собой. 

* **Плюсы:**
    *   Обеспечивает высокую отказоустойчивость и производительность, поскольку данные распределены. 
    *   Обеспечивает  более гибкий контроль над данными, так как оба мастера могут управлять ими независимо. 
* **Минусы:**
    *  Более сложный в настройке и обслуживании.

**Итог:**

* Master-Slave - простой и надежный способ репликации для небольших баз данных. 

* Master-Master - более сложный, но мощный подход для больших баз данных с повышенными требованиями к отказоустойчивости и производительности.

### Задание 2

C Master на Slave идет репликация:

![Скриншот-1](https://github.com/vodin26/homework_12-06/blob/main/img/Master_1.png)

Кофиги Master:

![Скриншот-1.2](https://github.com/vodin26/homework_12-06/blob/main/img/Conf_Master_1.png)

![Скриншот-1.2](https://github.com/vodin26/homework_12-06/blob/main/img/Conf_Master_2.png)

Со Slave ничего не копируется в Master, хотя если не отключен режим записи на Slave можно записать какое-нибудь значение.

![Скриншот-2](https://github.com/vodin26/homework_12-06/blob/main/img/Slave_1.png)

Конфиги Slave:

![Скриншот-1.2](https://github.com/vodin26/homework_12-06/blob/main/img/Conf_Slave_1.png)

![Скриншот-1.2](https://github.com/vodin26/homework_12-06/blob/main/img/Conf_slave_2.png)

### Задание 3

![Скриншот-1](https://github.com/vodin26/homework_12-06/blob/main/img/Master_1.2.png)

![Скриншот-1](https://github.com/vodin26/homework_12-06/blob/main/img/Master_2.2.png)