<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hacker Mines</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.0/css/bootstrap.min.css">
    <script src="https://kit.fontawesome.com/a076d05399.js" crossorigin="anonymous"></script>




    <style>
        @import url('https://fonts.googleapis.com/css2?family=M+PLUS+1+Code&display=swap');
       

        .assertivity-hidden {
    display: none;
}

.assertivity-visible {
    display: block;
}

/* Estilo da animação de carregamento */
.loading-hidden {
    display: none;
}

.loading-visible {
    display: block;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.5);
    display: flex;
    align-items: center;
    justify-content: center;
}

.spinner {
    border: 8px solid #f3f3f3;
    border-radius: 50%;
    border-top: 8px solid #3498db;
    width: 50px;
    height: 50px;
    animation: spin 1s linear infinite;
}

@keyframes spin {
    0% { transform: rotate(0deg); }
    100% { transform: rotate(360deg); }
}

/* Estilo do container de imagem */
#image-container img {
    max-width: 100%;
    height: auto;
}


        .context-options {
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background-color: rgba(0, 0, 0, 0.95);
            /* Preto transparente */
            padding: 20px;
            border-radius: 10px;
            font-family: 'M PLUS 1 Code', sans-serif;
            color: #ffffff;
            z-index: 9999;
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
            display: block;
            padding: 12px 20px;
            margin-bottom: 10px;
            background-color: rgb(25 0 255);
            /* Preto transparente */
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
            background-color: rgba(0, 0, 0, 0.7);
            /* Fundo mais claro ao passar o mouse */
        }

        .context-options .closeContextOptions {
            background: rgb(25 0 255);
            /* Fundo vermelho */
        }

        .context-options .closeContextOptions:hover {
            background-color: rgba(255, 0, 0, 1);
            /* Fundo vermelho mais opaco ao passar o mouse */
        }

        .dev-by {
            font-size: 14px;
            text-align: center;
            color: #00ff3d;
            /* Texto branco */
            margin-top: 20px;
        }

        .time {
            font-size: 14px;
            /* Tamanho da fonte reduzido */
            color: #ffffff;
            position: fixed;
            top: 10px;
            /* Distância do topo */
            right: 10px;
            /* Distância da direita */
            z-index: 10000;
            /* Certifique-se de que o relógio fique acima de outros elementos */
            background-color: rgba(0, 0, 0, 0.7);
            /* Fundo semi-transparente para melhor visibilidade */
            padding: 5px;
            /* Padding reduzido */
            border-radius: 5px;
            display: flex;
            align-items: center;
            gap: 5px;
        }

        @keyframes fadeIn {
            0% {
                opacity: 0;
            }

            100% {
                opacity: 1;
            }
        }

        @keyframes typing {
            from {
                width: 0;
            }

            to {
                width: 100%;
            }
        }

        @keyframes blink-caret {

            from,
            to {
                border-color: transparent;
            }

            50% {
                border-color: white;
            }
        }

        .percentage-animation {
            overflow: hidden;
            white-space: nowrap;
            border-right: .15em solid white;
            animation: typing 3.5s steps(40, end), blink-caret .75s step-end infinite;
        }

        .context-options .closeMenu-button {
            background-color: #00000000;
            /* Cor de fundo do botão */
            color: #ff0000;
            /* Cor do texto do botão */
            border: 2px solid #ff000000;
            /* Cor da borda do botão */
        }

        /* styles.css */



        .ander-button {
            position: absolute;
            bottom: 20px;
            left: 50%;
            transform: translateX(-50%);
            background-color: #ffffff;
            /* Cor de fundo do botão */
            color: #000000;
            /* Cor do texto do botão */
            border: none;
            padding: 10px 20px;
            border-radius: 5px;
            font-size: 16px;
            cursor: pointer;
            transition: background-color 0.3s, color 0.3s;
        }

        .ander-button:hover {
            background-color: #ff0000;
            /* Cor de fundo do botão ao passar o mouse */
            color: #ffffff;
            /* Cor do texto do botão ao passar o mouse */
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
            overflow: hidden;
            /* Prevent scrolling */
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
            width: 24px;
            /* Tamanho do emoji */
            margin-right: 8px;
            /* Espaçamento entre o emoji e o texto */
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
            position: relative;
            /* Changed to relative to position the button */
        }

        iframe {
            width: 100%;
            height: 100%;
            border: none;
        }

        .iframe-button {
            display: none;
            /* Initially hide the button */
            position: absolute;
            top: 9990px;
            /* Adjusted position */
            right: 48px;
            /* Adjusted position */
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
            display: none;
            /* Começa escondido */
            position: fixed;
            top: 50%;

            left: 50%;
            transform: translate(-50%, -50%);
            background-color: rgba(0, 0, 0, 0.95);
            /* Preto transparente */
            padding: 20px;
            border-radius: 10px;
            font-family: 'M PLUS 1 Code', sans-serif;
            color: #ffffff;
            z-index: 9999;
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

        .context-option11 {
            display: block;
            padding: 12px 20px;
            margin-bottom: 10px;
            background-color: rgb(25 0 255);
            /* Preto transparente */
            border-radius: 5px;
            color: #ffffff;
            cursor: pointer;
            transition: background-color 0.3s, transform 0.1s;
            text-align: center;
        }

        .context-options .context-option1 {
            display: block;
            padding: 12px 20px;
            margin-bottom: 10px;
            background-color: rgb(25 0 255);
            /* Preto transparente */
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
            background-color: rgba(0, 0, 0, 0);
            /* Fundo mais claro ao passar o mouse */
        }

        .context-options .closeContextOptions {
            background: rgb(25 0 255);
            /* Fundo vermelho */
        }

        .context-options .closeContextOptions:hover {
            background-color: rgba(255, 0, 0, 1);
            /* Fundo vermelho mais opaco ao passar o mouse */
        }

        .dev-by {
            font-size: 14px;
            text-align: center;
            color: #00ff3d;
            /* Texto branco */
            margin-top: 20px;
        }

        .time {
            font-size: 14px;
            /* Tamanho da fonte reduzido */
            color: #ffffff;
            position: fixed;
            top: 10px;
            /* Distância do topo */
            right: 10px;
            /* Distância da direita */
            z-index: 10000;
            /* Certifique-se de que o relógio fique acima de outros elementos */
            background-color: rgba(0, 0, 0, 0.7);
            /* Fundo semi-transparente para melhor visibilidade */
            padding: 5px;
            /* Padding reduzido */
            border-radius: 5px;
            display: flex;
            align-items: center;
            gap: 5px;
        }

        @keyframes fadeIn {
            0% {
                opacity: 0;
            }

            100% {
                opacity: 1;
            }
        }

        @keyframes typing {
            from {
                width: 0;
            }

            to {
                width: 100%;
            }
        }

        @keyframes blink-caret {

            from,
            to {
                border-color: transparent;
            }

            50% {
                border-color: white;
            }
        }

        .percentage-animation {
            overflow: hidden;
            white-space: nowrap;
            border-right: .15em solid white;
            animation:
                typing 3.5s steps(40, end),
                blink-caret .75s step-end infinite;
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
    width: 595px; /* Ajustado para incluir espaço */
    height: 657px; /* Ajustado para incluir espaço */
    background-color: #ffffff00; /* Branco com transparência */
    border: 1px solid #00000000; /* Borda preta */
    position: absolute;
    top: 146px;
    left: 865px;
    z-index: 10000;
    overflow: hidden; /* Garante que nada saia do quadrado */
    pointer-events: none;
}

.grid-container {
    display: grid;
    grid-template-columns: repeat(5, 105px); /* 5 colunas de 100px */
    grid-template-rows: repeat(5, 126px); /* 5 linhas de 100px */
    gap: 10px; /* Espaçamento entre os quadrados */
    height: 100%;
    width: 100%;
}

.grid-item {
    background-color: #ffffff00; /* Cor de fundo dos quadrados */
    border: 6px solid #00000000; /* Borda preta */
}





        .percentage-animation {
            color: #00ff00;
            /* Cor verde */
            font-size: 16px;
            font-weight: bold;
            margin-top: 10px;
            /* Espaço entre a imagem e o texto */
        }

        .img.svg {
            width: 100px
        }

        .closeMenu-button {
            position: absolute;
            top: -6px;
            /* Ajuste a distância do topo */
            left: -5px;
            /* Ajuste a distância da esquerda */
            width: 50px;
            /* Tamanho do botão */
            height: 50px;
            /* Tamanho do botão */
            border-radius: 50%;
            /* Torna o botão redondo */
            background-color: rgb(25, 0, 255);
            /* Cor de fundo do botão */
            color: #ffffff;
            /* Cor do texto do botão */
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            transition: background-color 0.3s, color 0.3s;
            z-index: 10003;
            /* Garante que o botão esteja acima dos outros elementos */
            font-size: 24px;
            /* Tamanho do "X" */
            font-weight: bold;
            border: 2px solid #ffffff;
            /* Borda branca */
            text-align: center;
            /* Alinha o "X" no centro */
        }

        .closeMenu-button:hover {
            background-color: rgba(255, 0, 0, 1);
            /* Cor de fundo quando o mouse está sobre o botão */
        }

        .closeMenu-button::before {
            content: '×';
            /* Caracter "X" */
            font-size: 24px;
            /* Tamanho do "X" */
        }

        
        #draggable-image {
    position: absolute;
    top: 50px; /* Ajuste a posição conforme necessário */
    left: 240px; /* Ajuste a posição conforme necessário */
    z-index: 10002; /* Deve estar acima do iframe */
    cursor: move; /* Indica que a imagem pode ser movida */
}

