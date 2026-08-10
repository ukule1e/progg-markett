<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>Маркет PROGG</title>
    <script src="https://telegram.org/js/telegram-web-app.js"></script>
</head>
<body style="background:#000;color:#fff;font-family:sans-serif;padding:10px;">
    <h1 style="color:#0f0;text-align:center;">🛒 МАРКЕТ PROGG</h1>
    <p style="text-align:center;" id="user">Загрузка...</p>
    <h3 style="color:#0f0;">🍺 Меню Бара</h3>
    <button onclick="buy('chips','🥔 Чипсы',120)" style="width:100%;padding:10px;margin:5px;background:#0f0;color:#000;border:none;">🥔 Чипсы - 120б.</button>
    <button onclick="buy('chocolate','🍫 Шоколад',80)" style="width:100%;padding:10px;margin:5px;background:#0f0;color:#000;border:none;">🍫 Шоколад - 80б.</button>
    <button onclick="buy('water','💧 Вода',50)" style="width:100%;padding:10px;margin:5px;background:#0f0;color:#000;border:none;">💧 Вода - 50б.</button>
    <h3 style="color:#0f0;">❄️ Холодильник</h3>
    <button onclick="buy('energy','⚡️ Энергетик',180)" style="width:100%;padding:10px;margin:5px;background:#0f0;color:#000;border:none;">⚡️ Энергетик - 180б.</button>
    <button onclick="buy('cold_tea','🧋 Чай',110)" style="width:100%;padding:10px;margin:5px;background:#0f0;color:#000;border:none;">🧋 Чай - 110б.</button>
    <button onclick="buy('soda','🥤 Газировка',100)" style="width:100%;padding:10px;margin:5px;background:#0f0;color:#000;border:none;">🥤 Газировка - 100б.</button>
    <script>
        var tg = window.Telegram.WebApp;
        tg.expand();
        document.getElementById('user').innerText = '👤 Готов к покупкам!';
        function buy(id, name, price) {
            tg.sendData(JSON.stringify({item_id:id, item_name:name, item_price:price}));
            tg.close();
        }
    </script>
</body>
</html>
