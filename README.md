# job-tracker

Трекер откликов на вакансии: компании, отклики, история смены статусов, REST API.

Стек: Python 3.14, Django 6.1, DRF, PostgreSQL, Docker Compose.

## Запуск

```bash
cp .env.example .env          # затем поменяй DJANGO_SECRET_KEY и пароли в .env
docker compose up --build     # сервисы web (Django) и db (PostgreSQL)
docker compose run --rm web python manage.py migrate
curl http://localhost:8000/health/
```

Остановка: `docker compose down` (данные базы остаются в томе `pgdata`; `down -v` удалит и их).

Статус: учебный проект, в разработке.
