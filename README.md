<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>21 очко - Игра</title>
    <script src="https://telegram.org/js/telegram-web-app.js"></script>
</head>
<body>
    <button id="btn">Send Data</button>
    <script>
        const tg = window.Telegram.WebApp;
        tg.MainButton.text = "Отправить данные";
        tg.MainButton.show();
        tg.MainButton.onClick(() => {
            window.Telegram.WebApp.postEvent("web_app_data_send", { data: JSON.stringify({ test: 123 }) });
        });
    </script>
</body>
</html>
