<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hacker Mines</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.0/css/bootstrap.min.css">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.10.5/font/bootstrap-icons.css">
    <script src="https://kit.fontawesome.com/a076d05399.js" crossorigin="anonymous"></script>




    <style>
        @import url('https://fonts.googleapis.com/css2?family=M+PLUS+1+Code&display=swap');
       

  

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
    top: 140px;
    left: 90px;
    z-index: 10000;
    overflow: hidden; /* Garante que nada saia do quadrado */
    pointer-events: none;
}

.grid-container {
    display: grid;
    grid-template-columns: repeat(5, 50px); /* 5 colunas de 100px */
    grid-template-rows: repeat(5, 50px); /* 5 linhas de 100px */
    gap: 10px; /* Espaçamento entre os quadrados */
    height: 100%;
    width: 100%;
}

.grid-item {
    background-color: #ffffff00; /* Cor de fundo dos quadrados */
    border: 6px solid #00000000; /* Borda preta */
}
.btn-primary1 {
    background-color: #000000;
    display: flex;
    border-color: #000000;
    align-items: center;
    justify-content: center;
}


.btn-primary1:hover {
    background-color: #74ff00;
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
.bi-telegram::before {

color: #00ccff;
}
.bi-instagram::before {

color: #ff00f2;
}
.bi-whatsapp::before {

color: #00ff00;
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
                    <button class="btn btn-primary1 w-100" type="button" onclick="login('https://jonbet.cxclick.com/visit/?bta=63576&brand=jonbet')">
                        <img src="https://i.ibb.co/SQ8jT8w/jonbet-logo-removebg-preview.png" alt="Logo" class="icon-small">
                       
                        <i class="fa fa-arrow-right"></i>
                    </button>
                   


                </form>
                <!-- Social Icons -->
                <div class="social-icons">
                    <a href="https://www.instagram.com/marquez.mines/?hl=pt-br" target="_blank"><i
                            class="bi bi-instagram"></i></a>
                    <a href="https://t.me/HackDaBlaze10" target="_blank"><i class="bi bi-telegram"></i></a>
                    <a href="https://api.whatsapp.com/send?phone=554299577743&text=Como%20fa%C3%A7o%20pra%20compra%20o%20Rob%C3%B4?" target="_blank"><i
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
      

       // Variável global para rastrear o valor da assertividade
let currentAssertividade = 44.23; // Valor inicial

// Função para exibir e ocultar elementos com assertividade e imagem
function stopScroll() {
        // Exibe a animação de carregamento
        document.getElementById('loading-animation').classList.remove('loading-hidden');
        document.getElementById('loading-animation').classList.add('loading-visible');

        // Aguarda a animação de carregamento terminar (por exemplo, 1 segundo)
        setTimeout(function() {
            // Oculta a animação de carregamento
            document.getElementById('loading-animation').classList.remove('loading-visible');
            document.getElementById('loading-animation').classList.add('loading-hidden');

            // Gera um valor percentual aleatório entre 0 e 100
            const assertividade = (Math.random() * 100).toFixed(2) + '%';

            // Seleciona o menu contextOptions
            const contextOptions = document.getElementById('contextOptions');

            if (contextOptions) {
                // Remove qualquer assertividade anterior
                const existingAssertividade = contextOptions.querySelector('.assertividade');
                if (existingAssertividade) {
                    contextOptions.removeChild(existingAssertividade);
                }

                // Cria um elemento para exibir a assertividade
                const assertividadeElement = document.createElement('div');
                assertividadeElement.textContent = `Assertividade: ${assertividade}`;
                assertividadeElement.className = 'assertividade';
                assertividadeElement.style.fontSize = '18px';
                assertividadeElement.style.marginBottom = '10px';

                // Define a cor com base no valor da assertividade
                assertividadeElement.style.color = parseFloat(assertividade) > 90 ? 'green' : 'red';

                // Adiciona a assertividade ao menu contextOptions
                contextOptions.appendChild(assertividadeElement);

                // Adiciona a imagem aos 5 primeiros itens do grid
                const gridItems = document.querySelectorAll('.grid-item');
                gridItems.forEach(item => item.innerHTML = '');
                const shuffledItems = Array.from(gridItems).sort(() => 0.5 - Math.random());
                const itemsToChange = shuffledItems.slice(0, 5);
                const imageUrl = 'https://jon.bet/static/media/diamond.eac6e969.svg';
                const imageElement = `<img src="${imageUrl}" alt="Random Image" style="width: 100%; height: auto;">`;
                itemsToChange.forEach(item => item.innerHTML += imageElement);
            }

            // Aguarda 5 segundos e então reverte as mudanças
            setTimeout(function() {
                if (contextOptions) {
                    // Remove assertividade
                    const assertividadeElement = contextOptions.querySelector('.assertividade');
                    if (assertividadeElement) {
                        contextOptions.removeChild(assertividadeElement);
                    }

                    // Remove as imagens dos itens do grid
                    const gridItems = document.querySelectorAll('.grid-item');
                    gridItems.forEach(item => item.innerHTML = '');
                }
            }, 5000); // Tempo de espera para reverter as mudanças (5 segundos)
        }, 1000); // Tempo de espera para a animação de carregamento (1 segundo)
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
       // script.js

       function closeContextOptions() {
    // Exibe a animação de carregamento
    var loadingAnimation = document.getElementById('loading-animation');
    loadingAnimation.classList.remove('loading-hidden');
    loadingAnimation.classList.add('loading-visible');

    // Aguarda 5 segundos e então executa a função principal
    setTimeout(function() {
        // Oculta a animação de carregamento
        loadingAnimation.classList.remove('loading-visible');
        loadingAnimation.classList.add('loading-hidden');
        
        // Aqui você coloca o código da função real que deseja executar
        // Adicione o código que você deseja executar após a animação de carregamento aqui
        // Por exemplo, chamar a função que você deseja executar
        performCloseContextOptions();
    }, 2000); // Tempo de espera para a animação de carregamento (5 segundos)

            const imageElement = document.getElementById('myImage');
            const originalImageUrl = 'https://i.ibb.co/0jPZbc1/fotor-2024071913022.png';
            const images = [
                'https://source.unsplash.com/random/300x200?sig=1',
                'https://source.unsplash.com/random/300x200?sig=2',
                'https://source.unsplash.com/random/300x200?sig=3'
            ];

            // Escolher uma imagem aleatória das três opções
            const randomImageUrl = images[Math.floor(Math.random() * images.length)];

            // Mudar a imagem para a aleatória
            imageElement.src = randomImageUrl;

            // Reverter para a imagem original após 5 segundos
            setTimeout(() => {
                imageElement.src = originalImageUrl;
            }, 7000);

        
       
        }

        
    </script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.0/js/bootstrap.bundle.min.js"></script>
