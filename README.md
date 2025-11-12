<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Para Você</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Georgia', serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 40px 20px;
            overflow-x: hidden;
            overflow-y: auto;
        }

        .container {
            max-width: 600px;
            width: 100%;
            background: rgba(255, 255, 255, 0.95);
            border-radius: 20px;
            padding: 50px 40px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
            position: relative;
            animation: fadeIn 1s ease-out;
            margin: 20px auto;
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .heart {
            font-size: 60px;
            text-align: center;
            margin-bottom: 20px;
            animation: heartbeat 1.5s ease-in-out infinite;
        }

        @keyframes heartbeat {
            0%, 100% { transform: scale(1); }
            25% { transform: scale(1.1); }
            50% { transform: scale(1); }
        }

        h1 {
            color: #764ba2;
            text-align: center;
            margin-bottom: 30px;
            font-size: 2em;
        }

        .message {
            color: #333;
            line-height: 1.8;
            font-size: 1.1em;
            text-align: justify;
            margin-bottom: 25px;
        }

        .highlight {
            color: #764ba2;
            font-weight: bold;
        }

        .signature {
            text-align: right;
            font-style: italic;
            color: #666;
            margin-top: 40px;
            font-size: 1.1em;
        }

        .flowers {
            position: fixed;
            font-size: 30px;
            opacity: 0.6;
            animation: float 6s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(5deg); }
        }

        .flower1 { top: 10%; left: 10%; animation-delay: 0s; }
        .flower2 { top: 20%; right: 15%; animation-delay: 1s; }
        .flower3 { bottom: 15%; left: 8%; animation-delay: 2s; }
        .flower4 { bottom: 25%; right: 10%; animation-delay: 1.5s; }

        @media (max-width: 600px) {
            .container {
                padding: 30px 25px;
            }
            h1 {
                font-size: 1.5em;
            }
            .message {
                font-size: 1em;
            }
        }
    </style>
</head>
<body>
    <div class="flowers flower1">🌸</div>
    <div class="flowers flower2">🌺</div>
    <div class="flowers flower3">🌼</div>
    <div class="flowers flower4">🌷</div>

    <div class="container">
        <h1>Para Você</h1>
        
        <div class="message">
            Oii Thiagoooo, tudo bom???
        </div>

        <div class="message">
            Espero que simm, ta chegando finalmente o último dia do enem que também é um dos dias mais legais as vezes ou mais chatos kkkkkkk, mas não fica ansioso nem nervoso, você estudou o ano todo e também se dedicou MUITO, vc é uma pessoa incrível e muito inteligente, ou seja <span class="highlight">vai tirar de letra esse dia</span>.
        </div>

        <div class="message">
            Vai dar tudo certooooo, sempre confiante, faça uma boa prova viuu, <span class="highlight">Gosto muito de tiii</span> 🫶🫶🫶
        </div>


    </div>
</body>
</html>
