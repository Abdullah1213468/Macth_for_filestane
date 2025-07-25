<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Hamster Mini App</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <!-- Telegram WebApp JS -->
  <script src="https://telegram.org/js/telegram-web-app.js"></script>

  <!-- CSS Styling -->
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #222;
      color: #fff;
      margin: 0;
      padding: 0;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }

    .container {
      text-align: center;
    }

    button {
      margin-top: 20px;
      padding: 10px 20px;
      font-size: 18px;
      background-color: #30a7ff;
      border: none;
      color: white;
      border-radius: 8px;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>🐹 Hamster Mini App</h1>
    <p>Welcome, <span id="username">...</span>!</p>
    <button onclick="startGame()">🚀 Start Game</button>
  </div>

  <!-- JS Logic -->
  <script>
    window.Telegram.WebApp.ready();
    const user = Telegram.WebApp.initDataUnsafe?.user;
    document.getElementById("username").innerText = user?.first_name || "Guest";

    function startGame() {
      Telegram.WebApp.showAlert("Game starting soon... 🚀");
    }
  </script>
</body>
</html>
