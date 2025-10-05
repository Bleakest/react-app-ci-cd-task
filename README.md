# React CI/CD Application

React приложение с автоматическим CI/CD пайплайном, развернутое на удаленном сервере с HTTPS.

## 🚀 О проекте

Это учебный проект, демонстрирующий полный цикл разработки и деплоя современного frontend-приложения:

- **Frontend**: React приложение, собранное с Vite
- **Infrastructure**: Docker контейнеризация, Nginx для раздачи статики
- **Reverse Proxy**: Traefik для автоматического HTTPS и маршрутизации
- **CI/CD**: Автоматический пайплайн сборки и деплоя на GitHub Actions
- **Deployment**: Удаленный сервер с автоматическим развертыванием по git push

🌐 Демо

Приложение доступно по адресу:

https://dmitry-kolesnikov.result-student.tw1.ru

## 🛠 Технологический стек

### Frontend

- **React** - современный frontend-фреймворк
- **Vite** - быстрый сборщик проектов

### DevOps & Infrastructure

- **Docker** - контейнеризация приложения
- **Docker Compose** - оркестрация контейнеров
- **Nginx** - веб-сервер для раздачи статики
- **Traefik** - reverse proxy с автоматическим SSL
- **GitHub Actions** - CI/CD пайплайн
- **Let's Encrypt** - автоматические SSL сертификаты

### Deployment

- **Ubuntu Server** - продакшен среда
- **SSH** - безопасное подключение к серверу
- **GitHub Secrets** - безопасное хранение чувствительных данных

## 🚀 Быстрый старт

### Локальная разработка

```bash
# Клонируй репозиторий
git clone https://github.com/Bleakest/react-app-ci-cd-task
cd react-app-ci-cd

# Установи зависимости
npm install

# Запусти в режиме разработки
npm run dev

# Собери для продакшена
npm run build

# Предпросмотр продакшен сборки
npm run preview
```

📦 Продакшен деплой

Деплой происходит автоматически при пуше в ветку master через GitHub Actions.

```bash
# Подключение к серверу
ssh username@server-ip

# Запуск приложения
cd /root/react-app
docker-compose up -d

# Проверка статуса
docker-compose ps

```

# 🔧 CI/CD Пайплайн

Проект использует автоматический пайплайн на GitHub Actions:

Этапы пайплайна:

- Build - сборка Docker образа

- Deploy - деплой на продакшен сервер

Секреты в GitHub:

- SSH_PRIVATE_KEY - приватный ключ для доступа к серверу

- SERVER_IP - IP адрес сервера

- SERVER_USER - пользователь для подключения
