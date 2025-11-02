<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Para alguém especial 💖</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: linear-gradient(135deg, #667eea 0%, #764ba2 50%, #f093fb 100%);
      color: #333;
      overflow: hidden;
      height: 100vh;
    }
    
    .hearts-bg {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      pointer-events: none;
      z-index: 1;
    }
    
    .floating-heart {
      position: absolute;
      font-size: 20px;
      animation: float-up 4s ease-in infinite;
      opacity: 0;
    }
    
    @keyframes float-up {
      0% {
        transform: translateY(0) rotate(0deg);
        opacity: 1;
      }
      100% {
        transform: translateY(-100vh) rotate(360deg);
        opacity: 0;
      }
    }
    
    .container {
      position: relative;
      z-index: 2;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      padding: 20px;
    }
    
    .card {
      background: rgba(255, 255, 255, 0.95);
      backdrop-filter: blur(10px);
      padding: 50px 40px;
      border-radius: 30px;
      box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
      max-width: 500px;
      width: 100%;
      animation: fadeIn 1.5s ease;
      position: relative;
    }
    
    .step {
      display: none;
      animation: slideIn 0.6s ease;
    }
    
    .step.active {
      display: block;
    }
    
    @keyframes fadeIn {
      from { 
        opacity: 0; 
        transform: scale(0.8); 
      }
      to { 
        opacity: 1; 
        transform: scale(1); 
      }
    }
    
    @keyframes slideIn {
      from {
        opacity: 0;
        transform: translateX(30px);
      }
      to {
        opacity: 1;
        transform: translateX(0);
      }
    }
    
    .card h1 {
      background: linear-gradient(135deg, #e91e63, #9c27b0);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      margin-bottom: 20px;
      font-size: 32px;
    }
    
    .card p {
      font-size: 18px;
      line-height: 1.6;
      margin-bottom: 30px;
      color: #555;
    }
    
    .heart-button {
      background: linear-gradient(135deg, #e91e63, #9c27b0);
      color: white;
      border: none;
      padding: 15px 40px;
      font-size: 18px;
      font-weight: 600;
      border-radius: 50px;
      cursor: pointer;
      transition: all 0.3s ease;
      box-shadow: 0 4px 15px rgba(233, 30, 99, 0.4);
      position: relative;
      overflow: hidden;
    }
    
    .heart-button:hover {
      transform: translateY(-3px);
      box-shadow: 0 6px 25px rgba(233, 30, 99, 0.6);
    }
    
    .heart-button:active {
      transform: translateY(-1px);
    }
    
    .heart-button::before {
      content: '';
      position: absolute;
      top: 50%;
      left: 50%;
      width: 0;
      height: 0;
      border-radius: 50%;
      background: rgba(255, 255, 255, 0.3);
      transform: translate(-50%, -50%);
      transition: width 0.6s, height 0.6s;
    }
    
    .heart-button:hover::before {
      width: 300px;
      height: 300px;
    }
    
    .heart-button span {
      position: relative;
      z-index: 1;
    }
    
    .options {
      display: flex;
      gap: 15px;
      flex-wrap: wrap;
      justify-content: center;
    }
    
    .option-btn {
      background: white;
      color: #e91e63;
      border: 2px solid #e91e63;
      padding: 12px 25px;
      font-size: 16px;
      border-radius: 25px;
      cursor: pointer;
      transition: all 0.3s ease;
    }
    
    .option-btn:hover {
      background: #e91e63;
      color: white;
      transform: scale(1.05);
    }
    
    .message-reveal {
      background: linear-gradient(135deg, #ffeaa7, #fdcb6e);
      padding: 20px;
      border-radius: 15px;
      margin-top: 20px;
      font-weight: 600;
      color: #2d3436;
      animation: pulse 2s infinite;
    }
    
    @keyframes pulse {
      0%, 100% {
        transform: scale(1);
      }
      50% {
        transform: scale(1.02);
      }
    }
    
    .emoji-rain {
      position: fixed;
      font-size: 30px;
      animation: fall 3s linear;
      pointer-events: none;
      z-index: 999;
    }
    
    @keyframes fall {
      to {
        transform: translateY(100vh) rotate(360deg);
        opacity: 0;
      }
    }
    
    .final-message {
      text-align: center;
    }
    
    .final-message h2 {
      color: #e91e63;
      margin-bottom: 15px;
      font-size: 28px;
    }
    
    .Hearth-counter {
      font-size: 48px;
      font-weight: bold;
      background: linear-gradient(135deg, #e91e63, #9c27b0);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      margin: 20px 0;
      animation: heartbeat 1.5s infinite;
    }
    
    @keyframes heartbeat {
      0%, 100% { transform: scale(1); }
      10%, 30% { transform: scale(1.1); }
      20%, 40% { transform: scale(0.9); }
    }
    
    @media (max-width: 600px) {
      .card {
        padding: 30px 25px;
      }
      
      .card h1 {
        font-size: 26px;
      }
      
      .card p {
        font-size: 16px;
      }
    }
  </style>
</head>
<body>
  <div class="hearts-bg" id="heartsBg"></div>
  
  <div class="container">
    <div class="card">
      <div class="step active" id="step1">
        <h1>Oi, pessoa linda! 💕</h1>
        <p>Preparei uma surpresa especial pra você. Está pronta(o) para descobrir?</p>
        <button class="heart-button" onclick="nextStep(2)">
          <span>Sim, quero ver! ✨</span>
        </button>
      </div>
      
      <div class="step" id="step2">
        <h1>Você sabia? 🌟</h1>
        <p>Você é uma pessoa Incrivel e muito Legall, Que bom que você notou!</p>
        <button class="heart-button" onclick="nextStep(3)">
          <span>Continuar 💖</span>
        </button>
      </div>
      
      <div class="step" id="step3">
        <h1>Uma pergunta... 🤔</h1>
        <p>O que você mais gosta em mim?</p>
        <div class="options">
          <button class="option-btn" onclick="showMessage('Seu sorriso')">Meu sorriso 😊</button>
          <button class="option-btn" onclick="showMessage('Seu jeito de ser')">Meu jeito 🥰</button>
          <button class="option-btn" onclick="showMessage('Seu humor')">Meu humor 😄</button>
          <button class="option-btn" onclick="showMessage('Tudo!')">Tudo! 💕</button>
        </div>
        <div id="messageBox"></div>
      </div>
      
      <div class="step" id="step4">
        <div class="final-message">
          <h2>E agora a melhor parte... 🎉</h2>
          <p>Você ilumina minha vida todos os dias!</p>
          <div class="Hearth-counter" id="HearthCounter">0%</div>
          <p style="font-size: 16px; color: #666;">O carinho de verdade</p>
          <button class="heart-button" onclick="explodeHearts()" style="margin-top: 20px;">
            <span>Clique para uma surpresa final! 💝</span>
          </button>
        </div>
      </div>
    </div>
  </div>

  <script>
    let currentStep = 1;
    
    function createFloatingHeart() {
      const heart = document.createElement('div');
      heart.className = 'floating-heart';
      heart.textContent = ['💕', '💖', '💗', '💘', '💝'][Math.floor(Math.random() * 5)];
      heart.style.left = Math.random() * 100 + '%';
      heart.style.animationDelay = Math.random() * 2 + 's';
      heart.style.animationDuration = (Math.random() * 2 + 3) + 's';
      document.getElementById('heartsBg').appendChild(heart);
      
      setTimeout(() => heart.remove(), 5000);
    }
    
    setInterval(createFloatingHeart, 300);
    
    function nextStep(step) {
      document.getElementById(`step${currentStep}`).classList.remove('active');
      document.getElementById(`step${step}`).classList.add('active');
      currentStep = step;
      
      if (step === 4) {
        animateCounter();
      }
    }
    
    function showMessage(choice) {
      const messages = {
        'Seu sorriso': 'Agradeço! Mas o seu sorriso deveria ser patrimônio mundial!😊',
        'Seu jeito de ser': 'Que bom! O meu segredo é simples: eu te uso como régua de inspiração. 🥰',
        'Seu humor': 'Fico feliz em te fazer rir! 😄',
        'Tudo!': 'Você não existe! Juro! Você é incrível demais!💕'
      };
      
      const messageBox = document.getElementById('messageBox');
      messageBox.innerHTML = `<div class="message-reveal">${messages[choice]}</div>`;
      
      setTimeout(() => {
        nextStep(4);
      }, 3000);
    }
    
    function animateCounter() {
      let count = 0;
      const counter = document.getElementById('Counter');
      const interval = setInterval(() => {
        count += 5;
        counter.textContent = count + '%';
        if (count >= 100) {
          clearInterval(interval);
          counter.textContent = '∞ 💖';
        }
      }, 50);
    }
    
    function explodeHearts() {
      const emojis = ['💖', '💕', '💗', '💘', '💝', '🌟', '✨', '⭐', '🎉', '🎊'];
      
      for (let i = 0; i < 50; i++) {
        setTimeout(() => {
          const emoji = document.createElement('div');
          emoji.className = 'emoji-rain';
          emoji.textContent = emojis[Math.floor(Math.random() * emojis.length)];
          emoji.style.left = Math.random() * 100 + '%';
          emoji.style.top = '-50px';
          emoji.style.animationDuration = (Math.random() * 2 + 2) + 's';
          document.body.appendChild(emoji);
          
          setTimeout(() => emoji.remove(), 3000);
        }, i * 100);
      }
      
      setTimeout(() => {
        alert('Você é incrível e muito especial pra mim! Obrigada por existir! 💖✨');
      }, 2000);
    }
  </script>
</body>
</html>
