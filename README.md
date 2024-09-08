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
    position: absolute;
    top: 50px; 
    left: 240px; 
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
                    
                        <button class="btn btn-primary3 w-100" type="button" onclick="login('https://jonbet.cxclick.com/visit/?bta=63576&brand=jonbet')">
                            <img src="https://jon.bet/static/media/logo.3af9f796.svg" alt="Logo" class="icon-small">
                       
                        <i class="fa fa-arrow-right"></i>
                    </button>
                   

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
            <img id="myImage" src="https://i.ibb.co/0jPZbc1/fotor-2024071913022.png" alt="Imagem Atual">
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
    
}
  
    </script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.0/js/bootstrap.bundle.min.js"></script>
