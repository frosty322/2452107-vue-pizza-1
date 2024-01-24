# HTML Academy. Личный проект «Pizza»

## Наставник Олег Глущенко 

## Начальные требования
- Docker
- NodeJS >= 16

## Docker установка
https://docs.docker.com/get-docker/

## Node js установка
Мы рекоммендуем использовать Node Version Manager для удобного управления версиями node.js

https://github.com/nvm-sh/nvm

Либо можно установить node.js отдельно

https://nodejs.org/en/download/

## Работа с помощью GNU Make
Для удобной работой с проектом мы используем GNU Make.

https://www.gnu.org/software/make/

По-умолчанию, GNU Make уже предустановлен на Unix операционных системах.
Чтобы проверить установлени ли GNU Make на вашем компьютере выполните команду в терминале

```
make --version 
```

В случае отстутствия GNU Make, мы рекоммендуем установить его.

В makefile доступны следующие команды

Установить зависимости для проекта

`$ make install_dependencies`

Запустить проект

`$ make start_project`

## Работа без GNU Make

### Frontend установка

- Перейдите в директорию (выполнить из корня приложения)

`cd frontend`

- Установите зависимости

`$ npm ci`

В директории `frontend` возможно выполнить следующие скрипты:

```
npm run dev - запуск проекта (только клиент) в режиме разработки
npm run build - создание продакшн сборки проекта
npm run test:unit - запуск юнит тестов
npm run lint - запуск линтера
```

### Backend установка

- Перейдите в директорию (выполнить из корня приложения)

`cd backend`

- Установите зависимости

`$ npm ci`

- Запуск сервера (для запуска необходима работающая база данных на порте :5432)

`$ npm start`

### Установка шаблона

- Перейдите в директорию (выполнить из корня приложения)

`cd template`

- Установите зависимости

`$ npm ci`

- Запуск шаблонов

`$ npm start`

### Docker настройка

- Сборка проекта

`$ docker compose build`

### Запуск проекта с Docker

`$ docker compose down -v`

`$ docker compose up`

Сервер будет доступен по адресу `localhost:3000`

Клиент будет доступен по адресу `localhost:8080`

### Запуск проекта без Docker

| Внимание: требуется ручной запуск базы данных |
|-----------------------------------------------|

- Запуск базы данных

Запустите PostgreSQL базу данных

Обновите конфигурацию подключения базы данных для сервера в файле `backend/src/datasources/database.datasource.ts`

- Запуск сервера (выполнить из корня приложения)

```
cd backend && npm start
```

- Запуск клиента (выполнить из корня приложения)

```
cd frontend && npm run dev
```

Сервер будет доспупен по адресу `localhost:3000`

Клиент будет доспупен по адресу `localhost:8080`


## Вход для авторизированного пользователя

Мы создали готового пользователя и разместили его в нашей базе данных. Для входа (логина) в систему используйте следующие данные:

```
email: user@example.com
password: user@example.com
```

Вы можете поменять данные пользователя в файле `backend/src/factory/users.json`

## Документация эндпоинтов сервера (OpenAPI)

Запустите проект и перейдите по адресу:

```
http://localhost:3000/explorer/
```

## Запуск и просмотр готовой верстки проекта

### С помощью GNU Make

`$ make install_template_dependencies`

`$ make run_template`

### Без GNU Make

Перейдите в директорию template:

```
cd template 
```

Установите зависимости, выполнив команду:

```
npm ci
```

Запустите проект командой:

```
npm start
```

Шаблон и вёрстка будут доступны по адресу: `http://localhost:9999`.

Вёрстку можно посмотреть в директории `template/src`.
