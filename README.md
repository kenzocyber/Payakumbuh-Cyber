
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>PAYAKUMBUH CYBER | PEMIMPIN</title>
  <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@600&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    body {
      font-family: 'Orbitron', sans-serif;
      background-color: #0a0a0a;
      color: #ffffff;
      min-height: 100vh;
      overflow-x: hidden;
      position: relative;
      z-index: 1;
    }
    #matrix {
      position: fixed;
      top: 0;
      left: 0;
      z-index: 0;
      width: 100%;
      height: 100%;
    }
    header {
      padding: 60px 20px;
      text-align: center;
      background: linear-gradient(145deg, #0d0d0d, #1a1a1a);
      box-shadow: 0 0 30px #00ffe0;
      z-index: 2;
      position: relative;
    }
    header h1 {
      font-size: 3em;
      color: #00ffe0;
      text-shadow: 0 0 10px #00ffe0;
    }
    header p {
      font-size: 1.2em;
      color: #ccc;
      margin-top: 10px;
    }
    section {
      padding: 40px 20px;
      max-width: 1000px;
      margin: auto;
      position: relative;
      z-index: 2;
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
      background: #111;
      border: 1px solid #00ffe0;
      padding: 15px;
      text-align: center;
      border-radius: 10px;
      transition: 0.3s;
    }
    .skill-box:hover {
      background: #00ffe0;
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
      background: #0d0d0d;
      padding: 30px 20px;
      text-align: center;
      color: #aaa;
      font-size: 0.9em;
      border-top: 1px solid #00ffe0;
      position: relative;
      z-index: 2;
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
  <h2>KEAHLIAN</h2>
  <div class="skills-grid">
    <div class="skill-box">Python</div>
    <div class="skill-box">Termux</div>
    <div class="skill-box">Brute Force</div>
    <div class="skill-box">Tracking</div>
    <div class="skill-box">Cyber Defense</div>
    <div class="skill-box">Phishing</div>
  </div>
</section>

<section>
  <h2>TENTANG KAMI</h2>
  <p class="contact">
    Kami berasal dari rasa penasaran, bergerak untuk pertahanan digital.<br>
    <strong>Payakumbuh Cyber Defense</strong> — dari rasa ingin tahu, menuju perlindungan siber.<br><br>
    Made by: <strong>Kenzo</strong><br>
    Email: <a href="mailto:pykcyber@gmail.com">pykcyber@gmail.com</a><br>
    WhatsApp: <a href="https://wa.me/6283143490913">+62 831-4349-0913</a><br>
    IG: <a href="https://instagram.com/__21chochocaramel">@__21chochocaramel</a><br>
    Supported by: <strong>BeritaPayakumbuh</strong><br>
  </p>
</section>

<footer>
  &copy; 2025 Payakumbuh Cyber. Hak Cipta Dilindungi Undang-Undang.
</footer>

<script>
  var c = document.getElementById("matrix");
  var ctx = c.getContext("2d");
  c.height = window.innerHeight;
  c.width = window.innerWidth;

  var letters = "01";
  letters = letters.split("");
  var fontSize = 14;
  var columns = c.width / fontSize;
  var drops = [];
  for (var x = 0; x < columns; x++) drops[x] = 1;

  function draw() {
    ctx.fillStyle = "rgba(0, 0, 0, 0.05)";
    ctx.fillRect(0, 0, c.width, c.height);
    ctx.fillStyle = "#00ffe0";
    ctx.font = fontSize + "px monospace";
    for (var i = 0; i < drops.length; i++) {
      var text = letters[Math.floor(Math.random() * letters.length)];
      ctx.fillText(text, i * fontSize, drops[i] * fontSize);
      if (drops[i] * fontSize > c.height && Math.random() > 0.975) drops[i] = 0;
      drops[i]++;
    }
  }

  setInterval(draw, 33);
</script>

</body>
</html>
