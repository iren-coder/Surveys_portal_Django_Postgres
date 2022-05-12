Меню сайта содержит:
- Главная страница с приветственным словом https://95.163.213.100/
- Регистрация нового пользователя https://95.163.213.100/signup/
- Вход в учётную запись https://95.163.213.100/login/
- Выход из учётной записи https://95.163.213.100/logout/
- Страница со всеми опросами https://95.163.213.100/polls-list/all/ 
- Все доступные опросы https://95.163.213.100/polls-list/available/
- Все пройденные опросы https://95.163.213.100/polls-list/checked/
- Все недоступные на данный момент опросы https://95.163.213.100//polls-list/not-available/
- Страница со статистикой https://95.163.213.100//statistics/
- Панель администратора https://95.163.213.100//admin/

Как развернуть приложение локально:

1. Создайте виртуальное окружение в папке, куда планируете скачать проект: python -m venv
(например, python -m venv C:\Users\project)

2. Активируйте виртуальное окружение командой cd C:\Users\project\Scripts\activate.bat

3. Скачайте проект по ссылке https://github.com/iren-coder/Surveys_portal_Django_Postgres либо склонируйте репозиторий git@github.com:iren-coder/Surveys_portal_Django_Postgres.git.

4. Установите Postgres и создайте базу данных Postgres, создайте юзера с именем и паролем и дайте ему все привилегии над базой. Затем впишите свои название БД, имя юзера и пароль в раздел DATABASES в файле my_project/settings.py
- установка PostgreSQL: sudo apt install postgresql postgresql-contrib
- войти в консоль postgres: sudo -u postgres psql
- создать базу данных и пользователя:
        - CREATE DATABASE db_name;
        - CREATE USER user_name WITH PASSWORD 'password';
- дать все разрешения пользователю для работы с базой данных: GRANT ALL PRIVILEGES ON DATABASE db_name TO user_name;

5. Создайте и примините миграции:
python manage.py makemigrations
python manage.py migrate

6. Скопируйте статические файлы python manage.py collectstatic

7. Теперь можно запустить сервер python manage.py runserver

