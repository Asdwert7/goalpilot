# GoalPilot

Мобильный трекер целей и задач с ИИ-помощником, который декомпозирует цели на задачи. Учебный проект.

## Стек
- Backend: ASP.NET Core Web API (.NET 10 LTS), EF Core + Npgsql
- БД и кэш: PostgreSQL 18, Redis 7
- Инфраструктура: Docker Compose
- Mobile: Android, Kotlin + Jetpack Compose (заготовка, см. `mobile/README.md`)
- ИИ: Google Gemini API (`gemini-2.5-flash`), ключ только через переменные окружения

## Быстрый старт
```bash
cp .env.example .env   # заполните значения
docker compose up --build
curl localhost:8080/health
```
Подробнее — в [DEPLOY.md](DEPLOY.md).
