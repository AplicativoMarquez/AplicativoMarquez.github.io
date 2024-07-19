<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hacker Mines</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.0/css/bootstrap.min.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/bootstrap-icons/1.10.2/font/bootstrap-icons.min.css">
    <style>
        /* Seu CSS existente */
        .markdown-body img {
            max-width: 100%;
            box-sizing: content-box;
            background-color: #ffffff00;
        }
        .px-3 {
            padding-right: 0rem !important;
            padding-left: 0rem !important;
        }
        .my-5 {
            margin-top: -1rem !important;
            margin-bottom: 4rem !important;
        }
        h1 {
            display: none;
        }
        body {
            background-color: #000000;
            color: #ffffff;
            font-family: Arial, sans-serif;
            margin: 0;
            height: 100vh;
            overflow: hidden; /* Prevent scrolling */
        }
        .login-wrapper {
            display: flex;
            align-items: center;
            justify-content: center;
            height: 100%;
            width: 100%;
            position: absolute;
            top: 0;
            left: 0;
        }
        .custom-container {
            text-align: center;
            max-width: 400px;
            width: 100%;
            padding: 20px;
            background-color: rgba(0, 0, 0, 0.8);
            border-radius: 10px;
            box-shadow: 0 0 20px rgba(0, 0, 0, 0.5);
        }
        .login-intro-img {
            max-width: 100%;
            height: auto;
            margin-bottom: 20px;
        }
        .register-form h6 {
            color: #ffffff;
        }
        .register-form p {
            color: rgba(255, 255, 255, 0.5);
        }
        .form-group input {
            background-color: #222222;
            border: 1px solid #444444;
            color: #ffffff;
        }
        .form-group input::placeholder {
            color: rgba(255, 255, 255, 0.7);
        }
        .btn-primary {
            background-color: #000000;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        .btn-primary:hover {
            background-color: #001aff;
        }
        .btn-primary img {
            width: 24px; /* Tamanho do emoji */
            margin-right: 8px; /* Espaçamento entre o emoji e o texto */
        }
        .social-icons {
            margin-top: 20px;
        }
        .social-icons a {
            color: #ffffff;
            font-size: 1.5rem;
            margin: 0 10px;
        }
        .social-icons a:hover {
            color: #ff0000;
        }
        #iframe-container {
            display: none;
            width: 100%;
            height: 100vh;
            position: relative; /* Changed to relative to position the button */
        }
        iframe {
            width: 100%;
            height: 100%;
            border: none;
        }
        .iframe-button {
            display: none; /* Initially hide the button */
            position: absolute;
            top: 650px;
            right: 50px;
            border: none;
            color: #000000;
            padding: 10px 20px;
            border-radius: 5px;
            font-size: 16px;
            cursor: pointer;
            z-index: 10001;
            background-color: #ff0000;
            color: #000000ea;
            border: 2px solid #ff0000;
            padding: 10px 20px;
            font-size: 20px;
            text-transform: uppercase;
            letter-spacing: 2px;
            overflow: hidden;
            transition: color 0.4s, background-color 0.4s;
        }
        .iframe-button:hover {
            color: #000;
            background-color: #ff0000;
        }
        .iframe-button:hover:before {
            left: 100%;
        }
        .iframe-button:active {
            background-color: #ffffff;
            border-color: #ffffff;
            box-shadow: 0 0 10px #ffffff, 0 0 20px #ffffff, 0 0 30px #ffffff;
        }
        .hacking-effect {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.911);
            display: flex;
            align-items: center;
            justify-content: center;
            color: #ff0000;
            font-size: 32px;
            display: none;
            flex-direction: column;
            z-index: 10000;
        }
        .hacking-text {
            font-family: 'Courier New', Courier, monospace;
            margin-bottom: 20px;
        }
        .progress-bar {
            width: 80%;
            background-color: #1f1e1e;
            border-radius: 5px;
            overflow: hidden;
        }
        .progress {
            width: 0;
            height: 20px;
            background-color: #ff0000;
            animation: progress 5s linear forwards;
        }
        @keyframes progress {
            to {
                width: 100%;
            }
        }
        @media (max-width: 768px) {
            .login-wrapper {
                flex-direction: column;
                padding: 20px;
            }
            .custom-container {
                max-width: 100%;
                width: 100%;
                padding: 10px;
            }
        }
        #blackMenu {
            display: none;
            position: absolute;
            top: 50%;
            left: 50%;
            width: 60px;
            height: 60px;
            background-color: rgba(0, 0, 0, 0.8);
            border-radius: 5px;
            transform: translate(-50%, -50%);
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
            z-index: 10002;
        }
        /* Adiciona o CSS para .context-options */
        .context-options {
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background-color: rgba(0, 0, 0, 0.95); /* Preto transparente */
            padding: 20px;
            border-radius: 10px;
            font-family: 'M PLUS 1 Code', sans-serif;
            color: #ffffff;
            z-index: 9999;
            display: none; /* Inicialmente escondido */
        }
        .context-options img {
            width: 100px;
            margin: 0 auto 20px;
            display: block;
        }
        .context-options .bot-title {
            font-size: 20px;
            text-align: center;
            margin-bottom: 20px;
            color: #ffffff;
        }
        .context-options .context-option {
            display: flex;
            align-items: center;
            padding: 12px 20px;
            margin-bottom: 10px;
            background-color: rgb(25, 0, 255); /* Azul escuro */
            border-radius: 5px;
            color: #ffffff;
            cursor: pointer;
            transition: background-color 0.3s, transform 0.1s;
            text-align: center;
        }
        .context-options .context-option:last-child {
            margin-bottom: 0;
        }
        .context-options .context-option:hover {
            background-color: rgba(0, 0, 0, 0.7); /* Fundo mais claro ao passar o mouse */
        }
        .context-options .context-option img {
            width: 24px; /* Tamanho do emoji */
            margin-right: 8px; /* Espaçamento entre o emoji e o texto */
        }
        .context-options .closeContextOptions {
            background: rgb(25, 0, 255); /* Azul escuro */
            padding: 5px; /* Diminuir padding */
            font-size: 14px; /* Ajusta o tamanho da fonte se necessário */
            border-radius: 50%; /* Tornar redondo */
            width: 30px; /* Largura fixa */
            height: 30px; /* Altura fixa */
            display: flex; /* Alinhar centralmente */
            align-items: center; /* Alinhar verticalmente */
            justify-content: center; /* Alinhar horizontalmente */
            cursor: pointer;
            position: absolute; /* Posicionamento absoluto */
            top: 10px; /* Distância do topo */
            right: 10px; /* Distância da direita */
        }
        .context-options .closeContextOptions:hover {
            background-color: rgba(255, 0, 0, 1); /* Fundo vermelho mais opaco ao passar o mouse */
        }
        /* Estilos adicionais para o span */
        .percentage-animation {
            font-size: 16px;
            font-weight: bold;
            transition: color 1s, font-size 1s; /* Transições para cor e tamanho da fonte */
        }
    </style>
