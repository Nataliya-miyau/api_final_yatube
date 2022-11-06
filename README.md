Учебный проект курса Python-разработчик (бекенд) от Яндекс.Практикума.
API для Yatube
(спринт 9)
Описание
API для Yatub  - это проект социальной сети, в которой авторизованный пользователь может публиковать и комментировать записи, а так же подписываться/отписываться на других авторов. Неавторизованному пользователю контент доступен только в режиме чтения.

Технологии
Python 3.7, Django, DRF, JWT + Djoser

Установка:
Клонируйте репозиторий и перейдите в него в командной строке:
git clone <ссылка на репозиторий>
cd api_final_yatube
Установите и активируйте виртуальное окружение c учетом версии Python 3.7:
python3.7 -m venv venv
source venv/bin/activate
python3.7 -m pip install --upgrade pip
Установите все зависимости из файла requirements.txt:
pip install -r requirements.txt
Выполните миграции:
python3.7 manage.py migrate
Далее создадим суперпользователя:
python manage.py createsuperuser
Запустите проект:
python3.7 manage.py runserver

Примеры работы с API:

- создание публикации

POST /api/v1/posts/
в body { "text": "string", "image": "string", "group": 0 }

- обновление публикации

PUT /api/v1/posts/{id}/
в body { "text": "string", "image": "string", "group": 0 }

PATCH /api/v1/posts/{id}/
в body { "text": "string", "image": "string", "group": 0 }

- удаление публикации

DEL /api/v1/posts/{id}/

- подписка пользователя, от имени которого сделан запрос
  на пользователя, переданного в теле запроса

GET /api/v1/follow/ 
