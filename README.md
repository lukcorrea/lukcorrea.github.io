<html lang="pt">
<head>
    <meta charset="UTF-8">
    <title>Crash Twinsanity Infinity</title>
    <style>
        body {
            background-color: white;
            color: black;
            transition: background-color 0.3s, color 0.3s;
            font-family: Arial, sans-serif;
        }
        .section {
            border: 1px solid #ccc;
            padding: 20px;
            margin: 20px 0;
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }
        .section h2 {
            margin-top: 0;
        }
        body.dark-mode {
            background-color: #121212;
            color: #e0e0e0;
        }
        body.dark-mode .section {
            border: 1px solid #333;
            box-shadow: 0 2px 4px rgba(255,255,255,0.1);
        }
        body.dark-mode a {
            color: #bb86fc;
        }
        .toggle-button, .credits-button {
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
        .toggle-button {
            right: 10px;
        }
        .credits-button {
            right: 150px;
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
<body>
    <button class="toggle-button" onclick="toggleDarkMode()">Modo Escuro</button>
    <button class="credits-button" onclick="showCredits()">Créditos</button>
    <div class="section">
        <h2>Lançamento da Beta Experimental!</h2>
        <p>Você pode baixar a demo <a href="http://github.com/lukcorrea/lukcorrea.github.io/releases/download/Prerelease/infinity.rar">clicando aqui!</a>.<br>
        Essa versão tem bastante bug! Nós vamos lançar uma versão estável daqui a alguns dias, fique atento!<br>
        <br>
        Criadores do jogo: LukeCreater & MindFlayer<br>
        Server do discord: <a href="https://discord.gg/buTy7a7982" target="_blank">Discord Server</a>
        </p>
        <h2>Instalação:</h2>
        <p>1) Extraia o arquivo .rar em qualquer lugar do seu computador.</p>
        <p>2) Abra o arquivo <span style="color: blue;">Twinfinity.exe</span> e divirta-se!</p>
        <h2>Controles:</h2>
        <p>Como essa é uma versão em desenvolvimento, não é possível alterar os controles ainda.<br>
        Por enquanto, o jogo está programado para esses botões:</p>
        W A S D = Movimento<br>
        Espaço = Pular / Pular Cena <br>
        Shift / Botão Direito do Mouse = Deslizar (Dash) / Barrigada<br>
        Esc = Menu de Pausa<br>
        I = Menu de Itens<br>
        1, 2, 3, 4 = Checkpoint Teleport!
    </div>

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
        function toggleDarkMode() {
            var body = document.body;
            body.classList.toggle('dark-mode');
            var modeButton = document.querySelector('.toggle-button');
            if (body.classList.contains('dark-mode')) {
                modeButton.textContent = 'Modo Claro';
            } else {
                modeButton.textContent = 'Modo Escuro';
            }
        }

        function showCredits() {
            var creditsOverlay = document.getElementById('creditsOverlay');
            creditsOverlay.style.display = 'flex';
        }

        function hideCredits() {
            var creditsOverlay = document.getElementById('creditsOverlay');
            creditsOverlay.style.display = 'none';
        }
    </script>
</body>
</html>