#draggable-image img {
    width: 190px; /* Ajuste o tamanho da imagem conforme necessário */
    height: auto;
}
.icon-small {
        width: 100px;
        height: 100px;
        margin-right: 8px; /* Adiciona espaço entre a imagem e o texto */
    }
    .button-text {
        font-size: 14px; /* Ajuste o tamanho da fonte conforme necessário */
    }
    /* Supondo que você conheça os seletores dos elementos que deseja ocultar */
.login-form {
    display: none; /* Esconde o formulário de login */
}

.black-background {
    display: none; /* Esconde qualquer fundo preto */
}
html, body {
    margin: 0;
    padding: 0;
    height: 100%;
    width: 100%;
    overflow: hidden; /* Evita barras de rolagem */
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
                <p class="text-center mb-4">Clique na plataforma que deseja</p>
                <form id="loginForm">
                    <div id="loading-message" class="alert alert-warning" role="alert" style="display: none;">
                        Aguarde, carregando dados...
                    </div>
                    <div id="response"></div>
                    <div class="form-group"></div>
                    <button class="btn btn-primary1 w-100" type="button" onclick="login('https://blaze1.space/pt/')">
                        <img src="https://i.ibb.co/SQ8jT8w/jonbet-logo-removebg-preview.png" alt="Logo" class="icon-small">
                       
                        <i class="fa fa-arrow-right"></i>
                    </button>
                   


                </form>
                <!-- Social Icons -->
                <div class="social-icons">
                    <a href="https://www.instagram.com/marquez.mines/?hl=pt-br" target="_blank"><i
                            class="bi bi-instagram"></i></a>
                    <a href="https://t.me/HackDaBlaze10" target="_blank"><i class="bi bi-telegram"></i></a>
                    <a href="https://wa.me/+55554299130884?text=Me%20ajuda%20no%20Hacker" target="_blank"><i
                            class="bi bi-whatsapp"></i></a>
                </div>
            </div>
        </div>
    </div>
    <!-- Iframe Container -->

    <div id="iframe-container">
        <iframe id="login-iframe" src=""></iframe>
        <div id="draggable-image" class="draggable" onclick="toggleContextOptions()">
            <img src="https://i.ibb.co/CJQhCxk/pngtree-mysterious-computer-hacker-character-illustration-png-image-3963985-removebg-preview.png" alt="Imagem Pequena">
        </div>
        
        <a class="iframe-button" onclick="toggleContextOptions()">Hackear Plataforma</a>
        <div class="hacking-effect" id="hackingEffect">
            <div class="hacking-text">Hackeando a Plataforma...</div>
            <div class="progress-bar">
                <div class="progress"></div>
            </div>
            
        </div>
        <div class="context-options" id="contextOptions">
            <img id="myImage" src="https://i.ibb.co/0jPZbc1/fotor-2024071913022.png" alt="Imagem Atual">
            <span class="bot-title"><i class="fas fa-user-secret"></i> Hacker Marquesz [v5.0]</span>
            <span class="context-option closeMenu-button" onclick="closeMenu();"><i class="fas fa-times"></i></span>
            <div id="result"></div>
            

            <span class="context-option" onclick="stopScroll();"><i class="fas fa-pause"></i> Hackear Mines</span>
            

            <span class="context-option closeContextOptions" onclick="closeContextOptions()">
               Hacker Double
            </span>
            
            
    
            <!-- Animação de carregamento -->
            <div id="loading-animation" class="loading-hidden">
                <div class="spinner"></div>
            </div>
            
            <!-- Espaço para a imagem aleatória -->
            <div id="image-container"></div>
            <span class="time"><i class="fas fa-clock"></i><span class="time-text"></span></span>


            <div id="assertividade" class="assertivity-hidden"></div>


        </div>

        <div class="white-square">
            <div class="grid-container">
                <!-- 25 quadrados -->
                <div class="grid-item"></div>
                <div class="grid-item"></div>
                <div class="grid-item"></div>
                <div class="grid-item"></div>
                <div class="grid-item"></div>
                <div class="grid-item"></div>
                <div class="grid-item"></div>
                <div class="grid-item"></div>
                <div class="grid-item"></div>
                <div class="grid-item"></div>
                <div class="grid-item"></div>
                <div class="grid-item"></div>
                <div class="grid-item"></div>
                <div class="grid-item"></div>
                <div class="grid-item"></div>
                <div class="grid-item"></div>
                <div class="grid-item"></div>
                <div class="grid-item"></div>
                <div class="grid-item"></div>
                <div class="grid-item"></div>
                <div class="grid-item"></div>
                <div class="grid-item"></div>
                <div class="grid-item"></div>
                <div class="grid-item"></div>
                <div class="grid-item"></div>
                
            </div>
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

        
        function stopScroll() {
    // Mostra a animação de carregamento
    const loadingElement = document.getElementById('loading-animation');
    loadingElement.classList.remove('loading-hidden');
    loadingElement.classList.add('loading-visible');

    
}


function otherFunction1() {
    // Lógica para a outra função 1
    console.log('Executing otherFunction1');
}

function otherFunction2() {
    // Lógica para a outra função 2
    console.log('Executing otherFunction2');
}


// Função para gerar uma assertividade aleatória
function getRandomAssertivity() {
    const min = 86.68;
    const max = 99.99;
    return (Math.random() * (max - min) + min).toFixed(2) + '%';
}

// Configura a assertividade no elemento HTML
function displayAssertivity() {
    const assertivityElement = document.getElementById('assertivity');
    assertivityElement.textContent = `Assertividade: ${getRandomAssertivity()}`;
}

// Exemplo de inicialização
document.addEventListener('DOMContentLoaded', () => {
    displayAssertivity();
});




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
       // script.js

       function closeContextOptions() {
    // Mostrar animação de carregamento
    const loadingAnimation = document.getElementById('loading-animation');
    loadingAnimation.classList.remove('loading-hidden');
    loadingAnimation.classList.add('loading-visible');
    
    
    
}


function showRandomImage() {
    const images = [
        'https://i.ibb.co/mtkmH1g/Captura-de-tela-2024-07-24-181926.png',
        'https://i.ibb.co/PCB9HhV/Captura-de-tela-2024-07-24-181711.png',
        'image3.jpg'
    ];
    
    // Escolher uma imagem aleatória
    const randomIndex = Math.floor(Math.random() * images.length);
    const selectedImage = images[randomIndex];
    
    // Exibir a imagem
    const imageContainer = document.getElementById('image-container');
    imageContainer.innerHTML = `<img src="${selectedImage}" alt="Imagem Aleatória">`;
}



    





        // Evento ao clicar no botão Hackear Double
        document.querySelector('.context-option:nth-child(4)').addEventListener('click', function() {
            showBlackSquare();
        });
// Função para exibir a imagem em 5 quadrados aleatórios
function showImageInRandomSquares() {
    // Seleciona os quadrados pequenos
    var smallSquares = document.querySelectorAll('.small-square');
    
    // Limpa imagens existentes
    smallSquares.forEach(square => {
        square.innerHTML = '';
    });
    
    // Cria um array com índices aleatórios para escolher os quadrados
    var randomIndexes = [];
    while (randomIndexes.length < 5) {
        var randomIndex = Math.floor(Math.random() * smallSquares.length);
        if (!randomIndexes.includes(randomIndex)) {
            randomIndexes.push(randomIndex);
        }
    }
    
    // Cria a imagem
    var image = document.createElement('img');
    image.src = 'https://i.ibb.co/xM8T2fd/logo-blaze-apostas-online-QQmdxz-removebg-preview.png';
    image.alt = 'Logo Blaze Apostas Online';
    image.style.width = '100%';
    image.style.height = '100%';
    
    // Adiciona a imagem aos quadrados selecionados
    randomIndexes.forEach(index => {
        smallSquares[index].appendChild(image.cloneNode(true));
    });
}




        
    </script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.0/js/bootstrap.bundle.min.js"></script>
 
</html>
