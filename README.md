# PayPlaner Frontend

React мини-приложение для Telegram, позволяющее отслеживать и управлять платными подписками.

## Технологии

- **React 18+** с TypeScript
- **Redux Toolkit** - управление состоянием
- **React Router** - навигация
- **Ant Design** - UI компоненты
- **Tailwind CSS** - стилизация
- **Vite** - сборщик и dev-сервер

## Быстрый старт

1. Установите зависимости:
```bash
npm install
```

2. Создайте файл `.env` в корне проекта с переменными:
   - `VITE_API_URL` - URL бекенд API (по умолчанию `http://localhost:3000/api`)
   - `VITE_TELEGRAM_BOT_NAME` - имя Telegram бота (опционально)

3. Запустите проект для разработки:
```bash
npm run dev
```

## Структура проекта

```
.
├── src/
│   ├── assets/           # Статические ресурсы (иконки)
│   ├── components/       # Переиспользуемые компоненты
│   ├── pages/            # Страницы приложения
│   │   ├── Dashboard.tsx
│   │   ├── Login.tsx
│   │   ├── Settings.tsx
│   │   ├── SubscriptionForm.tsx
│   │   └── Subscriptions.tsx
│   └── store/            # Redux store
│       ├── api.ts        # RTK Query API
│       ├── hooks.ts      # Typed hooks
│       ├── slices/       # Redux slices
│       ├── thunks/    # Async thunks
│       └── store.ts
├── Dockerfile
├── index.html
├── vite.config.ts
└── package.json
```

## Переменные окружения

- **VITE_API_URL**: URL бекенд API (например, `http://localhost:3000/api`)
- **VITE_TELEGRAM_BOT_NAME**: Имя Telegram бота (опционально)

## Команды

- `npm run dev` - запуск dev-сервера (Vite)
- `npm run build` - сборка для продакшена
- `npm run preview` - предпросмотр собранного проекта
- `npm run lint` - проверка кода линтером
- `npm run lint:fix` - автоматическое исправление ошибок линтера

## Разработка

Проект использует Vite для быстрой разработки. После запуска `npm run dev` приложение будет доступно на `http://localhost:5173` (или другом порту, указанном Vite).

Для работы с Telegram Mini App требуется HTTPS. При локальной разработке используйте туннель (ngrok, Cloudflare Tunnel и т.д.).

## Страницы

- **Login** - авторизация через Telegram
- **Dashboard** - главная страница с общей статистикой
- **Subscriptions** - список всех подписок
- **SubscriptionForm** - форма создания/редактирования подписки
- **Settings** - настройки приложения

