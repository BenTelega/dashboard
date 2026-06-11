# Dashboard

Страница с надписью **SOON**, развёрнутая в Docker.

## Стек

- **frontend** — nginx:alpine с кастомным `index.html`
- **nginx** — reverse proxy (nginx:alpine) на порту 5001
- **Caddy** — на хосте, слушает `dash.benetelega.ru` и проксирует на `localhost:5001`

## Файлы

| Файл | Описание |
|---|---|
| `index.html` | страница `SOON` |
| `Dockerfile` | сборка образа frontend |
| `nginx.conf` | конфиг reverse proxy → frontend:80 |
| `docker-compose.yml` | сервисы frontend + nginx |

## Запуск

```bash
cd ~/dashboard && docker compose up -d
```

Страница откроется на `http://localhost:5001`.

## Остановка

```bash
cd ~/dashboard && docker compose down
```
