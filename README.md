# Чат модуль для 1С

Получить скрипт с чатом можно по следующему url: https://raw.githubusercontent.com/Talalaev/1c_chat/main/dist/chat.js

Запуск скрипта в 1с: 
- вставив ссылку в атрибут src тега script
`<script src="https://raw.githubusercontent.com/Talalaev/1c_chat/main/dist/chat.js"></script>`
- загрузить скрип get запросом и вставить полученный контент внутри тегов 
script
`<script>content loaded from url</script>`

Для того чтобы чат запустился в html должен присутствовать тег `<div id="app"></div>`, 
до вызова скрипта чата.

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>1C Chat</title>
</head>
<body>
  <div id="app"></div>
  <script src="https://raw.githubusercontent.com/Talalaev/1c_chat/main/dist/chat.js"></script>
</body>
</html>
```

При успешном запуске должен появиться текст Chat. В html вместо `<div id="app"></div>`
должен появиться тег `<div class="1c-chat">Chat</div>`
Вызов кода чата происходит сразу после исполнения скрипта. Если скрипт не 
запустился то вызвать запуск приложения можно повторно.

```
// вызов запуска скрипта чата вручную из js
window.chat.run('#app', {});
```
