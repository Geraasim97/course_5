# coursework_5_test
# Работа с базами данных 

Для подключение к базе данных требуется создать файл database.ini и внести параметры:

import psycopg2

conn = psycopg2.connect(
    host="localhost",
    database="database",
    user="ВАШ ЛОГИН",
    password="ВАШ ПАРОЛЬ"
)

Данный проект получает данные о работодателях и их вакансиях с сайта hh.ru.
Работодатели выбраны случайным образом. Вакансии представлены только теми, которые являются активными у выбранных работодателей

Данные, полученные от hh.ru, записываются в БД hh_info(PostgreSQL) в соответствующие таблицы employers и vacancies.
(Команды, которыми создавались БД и таблицы в pgAdmin, зафиксированы в файле queries.sql)

Для заполнения таблиц БД необходимо запустить файл filling_bd.py.

После того как БД будет заполнена данными, пользователь сможет получить следующую информацию (функция main()):
Список работодателей и количество их вакансий;
Список всех вакансий;
Средняя зарплата по всем вакансиям;
Список вакансий за зарплатой выше средней;
Найти вакансии по ключевому слову.

