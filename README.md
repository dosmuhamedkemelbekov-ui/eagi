# EAGI Telegram Mini App (MVP)

Мини-приложение для Telegram: бот открывает WebApp, WebApp отправляет данные на сервер и обратно в Telegram.

## 1) Установка

```bash
npm install
```

## 2) Настройка

1. Скопируй `.env.example` в `.env`
2. Заполни:
   - `BOT_TOKEN` — токен бота из BotFather
   - `WEB_APP_URL` — публичный HTTPS URL мини-приложения
   - `PORT` — порт локального сервера (по умолчанию 3000)

## 3) Запуск

```bash
npm run dev
```

## 4) Как подключить к Telegram

1. Создай бота через [@BotFather](https://t.me/BotFather)
2. Подними публичный HTTPS URL (например, через Cloudflare Tunnel или ngrok):
   - `https://your-domain.com` -> `http://localhost:3000`
3. Укажи этот URL в `.env` как `WEB_APP_URL`
4. Перезапусти сервер
5. Открой чат с ботом и отправь `/start`

## Что есть в MVP

- Бот с кнопкой открытия mini app
- Страница mini app с Telegram WebApp SDK
- Кнопка изменения "баллов"
- Отправка данных на backend `/api/submit`
- Отправка данных в Telegram через `WebApp.sendData`

## Важно для продакшена

- Проверять `initData` подпись Telegram на бэкенде
- Добавить БД (пользователь, баллы, активности)
- Добавить авторизацию, роли и админ-панель
