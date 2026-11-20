Небольшой веб-сервис на Python
## чо внутри
 `app.py` — само Flask-приложение с двумя маршрутами (`/` и `/health`).
`requirements.txt` — (`Flask`, `gunicorn`).
`Dockerfile` — сборка образа на базе `python:3.11-slim`, запуск через Gunicorn от непривилегированного пользователя `appuser`
`.dockerignore` — исключение виртуального окружения `.venv` и кэша при сборке образа.

## Маршруты API
- `GET /` — возвращает информацию о приложении, версию и имя студента в формате JSON.
- `GET /health` — проверка работоспособности сервиса (`{"status": "ok"}`).

## Как запустить локально через Docker

1
```bash
docker build -t cloud-container-app:
2 
запуск контейнера с портом 10000
docker run --rm -p 10000:10000 --name cloud-demo cloud-container-app:1.0

-ссылка на рендер = https://containerapp-8z3d.onrender.com/
