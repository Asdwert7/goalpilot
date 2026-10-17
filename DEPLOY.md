# Развёртывание

## Требования
- Docker и Docker Compose v2
- (для разработки без Docker) .NET SDK 10

## Шаги
1. Создайте файл окружения и заполните значения (`.env` не коммитится):
   ```bash
   cp .env.example .env
   ```
2. Запустите сервисы:
   ```bash
   docker compose up --build
   ```
3. Проверьте:
   - `curl localhost:8080/health` → `{"status":"ok"}`
   - Swagger UI: http://localhost:8080/swagger (в окружении Development)
