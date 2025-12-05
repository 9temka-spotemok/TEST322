# AI Competitor Insight Hub (shot-news)

**Версия:** 0.1.0  
**Статус:** В разработке  

Интеллектуальная платформа для мониторинга новостей из мира ИИ-индустрии с персонализированными дайджестами.

## 🚀 Быстрый старт

### Предварительные требования
- Python 3.11+
- Node.js 20 LTS
- Docker & Docker Compose
- Git

### Установка

1. **Клонируйте репозиторий:**
```bash
git clone <repository-url>
cd shot-news
```

2. **Запустите инфраструктуру:**
```bash
docker-compose up -d postgres redis
```

3. **Настройте backend:**
```bash
cd backend
poetry install
cp env.example .env
poetry run alembic upgrade head
poetry run uvicorn main:app --reload --host 0.0.0.0 --port 8000
```

4. **Настройте frontend:**
```bash
cd frontend
npm install
cp env.example .env.local
npm run dev
```

5. **Проверьте работу:**
- Backend API: http://localhost:8000/docs
- Frontend: http://localhost:5173

## 📋 Структура проекта

```
shot-news/
├── backend/          # FastAPI backend
│   ├── app/         # Основной код приложения
│   ├── alembic/     # Миграции базы данных
│   └── main.py      # Точка входа
├── frontend/        # React frontend
│   ├── src/         # Исходный код
│   └── public/      # Статические файлы
└── docker-compose.yml
```

## 🛠️ Технологический стек

### Backend
- FastAPI
- SQLAlchemy (async)
- PostgreSQL
- Redis
- Celery
- Alembic

### Frontend
- React 18
- TypeScript
- Tailwind CSS
- TanStack Query
- React Router

## 📚 Документация

- [SETUP.md](SETUP.md) - Подробная инструкция по настройке
- [QUICK_START.md](QUICK_START.md) - Быстрый старт
- [DEVELOPMENT.md](DEVELOPMENT.md) - Руководство по разработке

## 🧪 Тестирование

### Backend
```bash
cd backend
poetry run pytest
```

### Frontend
```bash
cd frontend
npm test
```

## 📝 Лицензия

MIT