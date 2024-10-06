<html lang="pt">
<head>
    <meta charset="UTF-8">
    <title>Crash Twinsanity Infinity</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            font-family: Arial, sans-serif;
            background-color: #121212;
            transform: scale(1.25);
            color: #e0e0e0;
            transition: background-color 0.3s, color 0.3s;
        }

        .background-image {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: url('https://i.imgur.com/eNsHAwQ.png');
            background-size: cover;
            background-position: center;
            filter: blur(5px);
            z-index: -1;
        }

        .content {
            position: relative;
            z-index: 1;
            padding: 20px;
        }

        .section {
            border: 1px solid #333;
            padding: 20px;
            margin: 20px 0;
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(255, 255, 255, 0.1);
            background-color: rgba(18, 18, 18, 0.8);
        }

        .section h2 {
            margin-top: 0;
            font-size: 1.8em;
            text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.4);
            color: #ffffff;
        }

        .section p {
            font-size: 1.1em;
            line-height: 1.6;
            text-shadow: 0.5px 0.5px 2px rgba(0, 0, 0, 0.1);
        }

        a {
            color: #bb86fc;
        }

        .credits-button, .translate-button {
            position: fixed;
            top: 10px;
            padding: 10px 20px;
            background-color: #6200ee;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            z-index: 1000;
        }

        .credits-button {
            right: 10px;
        }

        .translate-button {
            right: 120px;
        }

        .credits-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.5);
            display: none;
            justify-content: center;
            align-items: center;
            z-index: 999;
        }

        .credits-content {
            background-color: white;
            padding: 20px;
            border-radius: 8px;
            max-width: 80%;
            max-height: 80%;
            overflow-y: auto;
            position: relative;
        }

        .credits-close {
            position: absolute;
            top: 10px;
            right: 10px;
            cursor: pointer;
        }
    </style>
</head>
<body class="dark-mode">
    <!-- Imagem de fundo desfocada -->
    <div class="background-image"></div>

    <!-- Conteúdo do site -->
    <div class="content">
        <button class="credits-button" onclick="showCredits()">Créditos</button>
        <button class="translate-button" onclick="translatePage()">Traduzir para Inglês</button>

        <div class="section">
            <h2>Crash Twinsanity Infinity!</h2>
            <p>Twinsanity Infinity é um projeto brasileiro de recriação do Crash Twinsanity (PS2)!<br><br>
            Criadores do jogo: <a href="https://www.youtube.com/@lukecreater">LukeCreater</a> & 
            <a href="https://www.youtube.com/@CrashouCT">MindFlayer</a><br>
            Servidor do discord: <a href="https://discord.gg/buTy7a7982" target="_blank">entre aqui</a>!</p>
            
            <h2>Versões</h2>
            <p>
            Early Beta (v0.3): <a href="https://github.com/lukcorrea/lukcorrea.github.io/releases/download/beta-3/infinity.rar">baixe aqui</a>!<br>
            Alpha Experimental (v0.09): <a href="https://github.com/lukcorrea/lukcorrea.github.io/releases/download/PrototypeBuild/Crash.Twinsanity.Infinity.zip">baixe aqui</a>!
            </p>
            <h2>Instalação:</h2>
            <p>1) Extraia o arquivo .rar em qualquer lugar do seu computador.</p>
            <p>2) Abra o arquivo <span style="color: aqua;">Twinfinity.exe</span> e divirta-se!</p>

            <h2>Controles:</h2>
            <p>W A S D = Movimento<br>
            Espaço = Pular / Pular Cena<br>
            Shift / Botão Direito do Mouse = Deslizar (Dash) / Barrigada<br>
            Esc = Menu de Pausa<br>
            I = Menu de Itens<br>
            1, 2, 3, 4 = Checkpoint Teleport!</p>
        </div>
    </div>

    <!-- Overlay de Créditos -->
    <div class="credits-overlay" id="creditsOverlay">
        <div class="credits-content">
            <span class="credits-close" onclick="hideCredits()">X</span>
            <h2>Créditos</h2>
            <p><strong>Direção, Programadores & Modeladores:</strong><br>
            - LukeCreater<br>
            - MindFlayer</p>
            <p><strong>Animadores:</strong><br>
            - LudwigFloko<br>
            - GuiBelcks</p>
            <p><strong>Artistas:</strong><br>
            - Jackie!<br>
            - Alexandra SSStylish<br>
            - RafaelCost</p>
            <p><strong>Beta Testers:</strong><br>
            - EduGameplays<br>
            - Soldier</p>
            <p><strong>Divulgador:</strong><br>
            - Bruno W</p>
            <p><strong>Agradecimentos Especiais:</strong><br>
            - Paul Gardner<br>
            - James Clark<br>
            - Nicola Cavalla<br>
            - Alex Waterston<br>
            - Neo Kesha<br>
            - Smartkin<br>
            - Lucas Parise<br>
            - Tio Gordo<br>
            - CrystalFissure<br>
            - KingGamesMC</p>
        </div>
    </div>

    <script>
        function showCredits() {
            var creditsOverlay = document.getElementById('creditsOverlay');
            creditsOverlay.style.display = 'flex';
        }

        function hideCredits() {
            var creditsOverlay = document.getElementById('creditsOverlay');
            creditsOverlay.style.display = 'none';
        }

        function translatePage() {
            window.location.href = "https://translate.google.com/translate?hl=en&sl=pt&u=" + encodeURIComponent(window.location.href);
        }
    </script>
</body>
</html>
