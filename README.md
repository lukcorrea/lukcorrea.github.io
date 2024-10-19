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
            color: #e0e0e0;
        }

        /* Estilo das imagens do projeto */
        .gallery {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 20px;
        }

        .gallery img {
            width: 150px;
            height: 150px;
            object-fit: cover;
            cursor: pointer;
            transition: transform 0.3s;
        }

        .gallery img:hover {
            transform: scale(1.05);
        }

        /* Estilo da tela de visualização */
        .overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.8);
            display: none;
            justify-content: center;
            align-items: center;
            z-index: 1000;
        }

        .overlay img {
            max-width: 90%;
            max-height: 90%;
            border-radius: 8px;
        }

        .close-btn {
            position: absolute;
            top: 20px;
            right: 20px;
            background-color: transparent;
            color: white;
            font-size: 24px;
            border: none;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <!-- Seção de Imagens do Projeto -->
    <div class="section">
        <h2>Imagens do Projeto:</h2>
        <div class="gallery">
            <img src="imagem1.jpg" alt="Imagem 1" onclick="openOverlay(this)">
            <img src="imagem2.jpg" alt="Imagem 2" onclick="openOverlay(this)">
            <img src="imagem3.jpg" alt="Imagem 3" onclick="openOverlay(this)">
            <img src="imagem4.jpg" alt="Imagem 4" onclick="openOverlay(this)">
        </div>
    </div>

    <!-- Overlay de visualização de imagens -->
    <div class="overlay" id="imageOverlay">
        <button class="close-btn" onclick="closeOverlay()">X</button>
        <img id="overlayImage" src="" alt="Imagem Ampliada">
    </div>

    <script>
        function openOverlay(image) {
            var overlay = document.getElementById('imageOverlay');
            var overlayImage = document.getElementById('overlayImage');
            overlayImage.src = image.src;
            overlay.style.display = 'flex';
        }

        function closeOverlay() {
            var overlay = document.getElementById('imageOverlay');
            overlay.style.display = 'none';
        }
    </script>
</body>
</html>
