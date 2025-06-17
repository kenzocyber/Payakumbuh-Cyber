# Payakumbuh-Cyber
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <title>PAYAKUMBUH CYBER | PEMIMPIN</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body, html {
      height: 100%;
      overflow: hidden;
      font-family: 'Orbitron', sans-serif;
      color: #ffffff;
      background: #000;
    }

    canvas {
      position: fixed;
      top: 0;
      left: 0;
      z-index: -1;
    }

    header {
      padding: 60px 20px;
      text-align: center;
      background: rgba(0, 0, 0, 0.7);
      box-shadow: 0 0 30px #00ffe0;
    }

    header h1 {
      font-size: 3em;
      color: #00ffe0;
      text-shadow: 0 0 10px #00ffe0;
    }

    header p {
      font-size: 1.1em;
      color: #ccc;
    }

    section {
      padding: 40px 20px;
      max-width: 1000px;
      margin: auto;
      background: rgba(0, 0, 0, 0.6);
      border-radius: 10px;
      margin-top: 20px;
    }

    h2 {
      font-size: 2em;
      color: #00ffe0;
      margin-bottom: 20px;
      border-bottom: 2px solid #00ffe0;
      padding-bottom: 5px;
    }

    .skills-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
      gap: 20px;
      margin-top: 20px;
    }

    .skill-box {
      background-color: #111;
      border: 1px solid #00ffe0;
      padding: 15px;
      text-align: center;
      border-radius: 10px;
      transition: 0.3s;
    }

    .skill-box:hover {
      background-color: #00ffe0;
      color: #000;
      transform: scale(1.05);
    }

    .contact {
      font-size: 1.1em;
      line-height: 2em;
    }

    .contact a {
      color: #00ffe0;
      text-decoration: none;
    }

    .contact a:hover {
      text-decoration: underline;
    }

    footer {
      background-color: rgba(0, 0, 0, 0.7);
      padding: 30px 20px;
      text-align: center;
      color: #aaa;
      font-size: 0.9em;
      border-top: 1px solid #00ffe0;
      margin-top: 30px;
    }

    .desc {
      margin-top: 20px;
      font-style: italic;
      color: #ccc;
      text-align: center;
      padding: 10px;
    }
  </style>
</head>
<body>

<canvas id="matrix"></canvas>

<header>
  <h1>PAYAKUMBUH CYBER</h1>
  <p>PEMIMPIN ETICAL HACKING INDONESIA</p>
</header>

<section>
  <h2>SKILL</h2>
  <div class="skills-grid">
    <div class="skill-box">Python</div>
    <div class="skill-box">Termux</div>
    <div class="skill-box">Brute Force</div>
    <div class="skill-box">SQL Injection</div>
    <div class="skill-box">Web Exploit</div>
    <div class="skill-box">OSINT</div>
  </div>
</section>

<section>
  <h2>KONTAK</h2>
  <div class="contact">
    Made by: Kenzo<br>
    Email: <a href="mailto:pykcyber@gmail.com">pykcyber@gmail.com</a><br>
    WhatsApp: <a href="https://wa.me/6283143490913" target="_blank">6283143490913</a><br>
    Instagram: <a href="https://instagram.com/__21chochocaramel" target="_blank">@__21chochocaramel</a><br><br>
    Supported by: <strong>Beritapayakumbuh</strong><br><br>
    <em>If you need our services, please contact us via the contact above.</em>
  </div>
</section>

<section class="desc">
  <p>Kami berasal dari rasa penasaran, bergerak untuk pertahanan digital.<br>
  <strong>Payakumbuh Cyber Defense</strong> — dari rasa ingin tahu, menuju perlindungan siber.</p>
</section>

<footer>
  Copyright is protected by law © 2025 PAYAKUMBUH CYBER
</footer>

<script>
  // Matrix Effect
  const canvas = document.getElementById('matrix');
  const ctx = canvas.getContext('2d');

  canvas.height = window.innerHeight;
  canvas.width = window.innerWidth;

  const letters = "01";
  const fontSize = 14;
  const columns = canvas.width / fontSize;
  const drops = [];

  for (let i = 0; i < columns; i++) {
    drops[i] = 1;
  }

  function draw() {
    ctx.fillStyle = "rgba(0, 0, 0, 0.05)";
    ctx.fillRect(0, 0, canvas.width, canvas.height);
    ctx.fillStyle = "#00ffe0";
    ctx.font = fontSize + "px monospace";

    for (let i = 0; i < drops.length; i++) {
      const text = letters[Math.floor(Math.random() * letters.length)];
      ctx.fillText(text, i * fontSize, drops[i] * fontSize);
      if (drops[i] * fontSize > canvas.height && Math.random() > 0.975) {
        drops[i] = 0;
      }
      drops[i]++;
    }
  }

  setInterval(draw, 33);
</script>

</body>
</html>
