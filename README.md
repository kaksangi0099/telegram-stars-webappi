<!DOCTYPE html>
<html lang="fa">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>بازی اسکوئید گیم - ورود</title>
  <style>
    body {
      font-family: 'Vazir', sans-serif;
      background: url('https://i.imgur.com/5VJzjef.jpeg') no-repeat center center fixed;
      background-size: cover;
      color: #fff;
      text-align: center;
      padding: 30px;
      direction: rtl;
    }

    .container {
      background: rgba(0, 0, 0, 0.7);
      padding: 25px;
      border-radius: 15px;
      max-width: 600px;
      margin: auto;
      box-shadow: 0 0 15px #ff0066;
    }

    h1 {
      font-size: 2em;
      color: #ff0066;
    }

    .player-code {
      font-size: 1.5em;
      margin: 20px 0;
      background: #111;
      padding: 10px;
      border-radius: 10px;
      border: 2px dashed #ff0066;
    }

    .status {
      font-size: 1.2em;
      margin-top: 20px;
    }

    .start-btn {
      background-color: #ff0066;
      border: none;
      color: white;
      padding: 15px 30px;
      font-size: 1.2em;
      border-radius: 10px;
      margin-top: 30px;
      display: none;
    }

    .hidden {
      display: none;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>🦑 ورود به اسکوئید گیم</h1>
    <div class="player-code" id="playerCode">کد شما: بازیکن ...</div>
    <div class="status" id="statusText">در انتظار تأیید توسط فرمانده...</div>
    <button class="start-btn" id="startGameBtn" onclick="startGame()">🎮 ورود به بازی</button>
  </div>

  <script>
    const urlParams = new URLSearchParams(window.location.search);
    const userId = urlParams.get('user_id') || 'unknown';
    const userName = urlParams.get('username') || 'بدون نام';

    // شبیه‌سازی کد بازیکن
    const code = "00" + (parseInt(userId.slice(-3)) || Math.floor(Math.random() * 999));
    document.getElementById("playerCode").innerText = "کد شما: بازیکن " + code;

    // شبیه‌سازی تأیید (اینجا دستی هست. بعدا با دیتابیس واقعی میشه)
    const approvedUsers = ["123456789", "987654321"]; // این لیست رو خودت باید در آینده با بک‌اند کنترل کنی

    if (approvedUsers.includes(userId)) {
      document.getElementById("statusText").innerText = "✅ تأیید شدید! آماده‌اید برای ورود به بازی؟";
      document.getElementById("startGameBtn").style.display = "inline-block";
    } else {
      document.getElementById("statusText").innerText = "⏳ در انتظار تأیید توسط فرمانده...";
    }

    function startGame() {
      alert("🚀 بازی به‌زودی شروع میشه... (اینجا مرحله بازی طراحی میشه)");
      // window.location.href = "glass-bridge.html"; // اگر صفحه بازی آماده داشتی
    }
  </script>
</body>
</html># telegram-stars-webappi
