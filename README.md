# Домашнее задание к занятию 12.7 "Репликация и масштабирование. Часть 2"
Домашнее задание выполните в Google Docs и отправьте в личном кабинете на проверку ссылку на ваш документ.

Название файла должно содержать номер лекции и фамилию студента. Пример названия: "12.7 "Репликация и масштабирование. Часть 2 - Александр Александров"

Перед тем как выслать ссылку, убедитесь, что ее содержимое не является приватным (открыто на просмотр всем, у кого есть ссылка). Если необходимо прикрепить дополнительные ссылки, просто добавьте их в свой Google Docs.

Любые вопросы по решению задач задавайте в чате учебной группы.

---

### Задание 1.

Опишите основные преимущества использования масштабирования методами:

- активный master-сервер и пассивный репликационный slave-сервер, (повышение отказоустойчивости, часть запросов можно отправить на slave для снижения нагрузки) 
- master-сервер и несколько slave-серверов, ( повышение отказоустойчивости, к примеру мастер работает на запись остальные slave работают для отработки запросов select через балансировщик)
- активный сервер со специальным механизмом репликации – distributed replicated block device (DRBD), снижается производительность часть ресурсов идет на обслуживание механизма DRBD, если что то пойдет не так то получим две не работающии реплики в итоге NULL.
- SAN-кластер. пишем читаем с разных дисков узкое место ресурсы цп памяти сервера БД

*Дайте ответ в свободной форме.*

---

### Задание 2.


Разработайте план для выполнения горизонтального и вертикального шаринга базы данных. База данных состоит из трех таблиц: 

- пользователи, 
- книги, 
- магазины (столбцы произвольно). 

Опишите принципы построения системы и их разграничение или (и) разбивку между базами данных.

*Пришлите блок схему, где и что будет располагатся. Опишите, в каких режимах будут работать сервера.* 

![alt text](https://github.com/vasev85/sql_replication2/blob/main/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202022-10-31%20%D0%B2%2022.54.24.png?raw=true)

## Дополнительные задания (со звездочкой*)

Эти задания дополнительные (не обязательные к выполнению) и никак не повлияют на получение вами зачета по этому домашнему заданию. Вы можете их выполнить, если хотите глубже и/или шире разобраться в материале.



---
### Задание 3*.

Выполните настройку выбранных методов шардинга из задания 2.

*Пришлите конфиг docker и sql скрипт с командами для базы данных*
