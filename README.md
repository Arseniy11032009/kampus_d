<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Buy form</title>
</head>
<body>

<div id="buy">
    <button id="button_buy">Купить</button>
</div>


<form id="form" style="display: none">
    <input type="text" id="user_name">
    <input type="text" id="last_name">
    <button id="order">Отправить</button>
</form>

<script src="https://telegram.org/js/telegram-web-app.js"></script>

<script>
    let tg = window.Telegram.WebApp;
    let buy_button = document.getElementById("button_buy");
    let order_button = document.getElementById("order");
    tg.expand();

    buy_button.addEventListener("click", () => {
        document.getElementById("buy").style.display = "none";
        document.getElementById("form").style.display = "block";
    });

    order_button.addEventListener("click", () => {
        document.getElementById("order").style.display = "none";
        tg.close()
   });
    tg.close()
</script>

</body>
</html>
