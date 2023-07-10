# Домашнее задание к занятию «Базы данных» - Семикова Т.В. FOPS-9

### Легенда

Заказчик передал вам [файл в формате Excel](https://github.com/netology-code/sdb-homeworks/blob/main/resources/hw-12-1.xlsx), в котором сформирован отчёт. 

На основе этого отчёта нужно выполнить следующие задания.

### Задание 1

Опишите не менее семи таблиц, из которых состоит база данных:

- какие данные хранятся в этих таблицах;
- какой тип данных у столбцов в этих таблицах, если данные хранятся в PostgreSQL.

Приведите решение к следующему виду:

Сотрудники (

- идентификатор, первичный ключ, serial,
- фамилия varchar(50),
- ...
- идентификатор структурного подразделения, внешний ключ, integer).
_____________________________________________________________

### ТАБЛИЦЫ:


### 1.Сотрудники
- id_sotr, первичный ключ, serial, NOT NULL;
- Фамилия VARCHAR(M), NOT NULL;
- Имя VARCHAR(M), NOT NULL;
- Отчество VARCHAR(M), NOT NULL;
- Дата найма DATE, NOT NULL;
- id_okl;
- id_dolg;
- id_otd;
- id_proj;

### 2.Оклад
- id_okl, первичный ключ, serial, NOT NULL;
- сумма - money, NOT NULL;
  
### 3. Должность
- id_dolg, первичный ключ, serial, NOT NULL;
- название должности - VARCHAR(M), NOT NULL;
- id_otd;
  
### 4. Отдел
- id_otd, первичный ключ, serial NOT NULL;
- наименование отдела VARCHAR(M), NOT NULL;
- id_podr;
  
### 5. Подразделение
- id_podr, первичный ключ, serial, NOT NULL;
- структурное подразделения VARCHAR(M), NOT NULL;
- id_adr;

### 6. Адрес филиала
- id_adr, первичный ключ, serial, NOT NULL;
- улица, номер дома VARCHAR(M), NOT NULL;
- id_gorod;

### 7. Город филиала
- id_gorod, первичный ключ, serial, NOT NULL;
- город - VARCHAR(M), NOT NULL;
- id_reg;

### 8. Регион филиала
- id_reg, первичный ключ, serial, NOT NULL;
- регион - VARCHAR(M), NOT NULL;
  
### 9. Проект
- id_proj, первичный ключ, serial, NOT NULL;
- название проекта VARCHAR(M), NOT NULL;

### 10. Назначение на проект
- id_proj;
- id_sotr;
