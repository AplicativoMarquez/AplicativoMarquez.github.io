<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hacker Mines</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.0/css/bootstrap.min.css">
    <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Sofia+Pro:wght@600&display=swap">

    <style>

    


.ander-button {
    position: absolute;
    bottom: 20px;
    left: 50%;
    transform: translateX(-50%);
    background-color: #ffffff; /* Cor de fundo do botão */
    color: #000000; /* Cor do texto do botão */
    border: none;
    padding: 10px 20px;
    border-radius: 5px;
    font-size: 16px;
    cursor: pointer;
    transition: background-color 0.3s, color 0.3s;
}

.ander-button:hover {
    background-color: #ff0000; /* Cor de fundo do botão ao passar o mouse */
    color: #ffffff; /* Cor do texto do botão ao passar o mouse */
}

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
        .btn-primary1 {
            background-color: #000000;
            display: flex;
            border-color: #ffffff;
            align-items: center;
            justify-content: center;
        }
        .btn-primary2 {
            background-color: #000000;
            display: flex;
            border-color: #ffffff;
            align-items: center;
            justify-content: center;
        }

        .btn-primary1:hover {
            background-color: #ff0000;
        }
        .btn-primary2:hover {
            background-color: #15ff00;
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
            top: 10px; /* Adjusted position */
            right: 10px; /* Adjusted position */
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
            padding: 26px;
            border-radius: 10px;
            font-family: 'SofiaPro-SemiBold';
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
        .context-options .context-option1 {
            display: flex;
            align-items: center;
            padding: 1px 20px;
            margin-bottom: 10px;
            background-color: rgb(25, 0, 255); /* Azul escuro */
            border-radius: 0px;
            color: #ffffff;
            cursor: pointer;
            transition: background-color 0.3s, transform 0.1s;
            text-align: center;
        }

        .context-options .context-option2 {
            display: flex;
            align-items: center;
            padding: 1px 20px;
            margin-bottom: 10px;
            background-color: rgb(255, 0, 0); /* Azul escuro */
            border-radius: 0px;
            color: #ffffff;
            cursor: pointer;
            transition: background-color 0.3s, transform 0.1s;
            text-align: center;
        }
        .context-options .context-option3 {
            display: flex;
            align-items: center;
            padding: 1px 20px;
            margin-bottom: 6px;
            background-color: rgb(25, 0, 255); /* Azul escuro */
            border-radius: 10px;
            color: #ffffff;
            cursor: pointer;
            transition: background-color 0.3s, transform 0.1s;
            text-align: center;
        }
        .context-options .context-option:last-child {
            margin-bottom: 0;
        }
        .context-options .context-option1:hover {
            background-color: rgba(0, 0, 0, 0.7); /* Fundo mais claro ao passar o mouse */
        }
        .context-options .context-option2:hover {
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
            line-height: 30px; /* Centralizar verticalmente */
            text-align: center; /* Centralizar horizontalmente */
            position: absolute; /* Posição absoluta */
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
        /* Estilos para o quadrado preto */
        .black-square {
    position: absolute;
    width: 600px;
    height: 664px;
    background-color: #00000079;
    display: none;
    z-index: 10002; /* Garante que o quadrado preto esteja na frente de tudo */
    top: 54%;
    left: 65%;
    transform: translate(-50%, -50%);
}
.loading-animation {
    width: 40px;
    height: 40px;
    margin: auto;
    border: 4px solid rgba(0, 255, 0, 0.2);
    border-radius: 50%;
    border-top-color: #00ff00;
    animation: spin 1s ease-in-out infinite;
}

@keyframes spin {
    0% {
        transform: rotate(0deg);
    }
    100% {
        transform: rotate(360deg);
    }
}


        .white-square {
    position: absolute;
    width: 100px; /* Largura dos quadrados */
    height: 100px; /* Altura dos quadrados */
    background-color: #ffffff; /* Cor de fundo branca */
    border: 1px solid #000000; /* Borda preta de 1px */
    display: flex; /* Usar flexbox para centralizar conteúdo */
    justify-content: center; /* Centralizar horizontalmente */
    align-items: center; /* Centralizar verticalmente */
}

.white-square img {
    max-width: 100%; /* Imagem dentro do quadrado ocupando todo o espaço disponível */
    max-height: 100%; /* Imagem dentro do quadrado ocupando todo o espaço disponível */
}
.percentage-animation {
    color: #00ff00; /* Cor verde */
    font-size: 16px;
    font-weight: bold;
    margin-top: 10px; /* Espaço entre a imagem e o texto */
}

.img.svg {
    width: 100px


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
                    <button class="btn btn-primary1 w-100" type="button" onclick="login('https://blaze-codigo.com/r/lA7Q8')">
                        <img src="https://i.ibb.co/xM8T2fd/logo-blaze-apostas-online-QQmdxz-removebg-preview.png" > <i class="fa fa-arrow-right"></i>
                    </button>
                    <button class="btn btn-primary2 w-100" type="button" onclick="login('https://jon.ceo/r/mLXAy')">
                        <img src="https://i.ibb.co/Tct020B/jonbet-logo-removebg-preview.png" >  <i class="fa fa-arrow-right"></i>
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
            <div class="bot-title">@Marquez.Mines</div>
            <div class="context-option1" onclick="closeContextOptions()">💎Hackear Mines💎</div>
        
            <div class="context-option2">🔥Hackear Double🔥</div>
            
           
            <!-- Adiciona o span aqui -->
            
        </div>
        <!-- Quadrado preto -->
        <div class="black-square" id="blackSquare">
            
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
        var image1Url = 'https://i.ibb.co/mtkmH1g/Captura-de-tela-2024-07-24-181926.png';
        var image2Url = 'https://i.ibb.co/PCB9HhV/Captura-de-tela-2024-07-24-181711.png';
        

        function closeContextOptions() {
    var loadingElement = document.createElement('div');
    loadingElement.className = 'loading-animation';

    var contextOptions = document.getElementById('contextOptions');
    contextOptions.appendChild(loadingElement);

    setTimeout(function() {
        contextOptions.removeChild(loadingElement);

        var newImage = document.createElement('img');
        var randomImageIndex = Math.random() < 0.5 ? 1 : 2;
        newImage.src = randomImageIndex === 1 ? image1Url : image2Url;
        newImage.alt = 'Nova Imagem';
        newImage.style.width = '50px';
        newImage.style.margin = '0 auto 20px';
        newImage.style.display = 'block';

        contextOptions.appendChild(newImage);

        // Criar o elemento span para a Assertividade
        var percentageSpan = document.createElement('span');
        percentageSpan.className = 'percentage-animation';
        var randomPercentage = (Math.random() * (99.99 - 98.88) + 98.88).toFixed(2);
        percentageSpan.textContent = 'Assertividade de ' + randomPercentage + '%';
        contextOptions.appendChild(percentageSpan);
    }, 2000);
}




        // Função para mostrar o quadrado preto
        function showBlackSquare() {
            var square = document.getElementById('blackSquare');
            square.style.display = 'block';
        }
        function showWhiteSquares() {
    var square = document.getElementById('blackSquare');
    square.innerHTML = ''; // Limpa qualquer conteúdo anterior
    
    var size = 100; // Tamanho dos quadrados ajustado para 100 pixels
    var gapHorizontal = 5; // Espaço horizontal entre os quadrados em pixels
    var gapVertical = 5; // Espaço vertical entre os quadrados em pixels

    // Criar 5 colunas
    for (let col = 0; col < 5; col++) {
        // Criar 5 quadrados em cada coluna
        for (let row = 0; row < 5; row++) {
            var whiteSquare = document.createElement('div');
            whiteSquare.className = 'white-square';
            whiteSquare.style.top = (row * (size + gapVertical)) + 'px';
            whiteSquare.style.left = (col * (size + gapHorizontal)) + 'px';
            
            // Adicionar imagem de diamante (ou outro conteúdo desejado)
            var diamondImg = document.createElement('img');
            diamondImg.src = '/static/media/background-game.602c4786.svg'; // Caminho da imagem
            diamondImg.alt = 'diamond'; // Texto alternativo da imagem
            diamondImg.className = 'image-box'; // Classe da imagem (se necessário)
            
            whiteSquare.appendChild(diamondImg);
            square.appendChild(whiteSquare);
        }
    }
}

// Função para embaralhar array
function shuffleArray(array) {
    for (let i = array.length - 1; i > 0; i--) {
        const j = Math.floor(Math.random() * (i + 1));
        [array[i], array[j]] = [array[j], array[i]];
    }
}

function showWhiteSquares() {
    var square = document.getElementById('blackSquare');
    square.innerHTML = ''; // Limpa qualquer conteúdo anterior
    
    var size = 100; // Tamanho dos quadrados ajustado para 100 pixels
    var gapHorizontal = 5; // Espaço horizontal entre os quadrados em pixels
    var gapVertical = 5; // Espaço vertical entre os quadrados em pixels

    // Criar 5 colunas
    for (let col = 0; col < 5; col++) {
        // Criar 5 quadrados em cada coluna
        for (let row = 0; row < 5; row++) {
            var whiteSquare = document.createElement('div');
            whiteSquare.className = 'white-square';
            whiteSquare.style.top = (row * (size + gapVertical)) + 'px';
            whiteSquare.style.left = (col * (size + gapHorizontal)) + 'px';
            
            // Adicionar imagem de diamante (ou outro conteúdo desejado)
            var diamondImg = document.createElement('img');
            diamondImg.src = '/static/media/background-game.602c4786.svg'; // Caminho da imagem
            diamondImg.alt = 'diamond'; // Texto alternativo da imagem
            diamondImg.className = 'image-box'; // Classe da imagem (se necessário)
            
            whiteSquare.appendChild(diamondImg);
            square.appendChild(whiteSquare);
        }
    }

    // Adicionar o botão "ander"
    var anderButton = document.createElement('button');
    anderButton.className = 'btn btn-primary ander-button';
    anderButton.textContent = 'Ander';
    square.appendChild(anderButton);
}




// Evento ao clicar no botão Parar Roleta
document.querySelector('.context-option:nth-child(4)').addEventListener('click', function() {
    showWhiteSquares();
});

        // Evento ao clicar no botão Hackear Double
        document.querySelector('.context-option:nth-child(4)').addEventListener('click', function() {
            showBlackSquare();
        });
    </script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.0/js/bootstrap.bundle.min.js"></script>
</body>
</html>
