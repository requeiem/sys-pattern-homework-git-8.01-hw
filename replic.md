# Домашнее задание к занятию «`Репликация и масштабирование. Часть 1 - Чесноков Александр`»

---

### Задание 1

На лекции рассматривались режимы репликации master-slave, master-master, опишите их различия.

### Ответ:

В режиме репликации master-slave, данные можно внести только через мастер ноду, которые реплицируются в slave ноду, и с slave ноды можно только читать данные.
В случае же с режимом репликации master-master, то данные можно вносить в каждой ноде master, тем самым репликация данных происходит в обе стороны.
При вводе данных на master-master репликации, нагрузка распределяется, тем самым улучшая скорость записи. 

---

### Задание 2

Выполните конфигурацию master-slave репликации, примером можно пользоваться из лекции.

![alt text](https://github.com/requeiem/sys-pattern-homework-git-8.03-hw/blob/main/img/REPLIC.jpg)
![alt text](https://github.com/requeiem/sys-pattern-homework-git-8.03-hw/blob/main/img/REPLIC1.jpg)

---

### Задание 3 

Выполните конфигурацию master-master репликации. Произведите проверку.

![alt text](https://github.com/requeiem/sys-pattern-homework-git-8.03-hw/blob/main/img/REPLICA2.jpg)
![alt text](https://github.com/requeiem/sys-pattern-homework-git-8.03-hw/blob/main/img/REPLICA3.jpg)