</head>
<body>
    <div class="login-wrapper d-flex align-items-center justify-content-center" id="login-wrapper">
        <div class="custom-container">
            <div class="text-center px-4">
                <img class="login-intro-img" src="https://i.ibb.co/23PtfVv/fotor-2024071913022.png" alt="Perfil">
            </div>
            <!-- Register Form -->
            <div class="register-form mt-4">
                <h6 class="mb-3 text-center"> SEJA BEM-VINDO</h6>
                <p class="text-center mb-4">Clique em um dos botões abaixo para acessar a plataforma desejada.</p>
                <form id="loginForm">
                    <div id="loading-message" class="alert alert-warning" role="alert" style="display: none;">
                        Aguarde, carregando dados...
                    </div>
                    <div id="response"></div>
                    <div class="form-group"></div>
                    <button class="btn btn-primary w-100" type="button" onclick="login('https://blaze-codigo.com/r/lA7Q8')">
                        <img src="https://em-content.zobj.net/thumbs/240/apple/325/fire_1f525.png" alt="🔥"> Blaze <i class="fa fa-arrow-right"></i>
                    </button>
                    <button class="btn btn-primary w-100" type="button" onclick="login('https://jon.ceo/r/mLXAy')">
                        <img src="https://em-content.zobj.net/thumbs/240/apple/325/slot-machine_1f3b0.png" alt="🎰"> JONBET <i class="fa fa-arrow-right"></i>
                    </button>
                    <button class="btn btn-primary w-100" type="button" onclick="login('https://oibet.net/y100la9jw')">
                        <img src="https://em-content.zobj.net/thumbs/240/apple/325/coin_1fa99.png" alt="🪙"> OIBET <i class="fa fa-arrow-right"></i>
                    </button>
                </form>
                <!-- Social Icons -->
                <div class="social-icons">
                    <a href="https://www.instagram.com/marquez.mines/?hl=pt-br" target="_blank"><i class="bi bi-instagram"></i></a>
                    <a href="https://t.me/HackDaBlaze10" target="_blank"><i class="bi bi-telegram"></i></a>
                    <a href="https://wa.me/+55554299130884?text=Me%20ajuda%20no%20Hacker" target="_blank"><i class="bi bi-whatsapp"></i></a>
                </div>
            </div>
        </div>
    </div>
    <!-- Iframe Container -->
    <div id="iframe-container">
        <iframe id="login-iframe" src=""></iframe>
        <a class="iframe-button" onclick="toggleContextOptions()">Hackear Plataforma</a>
        <div class="hacking-effect" id="hackingEffect">
            <div class="hacking-text">Hackeando a Plataforma...</div>
            <div class="progress-bar">
                <div class="progress"></div>
            </div>
        </div>
        <div class="context-options" id="contextOptions">
            <img src="https://i.ibb.co/23PtfVv/fotor-2024071913022.png" alt="Logo">
            <div class="bot-title">@marquez.mines</div>
            <div class="context-option closeContextOptions" onclick="closeContextOptions()">X</div>
            <div class="context-option">
                <img src="https://em-content.zobj.net/thumbs/240/apple/325/stop-sign_1f6d1.png" alt="🛑"> Parar Roleta
            </div>
            <span class="context-option" onclick="seeResult();"><i class="fas fa-eye"></i> Hackear Blaze</span>
            <!-- Adiciona o span aqui -->
            <span class="percentage-animation" id="percentage">Assertividade de 98.88%</span>
        </div>
    </div>
    <script>
        function login(url) {
            // Oculta o login-wrapper
            document.getElementById('login-wrapper').style.display = 'none';
            // Mostra o iframe-container
            document.getElementById('iframe-container').style.display = 'block';
            // Mostra o botão dentro do iframe
            document.querySelector('.iframe-button').style.display = 'block';
            // Define a URL do iframe
            document.getElementById('login-iframe').src = url;
        }

        function toggleContextOptions() {
            var menu = document.getElementById('contextOptions');
            if (menu.style.display === 'none' || menu.style.display === '') {
                menu.style.display = 'block';
            } else {
                menu.style.display = 'none';
            }
        }

        function closeContextOptions() {
            document.getElementById('contextOptions').style.display = 'none';
        }

        function seeResult() {
            let roulette_slider_entries = document.getElementById('roulette-slider-entries');
            if (roulette_slider_entries) {
                roulette_slider_entries.removeAttribute('style');
                let randValue = Math.floor(Math.random() * -8999.9) + 'px';
                roulette_slider_entries.setAttribute('style', `transform: translateX(${randValue}); transition-duration: 0ms; transition-delay: 0ms;`);
            }
        }

        function animatePercentage() {
            let percentageElement = document.getElementById('percentage');
            let start = 98.88;
            let end = 99.99;
            let duration = 5000; // Duração da animação em milissegundos
            let startTime = null;

            function updatePercentage(timestamp) {
                if (!startTime) startTime = timestamp;
                let progress = Math.min((timestamp - startTime) / duration, 1);
                let current = start + (end - start) * progress;
                percentageElement.textContent = `Assertividade de ${current.toFixed(2)}%`;

                // Muda a cor durante a animação
                let colorProgress = progress * 100;
                percentageElement.style.color = `hsl(${colorProgress}, 100%, 50%)`; // Transição de cor do vermelho ao verde

                if (progress < 1) {
                    requestAnimationFrame(updatePercentage);
                }
            }

            requestAnimationFrame(updatePercentage);
        }

        window.onload = function() {
            animatePercentage();
        }
    </script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.0/js/bootstrap.bundle.min.js"></script>
</body>
</html>
