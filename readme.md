# Взламываем электронный дневник

Проект создан в учебный целях.

Скрипт содержит ряд функций для работы с базой данных электронного дневника.

## 1. Подключение
Файл `script.py` должен быть размещен в том же месте что и файл `manage.py`.

## 2. Описание функций

`script.get_child(child_name)` - В качестве аргумента принимает строку с именем ученика, возвращает объект с учетной записью ученика, если найдена одна запись.

`script.fix_marks(schoolkid)` - В качестве аргумента принимает учетную запись ученика, находит все оценки 2 и 3 и исправляет на 4 и 5 рандомно.

`script.remove_chastisements(schoolkid)` - В качестве аргумента принимает учетную запись ученика, удаляет все замечания указанного ученика.

`script.create_commendation(schoolkid, subject)` - В качестве аргументов принимает учетную запись ученика и строку с наименованием предмета. Для указанного ученика и предмета создает похвалу.

## 3. Пример использования:
```
$ python manage.py shell
>>> from datacenter import script
>>> kid = script.get_child('Гордеев Олимпий') 
>>> kid.full_name
'Гордеев Олимпий Харитонович'
>>> script.fix_marks(kid)
>>> script.remove_chastisements(kid) 
>>> script.create_commendation(kid, 'Математика')
```
## Цели проекта:

Код написан в учебных целях — это урок в курсе по Python и веб-разработке на сайте [Devman](https://dvmn.org).