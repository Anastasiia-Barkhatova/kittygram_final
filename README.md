[![Main Kittygram workflow](https://github.com/Anastasiia-Barkhatova/kittygram_final/actions/workflows/main.yml/badge.svg)](https://github.com/Anastasiia-Barkhatova/kittygram_final/actions/workflows/main.yml)

### **Описание проекта Kittygram**

> Kittygram - это сервис для публикации данных о котиках.Пользователи могут пользователи хотят самостоятельно регистрироваться в сервисе, загружать фотографии с описанием котиков и смотреть питомцев других пользователей.

### **Cтек технологий:**
- Python 3.9
- Django 3.2.3
- Django Rest Framework 3.12.4
- PostgreSQL 13
- Node.js
- React

### **Как запустить backend проекта:**

Клонировать проект:

```bash
git clone https://github.com/Anastasiia-Barkhatova/kittygram_final
```

Создайть файл .env и заполнить его данными:
- POSTGRES_DB=kittygram
- POSTGRES_USER=kittygram_user
- POSTGRES_PASSWORD=kittygram_password
- DB_NAME=kittygram
- DB_HOST=db
- DB_PORT=5432

Перейти в репозиторий backend:

```bash
cd backend
```

Cоздать и активировать виртуальное окружение:

```bash
python -m venv env
```

* Если у вас Linux/macOS

    ```bash
    source env/bin/activate
    ```

* Если у вас windows

    ```bash
    source env/scripts/activate
    ```

```bash
python3 -m pip install --upgrade pip
```

Установить зависимости из файла requirements.txt:

```bash
pip install -r requirements.txt
```

Выполнить миграции:

```bash
python manage.py migrate
```

Запустить проект:

```bash
python manage.py runserver
```

### **Как запустить frontend проекта:**

Перейти в репозиторий frontend :

```bash
cd frontend
```

Установить зависимости:

```bash
npm i
```

Запустить проект:

```bash
npm run start
```

#  Как работать с репозиторием финального задания

## Что нужно сделать

Настроить запуск проекта Kittygram в контейнерах и CI/CD с помощью GitHub Actions

## Как проверить работу с помощью автотестов

В корне репозитория создайте файл tests.yml со следующим содержимым:
```yaml
repo_owner: ваш_логин_на_гитхабе
kittygram_domain: полная ссылка (https://доменное_имя) на ваш проект Kittygram
taski_domain: полная ссылка (https://доменное_имя) на ваш проект Taski
dockerhub_username: ваш_логин_на_докерхабе
```

Скопируйте содержимое файла `.github/workflows/main.yml` в файл `kittygram_workflow.yml` в корневой директории проекта.

Для локального запуска тестов создайте виртуальное окружение, установите в него зависимости из backend/requirements.txt и запустите в корневой директории проекта `pytest`.

## Чек-лист для проверки перед отправкой задания

- Проект Taski доступен по доменному имени, указанному в `tests.yml`.
- Проект Kittygram доступен по доменному имени, указанному в `tests.yml`.
- Пуш в ветку main запускает тестирование и деплой Kittygram, а после успешного деплоя вам приходит сообщение в телеграм.
- В корне проекта есть файл `kittygram_workflow.yml`.

Авторы: [команда Яндекс.Практикума](https://github.com/yandex-praktikum), [Бархатова Анастасия](https://github.com/Anastasiia-Barkhatova)