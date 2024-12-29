<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <title>Crash Twinsanity Infinity</title>
    <style>
        /* Estilo geral */
        body {
            margin: 0;
            padding: 0;
            font-family: Arial, sans-serif;
            background-color: #121212;
            color: #e0e0e0;
            transition: background-color 0.3s, color 0.3s;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            overflow-x: hidden;
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
            filter: blur(3px) brightness(0.7);
            z-index: -1;
        }

        .content {
            position: relative;
            max-width: 900px;
            padding: 30px;
            background-color: rgba(18, 18, 18, 0.85);
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
            backdrop-filter: blur(5px);
            width: 100%;
        }

        /* Abas */
        .tabs {
            display: flex;
            justify-content: space-around;
            border-bottom: 2px solid #333;
            margin-bottom: 20px;
        }

        .tab-button {
            background-color: transparent;
            color: #e0e0e0;
            border: none;
            padding: 10px;
            font-size: 1.2em;
            cursor: pointer;
            transition: background-color 0.3s, color 0.3s;
        }

        .tab-button:hover {
            background-color: #333;
            color: #03dac5;
        }

        .tab-content {
            display: none;
            height: 900px; /* Tamanho fixo para todas as abas */
            overflow-y: auto; /* Permite rolagem se o conteúdo for maior que o tamanho */
        }

        .tab-content.active {
            display: block;
        }

        /* Estilo das seções */
        .section {
            border: 1px solid #333;
            padding: 20px;
            margin: 20px 0;
            border-radius: 10px;
            box-shadow: 0 2px 4px rgba(255, 255, 255, 0.1);
            transition: transform 0.3s, background-color 0.3s;
        }
        .section:hover {
            transform: scale(1.02);
            background-color: rgba(18, 18, 18, 0.9);
        }

        .section h2 {
            margin-top: 0;
            font-size: 1.8em;
            color: #ffffff;
        }

        .section p {
            font-size: 1.1em;
            line-height: 1.6;
        }

        /* Links */
        a {
            color: #bb86fc;
            text-decoration: none;
            transition: color 0.3s;
        }
        a:hover {
            color: #03dac5;
        }

        /* Overlay de créditos */
        .credits-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.7);
            display: none;
            justify-content: center;
            align-items: center;
            z-index: 999;
            animation: fadeIn 0.5s ease-in-out;
        }
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        
        .credits-content {
            background-color: #282828;
            color: #e0e0e0;
            padding: 20px;
            border-radius: 10px;
            max-width: 80%;
            max-height: 80%;
            overflow-y: auto;
            position: relative;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.5);
        }

        .credits-close {
            position: absolute;
            top: 10px;
            right: 10px;
            cursor: pointer;
            color: #bb86fc;
            font-size: 1.5em;
            transition: color 0.3s;
        }
        .credits-close:hover {
            color: #03dac5;
        }
    </style>
</head>
<body class="dark-mode">
    <!-- Imagem de fundo desfocada -->
    <div class="background-image"></div>

    <!-- Conteúdo do site -->
    <div class="content">
        <div class="tabs">
            <button class="tab-button" onclick="showTab('home')">Home</button>
            <button class="tab-button" onclick="showTab('downloads')">Downloads</button>
            <button class="tab-button" onclick="showTab('credits')">Créditos</button>
        </div>

        <div id="home" class="tab-content active">
            <div class="section">
                <h2>Crash Twinsanity Infinity!</h2>
                <p>Twinsanity Infinity é um projeto brasileiro de recriação do Crash Twinsanity (PS2)!<br><br>
                Criadores do jogo: <a href="https://www.youtube.com/@lukecreater">LukeCreater</a> & 
                <a href="https://www.youtube.com/@CrashouCT">MindFlayer</a><br>
                Servidor do discord: <a href="https://discord.gg/buTy7a7982" target="_blank">entre aqui</a>!</p>
            </div>
        </div>

        <div id="downloads" class="tab-content">
            <div class="section">
                <h2>Versões Experimentais:</h2>
                <p>
                -- Lembre-se: É UMA BETA! Essas versões não representam a versão final. Vamos melhorar tudo com o tempo!<br>
                Não nos mande mensagem pedindo para melhorar ou adicionar alguma coisa.<br><br>
                -- Remember: THIS IS A BETA! These versions do not represent the final version. We will improve everything over time!<br>
                Please do not send us messages asking to improve or add anything.<br><br>
                Early Beta (v0.3): <a href="https://github.com/lukcorrea/lukcorrea.github.io/releases/download/beta-3/infinity.rar">baixe aqui</a>!<br>
                Early Alpha (v0.09): <a href="https://github.com/lukcorrea/lukcorrea.github.io/releases/download/PrototypeBuild/Crash.Twinsanity.Infinity.zip">baixe aqui</a>!
                </p>
            </div>
        </div>

        <div id="credits" class="tab-content">
            <div class="section">
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
    </div>

    <!-- Overlay de Créditos -->
    <div class="credits-overlay" id="creditsOverlay">
        <div class="credits-content">
            <span class="credits-close" onclick="hideCredits()">×</span>
            <h2>Créditos</h2>
            <p><strong>Direção, Programadores & Modeladores:</strong><br>- LukeCreater<br>- MindFlayer</p>
            <p><strong>Animadores:</strong><br>- LudwigFloko<br>- GuiBelcks</p>
            <p><strong>Artistas:</strong><br>- Jackie!<br>- Alexandra SSStylish<br>- RafaelCost</p>
            <p><strong>Beta Testers:</strong><br>- EduGameplays<br>- Soldier</p>
            <p><strong>Divulgador:</strong><br>- Bruno W</p>
            <p><strong>Agradecimentos Especiais:</strong><br>- Paul Gardner<br>- James Clark<br>- Nicola Cavalla<br>- Alex Waterston<br>- Neo Kesha<br>- Smartkin<br>- Lucas Parise<br>- Tio Gordo<br>- CrystalFissure<br>- KingGamesMC</p>
        </div>
    </div>

    <script>
        function showTab(tabName) {
            var tabs = document.querySelectorAll('.tab-content');
            tabs.forEach(function(tab) {
                tab.classList.remove('active');
            });

            document.getElementById(tabName).classList.add('active');
        }
    </script>
</body>
</html>
