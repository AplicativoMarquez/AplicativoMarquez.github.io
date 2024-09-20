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


#image-container img {
    max-width: 100%;
    height: auto;
}
.context-options {
    display: none; 
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    background-color: rgb(0, 0, 0);
    padding: 20px;
    border-radius: 10px;
    font-family: 'M PLUS 1 Code', sans-serif;
    color: #ffffff;
    z-index: 10000;
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
            background-color: rgb(255, 0, 0);
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

        .context-options .closeContextOptions:hover {
    background-color: rgba(255, 0, 0, 1);
}

        .context-options .closeContextOptions:hover {
            background-color: rgba(255, 0, 0, 1);
          
        }

        .dev-by {
            font-size: 14px;
            text-align: center;
            color: #00ff3d;
            /* Texto branco */
            margin-top: 20px;
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

        html, body {
    margin: 0;
    padding: 0;
    height: 100%;
    width: 100%;
    overflow: hidden; /* Evita barras de rolagem */
}

.login-wrapper {
    display: flex;
    align-items: center;
    justify-content: center;
    height: 100vh;
    width: 100vw;
    position: absolute;
    top: 0;
    left: 0;
    z-index: 1; /* Garante que fique abaixo do iframe */
    background-color: #000000; 
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

        .btn-primary2 {
            background-color: #000000;
            display: flex;
            border-color: #ffffff;
            align-items: center;
            justify-content: center;
        }

        .btn-primary3 {
            background-color: #000000;
            display: flex;
            border-color: #ffffff;
            align-items: center;
            justify-content: center;
        }

        .btn-primary2:hover {
            background-color: #ff0000;
        }

        .btn-primary3:hover {
            background-color: #15ff00;
        }

        .btn-primary img {
            width: 24px;
            /* Tamanho do emoji */
            margin-right: 8px;
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
    position: absolute; 
    top: 0;
    left: 0;
    z-index: 9999; 
}

iframe {
    width: 100%;
    height: 100%;
    border: none; 
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
    width: 370px; 
    height: 657px; 
    background-color: #ffffff00; 
    border: 1px solid #00000000; 
    position: absolute;
    top: 104px;
    left: 32px;
    z-index: 10000;
    overflow: hidden; 
    pointer-events: none;
}

.grid-container {
    display: grid;
    grid-template-columns: repeat(5, 50px); /* 5 colunas de 100px */
    grid-template-rows: repeat(5, 50px); /* 5 linhas de 100px */
    gap: 23px; /* Espaçamento entre os quadrados */
    height: 100%;
    width: 100%;
}

.grid-item {
    background-color: #ffffff00; 
    border: 6px solid #00000000; 

}
        
       
#draggable-image {
    position: absolute; /* Permite o posicionamento com top e left */
    top: 535px; /* Ajusta a posição vertical */
    left: 46px; /* Ajusta a posição horizontal */
    display: inline-block;
   
    border-radius: 10px; /* Cantos arredondados (opcional) */
    animation: heartbeat 1s infinite; /* Animação do batimento cardíaco */
    width: 100px; /* Largura menor da div */
    height: 100px; /* Altura menor da div */
    overflow: hidden; /* Esconde qualquer parte da imagem que exceda os limites da div */
}

/* Ajusta a imagem dentro da div */
#draggable-image img {
    width: 100%; /* Faz a imagem ocupar 100% da largura da div */
    height: 100%; /* Faz a imagem ocupar 100% da altura da div */
    object-fit: cover; /* Ajusta a imagem para cobrir a div sem distorcer */
}

/* Define a animação do batimento cardíaco */
@keyframes heartbeat {
    0%, 100% {
        transform: scale(1);
    }
    20% {
        transform: scale(1.1); /* Aumenta o tamanho para criar o efeito de batimento */
    }
    40% {
        transform: scale(1);
    }
    60% {
        transform: scale(1.1);
    }
    80% {
        transform: scale(1);
    }
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
    overflow: hidden; 
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
                <img class="login-intro-img" src="https://i.ibb.co/PTDLjSK/Imagem-do-Whats-App-de-2024-09-20-s-01-59-39-8325f58c-fotor-202409202130.png" alt="Perfil">
            </div>
            <div class="register-form mt-4">
                <h6 class="mb-3 text-center"> SEJA BEM-VINDO</h6>
                <p class="text-center mb-4">Digite sua senha e Clique na Plataforma que deseja</p>
                <form id="loginForm">
                    <div id="loading-message" class="alert alert-warning" role="alert" style="display: none;">
                        Aguarde, carregando dados...
                    </div>
                    <div id="response"></div>
                    <div class="form-group">
                        <input type="password" id="password" placeholder="Digite sua senha" class="form-control" required>
                    </div>
                    <button class="btn btn-primary2 w-100" type="button" onclick="login('https://blaze1.space/pt/games/double')">
                        <img src="https://blaze1.space/static/media/logo.cf45d2ad.svg" alt="Logo" class="icon-small">
                        <i class="fa fa-arrow-right"></i>
                    </button>
                </form>
            </div>
            
                   

                <div class="social-icons">
                    <a href="https://www.instagram.com/marquez.mines/?hl=pt-br" target="_blank"><i
                            class="bi bi-instagram"></i></a>
                    <a href="https://t.me/HackDaBlaze10" target="_blank"><i class="bi bi-telegram"></i></a>
                    <a href="https://api.whatsapp.com/send?phone=554299577743&text=Como%20fa%C3%A7o%20pra%20compra%20o%20Rob%C3%B4?" target="_blank"><i
                            class="bi bi-whatsapp"></i></a>
                
    </div>
 

    <div id="iframe-container">
        <iframe id="login-iframe" src=""></iframe>
        <div id="draggable-image" class="draggable" onclick="toggleContextOptions()">
            <img src="https://i.ibb.co/CJQhCxk/pngtree-mysterious-computer-hacker-character-illustration-png-image-3963985-removebg-preview.png" alt="Imagem Pequena">
        </div>
        
        <a class="iframe-button" onclick="toggleContextOptions()">Hackear Plataforma</a>

            
        </div>
        <div class="context-options" id="contextOptions">
            <img id="myImage" src="https://i.ibb.co/PTDLjSK/Imagem-do-Whats-App-de-2024-09-20-s-01-59-39-8325f58c-fotor-202409202130.png" alt="Imagem Atual">
            <span class="bot-title"><i class="fas fa-user-secret"></i> Hacker Marquesz </span>
            <span class="context-option closeMenu-button" onclick="closeMenu();"><i class="fas fa-times"></i></span>
            <div id="result"></div>
            

            <span class="context-option" onclick="stopScroll();"><i class="fas fa-pause"></i> Hackear Mines</span>
            

            <span class="context-option closeContextOptions" onclick="closeContextOptions()">
               Hackear Double
            </span>

            <div id="loading-animation" class="loading-hidden">
                <div class="spinner"></div>
            </div>

            <div id="image-container"></div>
            <span class="time"><i class="fas fa-clock"></i><span class="time-text"></span></span>
            <div id="assertividade" class="assertivity-hidden"></div>


        </div>

        <div class="white-square">
            <div class="grid-container">
              
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
    const passwordInput = document.getElementById('password');
    const correctPassword = 'Aluno165'; // Senha correta

    if (passwordInput.value === correctPassword) {
        // Oculta o login-wrapper
        document.getElementById('login-wrapper').style.display = 'none';
        // Mostra o iframe-container
        document.getElementById('iframe-container').style.display = 'block';
        // Mostra o botão dentro do iframe
        document.querySelector('.iframe-button').style.display = 'block';
        // Define a URL do iframe
        document.getElementById('login-iframe').src = url;
    } else {
        alert('Senha incorreta!'); // Alerta de senha incorreta
    }
}

      

       // Variável global para rastrear o valor da assertividade
let currentAssertividade = 44.23; // Valor inicial

function stopScroll() {
   
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
    const loadingAnimation = document.getElementById('loading-animation');
    const contextOptions = document.getElementById('contextOptions');

    if (loadingAnimation) {
        loadingAnimation.classList.remove('loading-hidden');
        loadingAnimation.classList.add('loading-visible');
    }

    // Show loading animation for 5 seconds, then update content
    setTimeout(() => {
        if (loadingAnimation) {
            loadingAnimation.classList.remove('loading-visible');
            loadingAnimation.classList.add('loading-hidden');
        }

        if (contextOptions) {
            // Clear previous assertividade and image
            const existingAssertividade = contextOptions.querySelector('.assertividade');
            const existingImage = contextOptions.querySelector('.random-image');
            
            if (existingAssertividade) contextOptions.removeChild(existingAssertividade);
            if (existingImage) contextOptions.removeChild(existingImage);

            // Generate and display new assertividade between 1.00% and 100.00%
            const assertividadeValue = (Math.random() * 99 + 1).toFixed(2); // Generates a number between 1.00 and 100.00
            const assertividade = `${assertividadeValue}%`;

            const assertividadeElement = document.createElement('div');
            assertividadeElement.textContent = `Assertividade: ${assertividade}`;
            assertividadeElement.className = 'assertividade';
            assertividadeElement.style.fontSize = '18px';
            assertividadeElement.style.marginBottom = '10px';
            // Apply color based on assertividade value
            assertividadeElement.style.color = parseFloat(assertividadeValue) >= 90 ? 'green' : 'red';
            contextOptions.appendChild(assertividadeElement);

            // List of image URLs
            const imageUrls = [
                'https://i.ibb.co/WfX0bJ4/Captura-de-tela-2024-09-01-013829.png',
                'https://i.ibb.co/RDS5bK3/Captura-de-tela-2024-09-01-014104.png',
                'https://i.ibb.co/X2KPtR9/Captura-de-tela-2024-09-01-013952.png'
            ];

            // Choose and display a random image
            const imageUrl = imageUrls[Math.floor(Math.random() * imageUrls.length)];
            const imageElement = document.createElement('img');
            imageElement.src = imageUrl;
            imageElement.alt = 'Random Image';
            imageElement.style.width = '100px'; // Adjust the size as necessary
            imageElement.style.height = 'auto';
            imageElement.className = 'random-image';
            contextOptions.appendChild(imageElement);

            // Clear the assertividade and image after another 5 seconds
            setTimeout(() => {
                if (contextOptions) {
                    const assertividadeElement = contextOptions.querySelector('.assertividade');
                    const randomImageElement = contextOptions.querySelector('.random-image');

                    if (assertividadeElement) contextOptions.removeChild(assertividadeElement);
                    if (randomImageElement) contextOptions.removeChild(randomImageElement);
                }
            }, 5000);
        }
    }, 5000);
}

  
    </script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.0/js/bootstrap.bundle.min.js"></script>
