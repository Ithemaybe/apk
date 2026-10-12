# Чат для друзей

## 1. Сервер (Termux или ПК)
Нужно: Node.js 22+ и cloudflared.
    cd server
    ./start.sh          # Termux: запускает сервер и туннель
Либо вручную:  HTTPS=1 node server.js   и в другом окне   cloudflared tunnel --url http://localhost:5000
В выводе cloudflared найдите ссылку https://xxxx.trycloudflare.com — это адрес чата.
Админ: John / test (СМЕНИТЕ пароль в профиле).

## 2. APK
Залейте всю эту папку в репозиторий GitHub → вкладка Actions → "Build APK" → Run workflow →
после сборки (3–6 мин) скачайте артефакт chat-apk (внутри app-debug.apk).
При первом запуске приложения вставьте ссылку из пункта 1.
