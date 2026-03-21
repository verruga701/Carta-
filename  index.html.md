<!DOCTYPE html>  
<html lang="es">  
<head>  
  <meta charset="UTF-8" />  
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />  
  <title>Para Yamilet 💙</title>  
  <style>  
    * {  
      box-sizing: border-box;  
    }  
  
    html, body {  
      margin: 0;  
      padding: 0;  
      min-height: 100%;  
      overflow-x: hidden;  
      overflow-y: auto;  
      font-family: Arial, sans-serif;  
      scroll-behavior: smooth;  
    }  
  
    body {  
      color: #24324f;  
      background:  
        radial-gradient(circle at top, #ffe7a8 0%, #ffd6b3 25%, #ffd3e3 55%, #d8ecff 78%, #c5ddff 100%);  
      position: relative;  
    }  
  
    .sunset-glow {  
      position: fixed;  
      inset: 0;  
      background:  
        radial-gradient(circle at 50% 12%, rgba(255,255,255,0.38), transparent 20%),  
        radial-gradient(circle at 82% 10%, rgba(255,212,120,0.25), transparent 14%),  
        radial-gradient(circle at 18% 16%, rgba(255,180,200,0.18), transparent 16%);  
      pointer-events: none;  
      z-index: 0;  
    }  
  
    .floating {  
      position: fixed;  
      top: -60px;  
      pointer-events: none;  
      z-index: 1;  
      animation-name: fall;  
      animation-timing-function: linear;  
      animation-fill-mode: forwards;  
      opacity: 0.95;  
      filter: drop-shadow(0 4px 8px rgba(0,0,0,0.12));  
    }  
  
    .page {  
      position: relative;  
      z-index: 2;  
      max-width: 920px;  
      margin: 0 auto;  
      padding: 28px 16px 70px;  
    }  
  
    .hero {  
      text-align: center;  
      padding-top: 10px;  
      margin-bottom: 24px;  
    }  
  
    .hero h1 {  
      margin: 0;  
      font-size: clamp(2.4rem, 7vw, 4.3rem);  
      color: #ff5fa8;  
      text-shadow: 0 3px 12px rgba(255,255,255,0.35);  
    }  
  
    .hero p {  
      margin-top: 12px;  
      font-size: clamp(1.1rem, 3vw, 1.5rem);  
      color: #355e96;  
      font-weight: bold;  
    }  
  
    .message-box {  
      background: rgba(255,255,255,0.28);  
      border: 2px solid rgba(255,255,255,0.35);  
      border-radius: 28px;  
      padding: 28px 20px;  
      box-shadow: 0 12px 30px rgba(0,0,0,0.08);  
      backdrop-filter: blur(6px);  
      text-align: center;  
      margin-bottom: 34px;  
      animation: fadeUp 1.2s ease;  
    }  
  
    .message-box p {  
      margin: 0;  
      white-space: pre-line;  
      line-height: 1.9;  
      font-size: clamp(1.15rem, 3.2vw, 1.65rem);  
      color: #26395a;  
    }  
  
    .scene {  
      position: relative;  
      min-height: 520px;  
      display: flex;  
      align-items: center;  
      justify-content: center;  
      margin-top: 10px;  
      animation: fadeUp 1.6s ease;  
    }  
  
    .ring {  
      position: relative;  
      width: min(92vw, 470px);  
      height: min(92vw, 470px);  
      display: flex;  
      align-items: center;  
      justify-content: center;  
    }  
  
    .orbit {  
      position: absolute;  
      inset: 0;  
      animation: spin 22s linear infinite;  
    }  
  
    .sunflower {  
      position: absolute;  
      width: 95px;  
      height: 95px;  
      display: flex;  
      align-items: center;  
      justify-content: center;  
      animation: flowerWobble 5s ease-in-out infinite;  
    }  
  
    .sunflower::before {  
      content: "🌻";  
      font-size: 74px;  
      position: absolute;  
      inset: 0;  
      display: flex;  
      align-items: center;  
      justify-content: center;  
    }  
  
    .sunflower span {  
      position: relative;  
      z-index: 2;  
      color: #fff7db;  
      font-weight: bold;  
      font-size: 13px;  
      text-shadow: 0 1px 4px rgba(0,0,0,0.55);  
      transform: rotate(-18deg);  
    }  
  
    .s1 { top: 0; left: 50%; transform: translate(-50%, 0); }  
    .s2 { top: 14%; right: 5%; }  
    .s3 { top: 50%; right: -1%; transform: translateY(-50%); }  
    .s4 { bottom: 14%; right: 5%; }  
    .s5 { bottom: 0; left: 50%; transform: translate(-50%, 0); }  
    .s6 { bottom: 14%; left: 5%; }  
    .s7 { top: 50%; left: -1%; transform: translateY(-50%); }  
    .s8 { top: 14%; left: 5%; }  
  
    .dog-wrap {  
      position: relative;  
      width: 245px;  
      height: 285px;  
      display: flex;  
      align-items: center;  
      justify-content: center;  
      animation: floatDog 4.5s ease-in-out infinite;  
      z-index: 3;  
    }  
  
    .dog {  
      position: relative;  
      width: 190px;  
      height: 220px;  
    }  
  
    .head {  
      position: absolute;  
      top: 8px;  
      left: 45px;  
      width: 100px;  
      height: 95px;  
      background: #fff;  
      border: 4px solid #222;  
      border-radius: 50%;  
      z-index: 3;  
    }  
  
    .ear-left, .ear-right {  
      position: absolute;  
      width: 34px;  
      height: 62px;  
      background: #222;  
      border-radius: 20px;  
      top: 2px;  
      z-index: 2;  
    }  
  
    .ear-left { left: 32px; transform: rotate(-18deg); }  
    .ear-right { right: 32px; transform: rotate(18deg); }  
  
    .eye-left, .eye-right {  
      position: absolute;  
      width: 8px;  
      height: 8px;  
      background: #222;  
      border-radius: 50%;  
      top: 44px;  
      z-index: 4;  
    }  
  
    .eye-left { left: 70px; }  
    .eye-right { right: 70px; }  
  
    .nose {  
      position: absolute;  
      width: 18px;  
      height: 13px;  
      background: #222;  
      border-radius: 50%;  
      top: 58px;  
      left: 50%;  
      transform: translateX(-50%);  
      z-index: 4;  
    }  
  
    .mouth {  
      position: absolute;  
      width: 34px;  
      height: 18px;  
      border-bottom: 3px solid #222;  
      border-radius: 0 0 20px 20px;  
      top: 69px;  
      left: 50%;  
      transform: translateX(-50%);  
      z-index: 4;  
    }  
  
    .body-dog {  
      position: absolute;  
      top: 88px;  
      left: 58px;  
      width: 72px;  
      height: 85px;  
      background: #fff;  
      border: 4px solid #222;  
      border-radius: 34px;  
      z-index: 1;  
    }  
  
    .arm-left, .arm-right {  
      position: absolute;  
      width: 22px;  
      height: 58px;  
      background: #fff;  
      border: 4px solid #222;  
      border-radius: 18px;  
      top: 102px;  
      z-index: 0;  
    }  
  
    .arm-left { left: 45px; transform: rotate(8deg); }  
    .arm-right { right: 45px; transform: rotate(-8deg); }  
  
    .sign {  
      position: absolute;  
      bottom: 20px;  
      left: 50%;  
      transform: translateX(-50%);  
      background: linear-gradient(180deg, #d8efff, #b9dfff);  
      border: 4px solid #5a97df;  
      border-radius: 18px;  
      padding: 16px 22px;  
      min-width: 170px;  
      text-align: center;  
      color: #295892;  
      font-weight: bold;  
      font-size: 1.05rem;  
      box-shadow: 0 10px 18px rgba(0,0,0,0.12);  
      z-index: 6;  
    }  
  
    .sign span {  
      display: block;  
      font-size: 2rem;  
      margin-top: 2px;  
    }  
  
    .final-note {  
      text-align: center;  
      margin-top: 18px;  
      font-size: 1rem;  
      color: #4c6f9f;  
      font-weight: bold;  
    }  
  
    @keyframes fall {  
      0% {  
        transform: translateY(-50px) translateX(0) rotate(0deg);  
        opacity: 0;  
      }  
      10% {  
        opacity: 1;  
      }  
      100% {  
        transform: translateY(115vh) translateX(50px) rotate(360deg);  
        opacity: 0;  
      }  
    }  
  
    @keyframes spin {  
      from { transform: rotate(0deg); }  
      to { transform: rotate(360deg); }  
    }  
  
    @keyframes flowerWobble {  
      0%, 100% { transform: scale(1) rotate(0deg); }  
      50% { transform: scale(1.06) rotate(4deg); }  
    }  
  
    @keyframes floatDog {  
      0%, 100% { transform: translateY(0); }  
      50% { transform: translateY(-8px); }  
    }  
  
    @keyframes fadeUp {  
      from {  
        opacity: 0;  
        transform: translateY(18px);  
      }  
      to {  
        opacity: 1;  
        transform: translateY(0);  
      }  
    }  
  
    @media (max-width: 600px) {  
      .message-box {  
        padding: 24px 16px;  
      }  
  
      .scene {  
        min-height: 440px;  
      }  
  
      .ring {  
        width: 350px;  
        height: 420px;  
      }  
  
      .sunflower {  
        width: 78px;  
        height: 78px;  
      }  
  
      .sunflower::before {  
        font-size: 62px;  
      }  
  
      .sunflower span {  
        font-size: 11px;  
      }  
  
      .dog-wrap {  
        transform: scale(0.92);  
      }  
    }  
  </style>  
</head>  
<body>  
  <div class="sunset-glow"></div>  
  
  <div class="page">  
    <section class="hero">  
      <h1>Para YAMILET 💙</h1>  
      <p>Lo hice pensando en ti</p>  
    </section>  
  
    <section class="message-box">  
      <p>Te pido perdón como me comporté, fui muy inmaduro contigo.  
  
Me gustas desde hace mucho tiempo, pero no me he atrevido a decírtelo. En ocasiones me ganan los nervios y se me olvida.  
  
Sé que no hablamos, pero eso no quiere decir que ya no sienta lo mismo. Al contrario, te quiero más, me gustas más.  
  
Todo este tiempo no he dejado de pensar en ti. Por más loco que suene, te sueño por las noches frecuentemente.  
  
Y sé que entiendo y acepto tu respuesta, pero dame una chance. 💙</p>  
    </section>  
  
    <section class="scene">  
      <div class="ring">  
        <div class="orbit">  
          <div class="sunflower s1"><span>Te amo</span></div>  
          <div class="sunflower s2"><span>Te amo</span></div>  
          <div class="sunflower s3"><span>Te amo</span></div>  
          <div class="sunflower s4"><span>Te amo</span></div>  
          <div class="sunflower s5"><span>Te amo</span></div>  
          <div class="sunflower s6"><span>Te amo</span></div>  
          <div class="sunflower s7"><span>Te amo</span></div>  
          <div class="sunflower s8"><span>Te amo</span></div>  
        </div>  
  
        <div class="dog-wrap">  
          <div class="dog">  
            <div class="ear-left"></div>  
            <div class="ear-right"></div>  
            <div class="head"></div>  
            <div class="eye-left"></div>  
            <div class="eye-right"></div>  
            <div class="nose"></div>  
            <div class="mouth"></div>  
            <div class="arm-left"></div>  
            <div class="arm-right"></div>  
            <div class="body-dog"></div>  
          </div>  
          <div class="sign">Te amo <span>💙</span></div>  
        </div>  
      </div>  
    </section>  
  
    <div class="final-note">Con todo mi corazón 💙</div>  
  </div>  
  
  <script>  
    const items = ["💙", "🩵", "🌻", "💙", "🩵", "🌻", "🩵", "💙"];  
  
    function createFloatingItem() {  
      const el = document.createElement("div");  
      el.className = "floating";  
      el.textContent = items[Math.floor(Math.random() * items.length)];  
      el.style.left = Math.random() * 100 + "vw";  
      el.style.fontSize = (22 + Math.random() * 22) + "px";  
      el.style.animationDuration = (6 + Math.random() * 5) + "s";  
      document.body.appendChild(el);  
  
      setTimeout(() => {  
        el.remove();  
      }, 12000);  
    }  
  
    setInterval(createFloatingItem, 180);  
  
    for (let i = 0; i < 18; i++) {  
      setTimeout(createFloatingItem, i * 180);  
    }  
  </script>  
</body>  
</html>  
