<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <title>GitHub Banner - Nathan Ferreira</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: "Courier New", monospace;
    }

    body {
      background: black;
      overflow: hidden;
    }

    .container {
      position: relative;
      width: 100%;
      height: 300px;
      background: black;
      color: white;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    /* TEXTO PRINCIPAL */
    .content {
      position: relative;
      z-index: 2;
      text-align: center;
    }

    .content h1 {
      font-size: 32px;
      letter-spacing: 3px;
    }

    .content p {
      font-size: 14px;
      margin-top: 10px;
      opacity: 0.7;
    }

    /* CHUVA MATRIX */
    canvas {
      position: absolute;
      top: 0;
      left: 0;
      z-index: 1;
    }

    /* EFEITO GLITCH SUAVE */
    .glitch {
      position: relative;
      color: white;
    }

    .glitch::before,
    .glitch::after {
      content: attr(data-text);
      position: absolute;
      left: 0;
      width: 100%;
      overflow: hidden;
      color: white;
    }

    .glitch::before {
      animation: glitchTop 2s infinite linear;
    }

    .glitch::after {
      animation: glitchBottom 2s infinite linear;
    }

    @keyframes glitchTop {
      0% { clip-path: inset(0 0 90% 0); transform: translate(-1px, -1px); }
      50% { clip-path: inset(0 0 50% 0); transform: translate(1px, 1px); }
      100% { clip-path: inset(0 0 90% 0); transform: translate(0, 0); }
    }

    @keyframes glitchBottom {
      0% { clip-path: inset(90% 0 0 0); transform: translate(1px, 1px); }
      50% { clip-path: inset(50% 0 0 0); transform: translate(-1px, -1px); }
      100% { clip-path: inset(90% 0 0 0); transform: translate(0, 0); }
    }
  </style>
</head>
<body>

<div class="container">
  <canvas id="matrix"></canvas>

  <div class="content">
    <h1 class="glitch" data-text="NATHAN FERREIRA">
      NATHAN FERREIRA
    </h1>
    <p>
      Python • ETL • Automação • Power Platform • APIs • Data Engineering
    </p>
  </div>
</div>

<script>
  const canvas = document.getElementById("matrix");
  const ctx = canvas.getContext("2d");

  canvas.width = window.innerWidth;
  canvas.height = 300;

  const letters = "01ABCDEFGHIJKLMNOPQRSTUVWXYZ";
  const fontSize = 14;
  const columns = canvas.width / fontSize;

  const drops = [];

  for (let i = 0; i < columns; i++) {
    drops[i] = 1;
  }

  function draw() {
    ctx.fillStyle = "rgba(0, 0, 0, 0.05)";
    ctx.fillRect(0, 0, canvas.width, canvas.height);

    ctx.fillStyle = "#FFFFFF";
    ctx.font = fontSize + "px monospace";

    for (let i = 0; i < drops.length; i++) {
      const text = letters.charAt(Math.floor(Math.random() * letters.length));
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


<div >
  
  <img height="150em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=nathanzd&layout=compact&langs_count=7&theme=chartreuse-dark"/>
</div>
<div style="display:inline_block"><br>
  <img align="center" alt="Js" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-plain.svg">
  <img align="center" alt="HTML" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original.svg">
  <img align="center" alt="CSS" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original.svg">
  <!--<img align="center" alt="Ts" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/typescript/typescript-plain.svg">-->
  <img align="center" alt="React" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/react/react-original.svg">
  <img align="center" alt="Python" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg">
  <!--<img align="right" alt="Dragon" height="150" style="border-radius:100px;" src="https://cdn.discordapp.com/attachments/918234319548465162/922262680419577936/download20211200195447.png">-->
</div>

##

<div> 
  
  <a href = "mailto:nathan.fe.dias@gmail.com"><img src="https://img.shields.io/badge/-Gmail-%23333?style=for-the-badge&logo=gmail&logoColor=white" target="_blank"></a>
  <a href="https://www.linkedin.com/in/nathanzd/" target="_blank"><img src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white" target="_blank"></a> 
</div>


<!---
nathanzd/nathanzd is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
