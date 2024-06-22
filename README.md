<html lang="pt">
<head>
    <meta charset="UTF-8">
    <title>Crash Twinsanity Infinity - Updates</title>
    <style>
        body {
            background-color: white;
            color: black;
            transition: background-color 0.3s, color 0.3s;
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
        /* Dark mode styles */
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
        .toggle-button {
            position: fixed;
            top: 10px;
            right: 10px;
            padding: 10px 20px;
            background-color: #6200ee;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <button class="toggle-button" onclick="toggleDarkMode()">Modo Escuro</button>
    <div class="section">
        <h2>Lançamento 18-07-2024</h2>
        <p>Você pode baixar a demo <a href="https://www.google.com.br">clicando aqui</a>.</p>
        <h2>Instalação:</h2>
        <p>1) Extraia o arquivo .rar em qualquer lugar do seu computador.</p>
        <p>2) Abra o arquivo <span style="color: blue;">Crash Twinsanity Infinity.exe</span> e divirta-se!</p>
        <h2>Controles:</h2>
        <p>Como essa é uma versão em desenvolvimento, não é possível alterar os controles ainda.<br>
        Por enquanto, o jogo está programado para esses botões:</p>
        W A S D = Movimento<br>
        Espaço = Pular / Pular Cena <br>
        Shift / Botão Direito do Mouse = Deslizar (Dash) / Barrigada<br>
        Esc = Menu de Pausa<br>
        E = Menu de Itens<br>
    </div>
    <script>
        function toggleDarkMode() {
            document.body.classList.toggle('dark-mode');
        }
    </script>
</body>
</html>
