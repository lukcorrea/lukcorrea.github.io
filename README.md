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
            filter: blur(1px);
            z-index: -1;
        }

        .content {
            position: relative;
            z-index: 1;
            padding: 20px;
            display: flex; /* Organiza o layout em colunas */
        }

        .section {
            border: 1px solid #333;
            padding: 20px;
            margin: 20px 0;
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(255, 255, 255, 0.1);
            background-color: rgba(18, 18, 18, 0.8);
            width: 70%; /* Define a largura do conteúdo de texto */
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

        .gallery {
            display: flex;
            flex-direction: column;
            width: 30%; /* Define a largura da galeria de imagens */
            margin-left: 20px;
        }

        .gallery img {
            width: 100%;
            height: auto;
            margin-bottom: 10px;
            cursor: pointer;
            border-radius: 8px;
        }

        .gallery img:hover {
            filter: brightness(0.8);
        }

        .image-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.9);
            display: none;
            justify-content: center;
            align-items: center;
            z-index: 1000;
        }

        .image-overlay img {
            max-width: 90%;
            max-height: 90%;
            border-radius: 8px;
        }

        .close-button {
            position: absolute;
            top: 20px;
            right: 20px;
            font-size: 24px;
            color: white;
            cursor: pointer;
            background: transparent;
            border: none;
        }
    </style>
</head>
<body class="dark-mode">
    <!-- Imagem de fundo desfocada -->
    <div class="background-image"></div>

    <!-- Conteúdo do site com layout em colunas -->
    <div class="content">
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

        <!-- Galeria de Imagens -->
        <div class="gallery">
            <img src="https://via.placeholder.com/150" alt="Imagem 1" onclick="openOverlay(this)">
            <img src="https://via.placeholder.com/150" alt="Imagem 2" onclick="openOverlay(this)">
            <img src="https://via.placeholder.com/150" alt="Imagem 3" onclick="openOverlay(this)">
        </div>
    </div>

    <!-- Overlay de Imagem Grande -->
    <div class="image-overlay" id="imageOverlay">
        <img id="overlayImage" src="" alt="Imagem Grande">
        <button class="close-button" onclick="closeOverlay()">X</button>
    </div>

    <script>
        // Função para abrir o overlay de imagem
        function openOverlay(image) {
            var overlay = document.getElementById('imageOverlay');
            var overlayImage = document.getElementById('overlayImage');
            overlayImage.src = image.src;
            overlay.style.display = 'flex';
        }

        // Função para fechar o overlay de imagem
        function closeOverlay() {
            var overlay = document.getElementById('imageOverlay');
            overlay.style.display = 'none';
        }
    </
