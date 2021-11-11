# Чат модуль для 1С

Получить скрипт с чатом можно по следующему url: https://raw.githubusercontent.com/Talalaev/1c_chat/main/dist/chat.ts

Запуск скрипта в 1с: 
- загрузить скрип get запросом и вставить полученный контент внутри тегов 
script
`<script>content loaded from url</script>`

Пример Html шаблона для 1C в который нужно вставить загруженный скрипт.

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>1C Chat</title>
</head>
<body>
  <div id="app"></div>
  <script>content loaded from url</script>
</body>
</html>
```

## Chat API

Приложение чата доступно в глобальной переменной `chat` (`window.chat`).

### Старт чата

`window.chat.run()`

### Отправка сообщений в чат

`window.chat.sendMessage("сообщение в чат")`
