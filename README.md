1. Создайте виртуальное окружение в папке с проектом: python -m venv
(например, python -m venv C:\Users\project)

2. Активируйте виртуальное окружение командой cd C:\Users\project\Scripts\activate.bat

3. Скачайте проект.

4. Создайте базу данных Postgres, создайте юзера с именем и паролем и дайте ему все привилегии над базой. Затем впишите название БД, имя юзера и пароль в раздел DATABASES в файле my_project/settings.py

5. Создайте и примините миграции:
python manage.py makemigrations
python manage.py migrate

6. Теперь можно запустить сервер python manage.py runserver

superuser:
iraed
123
