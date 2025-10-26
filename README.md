# Site
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Para alguém especial 💖</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: linear-gradient(to right, #ffc0cb, #ffe4e1);
      color: #333;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      text-align: center;
    }

    .card {
      background-color: white;
      padding: 40px;
      border-radius: 20px;
      box-shadow: 0 4px 20px rgba(0, 0, 0, 0.2);
      max-width: 400px;
      animation: fadeIn 2s ease;
    }

    .card h1 {
      color: #e91e63;
      margin-bottom: 20px;
    }

    .card p {
      font-size: 18px;
      margin-bottom: 30px;
    }

    .heart-button {
      background-color: #e91e63;
      color: white;
      border: none;
      padding: 15px 30px;
      font-size: 16px;
      border-radius: 50px;
      cursor: pointer;
      transition: background 0.3s ease;
    }

    .heart-button:hover {
      background-color: #c2185b;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(-20px); }
      to { opacity: 1; transform: translateY(0); }
    }
  </style>
</head>
<body>
  <div class="card">
    <h1>Oi, pessoa linda! 💕</h1>
    <p>Criei esse cantinho só pra dizer que você é muito especial pra mim.<br>Seu sorriso ilumina meus dias e seu jeitinho me encanta cada vez mais.</p>
    <button class="heart-button" onclick="alert('Você ganhou um pedacinho do meu coração 💘')">Clique aqui 💖</button>
  </div>
</body>
</html>
