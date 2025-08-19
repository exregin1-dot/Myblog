<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <title>Ошибка сервера</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Russo+One&display=swap');

    body {
      margin: 0;
      padding: 0;
      height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      overflow: hidden;
      font-family: 'Russo One', sans-serif;
      color: white;
      background: url("https://images.unsplash.com/photo-1507525428034-b723cf961d3e?ixlib=rb-4.0.3&auto=format&fit=crop&w=1650&q=80") no-repeat center center/cover;
      position: relative;
    }

    /* затемнение */
    body::before {
      content: "";
      position: absolute;
      top: 0; left: 0;
      width: 100%; height: 100%;
      background: rgba(0,0,0,0.85);
      z-index: 0;
    }

    /* молния */
    .lightning {
      position: absolute;
      top: 0; left: 0;
      width: 100%; height: 100%;
      background: rgba(255,255,255,0.9);
      opacity: 0;
      z-index: 1;
    }

    /* дождь */
    .rain {
      position: absolute;
      top: -120px;
      width: 2px;
      height: 100px;
      background: rgba(255,255,255,0.25);
      animation: fall linear infinite;
      z-index: 2;
    }
    @keyframes fall {
      0% { transform: translateY(-120px); }
      100% { transform: translateY(110vh); }
    }

    /* блески */
    .sparkle {
      position: absolute;
      border-radius: 50%;
      background: rgba(255,255,255,0.8);
      width: 3px; height: 3px;
      opacity: 0.7;
      animation: float 6s infinite ease-in-out;
      z-index: 2;
    }
    @keyframes float {
      0% { transform: translateY(0) scale(0.5); opacity: 0.5; }
      50% { transform: translateY(-40px) scale(1.2); opacity: 1; }
      100% { transform: translateY(0) scale(0.5); opacity: 0.3; }
    }

    /* заголовок */
    h1 {
      margin: 0;
      position: absolute;
      top: 40px;
      font-size: 4.2em;
      color: #fff;
      text-shadow: 0 0 20px #00f0ff, 0 0 50px #00e0ff;
      animation: glow 2.5s infinite alternate, fadeSlideDown 1.5s ease-out forwards;
      opacity: 0;
      z-index: 3;
    }
    @keyframes glow {
      from { text-shadow: 0 0 15px #00f0ff, 0 0 40px #00e0ff; }
      to   { text-shadow: 0 0 40px #00ffff, 0 0 80px #00e5ff; }
    }
    @keyframes fadeSlideDown {
      0% { opacity: 0; transform: translateY(-50px); }
      100% { opacity: 1; transform: translateY(0); }
    }

    /* кнопки контейнер */
    .buttons {
      display: flex;
      justify-content: center;
      gap: 45px;
      flex-wrap: wrap;
      z-index: 3;
      padding: 35px 60px;
      border-radius: 25px;
      background: rgba(255, 255, 255, 0.07);
      backdrop-filter: blur(18px);
      border: 2px solid rgba(255, 255, 255, 0.15);
      box-shadow: 0 0 25px rgba(0,0,0,0.6), 0 0 50px rgba(0, 255, 255, 0.2);
      animation: fadeSlideUp 1.5s ease-out forwards;
      opacity: 0;
    }
    @keyframes fadeSlideUp {
      0% { opacity: 0; transform: translateY(50px); }
      100% { opacity: 1; transform: translateY(0); }
    }

    /* кнопки */
    .btn {
      position: relative;
      padding: 30px 70px;
      font-size: 30px;
      border-radius: 22px;
      color: white;
      text-decoration: none;
      overflow: hidden;
      transition: 0.4s;
      display: flex;
      align-items: center;
      gap: 18px;
      backdrop-filter: blur(8px);
      border: none;
      box-shadow: 0 0 25px rgba(255,255,255,0.25);
      min-width: 260px;
      justify-content: center;
    }
    .btn i { font-size: 36px; }

    .tiktok { background: linear-gradient(135deg, #ff0050, #00f2ea); }
    .instagram { background: linear-gradient(135deg, #feda75, #d62976, #962fbf, #4f5bd5); }
    .youtube { background: linear-gradient(135deg, #ff0000, #b80000); }
    .telegram { background: linear-gradient(135deg, #0088cc, #00c6ff); }

    /* hover + ripple */
    .btn:hover {
      filter: brightness(1.25);
      box-shadow: 0 0 40px white, 0 0 70px white;
      transform: scale(1.08);
    }
    .btn:active::after {
      content: "";
      position: absolute;
      top: 50%; left: 50%;
      width: 15px; height: 15px;
      background: rgba(255,255,255,0.8);
      border-radius: 50%;
      transform: translate(-50%, -50%) scale(0);
      animation: ripple 0.6s linear;
    }
    @keyframes ripple {
      to {
        transform: translate(-50%, -50%) scale(12);
        opacity: 0;
      }
    }
    .btn:active { opacity: 0.6; }

    /* блеск по кнопке */
    .btn::before {
      content: "";
      position: absolute;
      top: -50%; left: -50%;
      width: 200%; height: 200%;
      background: radial-gradient(circle, rgba(255,255,255,0.25) 0%, transparent 70%);
      transform: rotate(25deg);
      animation: shine 5s infinite linear;
      z-index: 1;
    }
    @keyframes shine {
      0% { transform: translateX(-200%) rotate(25deg); }
      100% { transform: translateX(200%) rotate(25deg); }
    }

    /* футер */
    .footer {
      position: absolute;
      bottom: 20px;
      font-size: 20px;
      color: #ccc;
      letter-spacing: 3px;
      text-shadow: 0 0 10px #00f0ff, 0 0 20px #00e0ff;
      z-index: 3;
    }
  </style>
  <script src="https://kit.fontawesome.com/4e5b9d7f4d.js" crossorigin="anonymous"></script>
</head>
<body>
  <div class="lightning"></div>
  <h1>ОШИБКА СЕРВЕРА</h1>

  <div class="buttons">
    <a href="https://www.tiktok.com/@_error_server?_t=ZS-8yzcYAucO8e&_r=1" class="btn tiktok"><i class="fab fa-tiktok"></i> TikTok</a>
    <a href="https://www.instagram.com/_mactraxer__?igsh=MWE3Z240OGVsd3Y3bQ%3D%3D&utm_source=qr" class="btn instagram"><i class="fab fa-instagram"></i> Instagram</a>
    <a href="https://youtube.com/@erroreserver?si=xIpsTivOfrcX6qla" class="btn youtube"><i class="fab fa-youtube"></i> YouTube</a>
    <a href="https://t.me/Asysnes_tdm" class="btn telegram"><i class="fab fa-telegram"></i> Telegram</a>
  </div>

  <div class="footer">⚡ By ERROR SERVER ⚡</div>

  <!-- Звуки грома -->
  <audio id="thunderSound" src="https://www.soundjay.com/nature/thunder-1.mp3" preload="auto"></audio>

  <script>
    const body = document.body;
    const lightning = document.querySelector('.lightning');
    const thunderSound = document.getElementById("thunderSound");

    // дождь сверху
    for (let i = 0; i < 120; i++) {
      let drop = document.createElement("div");
      drop.classList.add("rain");
      drop.style.left = Math.random() * window.innerWidth + "px";
      drop.style.animationDuration = (0.6 + Math.random() * 0.8) + "s";
      body.appendChild(drop);
    }

    // блески
    for (let i = 0; i < 40; i++) {
      let sparkle = document.createElement("div");
      sparkle.classList.add("sparkle");
      sparkle.style.left = Math.random() * window.innerWidth + "px";
      sparkle.style.top = Math.random() * window.innerHeight + "px";
      sparkle.style.animationDuration = (3 + Math.random() * 6) + "s";
      body.appendChild(sparkle);
    }

    // молнии + гром
    function triggerLightning() {
      lightning.style.opacity = "1";
      setTimeout(() => lightning.style.opacity = "0", 150);
      setTimeout(() => thunderSound.play(), 400); // задержка звука после вспышки
    }

    setInterval(() => {
      if (Math.random() > 0.7) { // редкие вспышки
        triggerLightning();
      }
    }, 8000);
  </script>
</body>
</html>