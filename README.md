
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>PAYAKUMBUH CYBER | PEMIMPIN</title>
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
      overflow-x: hidden;
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
      background: linear-gradient(145deg, #0d0d0d, #1a1a1a);
      box-shadow: 0 0 30px #00ffe0;
    }
    header h1 {
      font-size: 3em;
      color: #00ffe0;
      text-shadow: 0 0 10px #00ffe0;
    }
    header p {
      margin-top: 10px;
      font-size: 1.1em;
      color: #ccc;
    }
    section {
      padding: 40px 20px;
      max-width: 1000px;
      margin: auto;
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
      background-color: #0d0d0d;
      padding: 30px 20px;
      text-align: center;
      color: #aaa;
      font-size: 0.9em;
      border-top: 1px solid #00ffe0;
    }
    .btn {
      display: inline-block;
      margin: 10px 5px;
      padding: 10px 20px;
      border: 1px solid #00ffe0;
      color: #00ffe0;
      border-radius: 5px;
      transition: 0.3s;
      text-decoration: none;
    }
    .btn:hover {
      background-color: #00ffe0;
      color: #000;
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
  <h2>KEAHLIAN HACKING</h2>
  <div class="skills-grid">
    <div class="skill-box">SQL Injection</div>
    <div class="skill-box">XSS (Cross Site Scripting)</div>
    <div class="skill-box">DDoS Attack</div>
    <div class="skill-box">Brute Force Login</div>
    <div class="skill-box">WiFi Cracking</div>
    <div class="skill-box">Social Engineering</div>
    <div class="skill-box">Python Exploit</div>
    <div class="skill-box">Phishing Tools</div>
  </div>
</section>

<section>
  <h2>KONTAK KAMI</h2>
  <div class="contact">
    <p><strong>Email:</strong> <a href="mailto:pykcyber@gmail.com">pykcyber@gmail.com</a></p>
    <p><strong>WhatsApp:</strong> <a href="https://wa.me/6283143490913">6283143490913</a></p>
    <p><strong>Instagram:</strong> <a href="https://instagram.com/__21chochocaramel">@__21chochocaramel</a></p>
    <p><strong>Announcement:</strong> Hubungi kami melalui kontak di atas jika Anda butuh jasa kami.</p>
  </div>
</section>

<footer>
  <p>Made by: Kenzo</p>
  <p>Supported by: Beritapayakumbuh</p>
  <p>Copyright is protected by law</p>
</footer>

<script>
  var canvas = document.getElementById("matrix");
  var ctx = canvas.getContext("2d");
  canvas.height = window.innerHeight;
  canvas.width = window.innerWidth;
  var letters = "01".split("");
  var fontSize = 14;
  var columns = canvas.width / fontSize;
  var drops = [];
  for (var x = 0; x < columns; x++) drops[x] = 1;

  function draw() {
    ctx.fillStyle = "rgba(0, 0, 0, 0.05)";
    ctx.fillRect(0, 0, canvas.width, canvas.height);
    ctx.fillStyle = "#00ffe0";
    ctx.font = fontSize + "px monospace";
    for (var i = 0; i < drops.length; i++) {
      var text = letters[Math.floor(Math.random() * letters.length)];
      ctx.fillText(text, i * fontSize, drops[i] * fontSize);
      if (drops[i] * fontSize > canvas.height && Math.random() > 0.975) drops[i] = 0;
      drops[i]++;
    }
  }

  setInterval(draw, 33);
</script>

</body>
</html>
