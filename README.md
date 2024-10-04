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
        .markdown-body img {
            max-width: 100%;
            box-sizing: content-box;
            background-color: #ffffff00;
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
    border: 8px solid #222;
    border-radius: 50%;
    border-top: 8px solid #ff0000;
    width: 50px;
    height: 50px;
    animation: spin 1s linear infinite;
    box-shadow: 0 0 20px rgba(255, 0, 0, 0.7);
}

        @keyframes spin {
            0% {
                transform: rotate(0deg);
            }

            100% {
                transform: rotate(360deg);
            }
        }

        #image-container img {
            max-width: 100%;
            height: auto;
        }

        .feedback-hidden {
    display: none;
    color: #ffffff;
    font-family: 'M PLUS 1 Code', monospace;
    margin-top: 10px;
}

#hack-feedback {
    font-size: 14px;
    text-align: center;
    margin-top: 20px;
    color: #00ff3d;
    background-color: rgba(0, 0, 0, 0.8);
    padding: 10px;
    border-radius: 5px;
    width: 100%;
    display: none; /* Hide until hack starts */
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
    font-size: 22px;
    text-align: center;
    margin-bottom: 20px;
    color: #ffffff;
    text-shadow: 0 0 10px rgba(255, 255, 255, 0.7);
}

.context-options .context-option {
    display: block;
    padding: 12px 20px;
    margin-bottom: 10px;
    background-color: rgb(255, 0, 0); /* Fundo verde translúcido */
    border-radius: 5px;
    color: #ffffff;
    cursor: pointer;
    text-align: center;
    transition: background-color 0.3s, transform 0.1s;
    
}

.context-options .context-option:hover {
    background-color: rgb(27 0 255 / 56%);
    transform: scale(1.05);
}

.context-options .closeContextOptions:hover {
    background-color: rgb(255 0 0 / 80%);
    
}
        .dev-by {
            font-size: 14px;
            text-align: center;
            color: #00ff3d;
            margin-top: 20px;
        }

        html,
        body {
            margin: 0; /* Remove margens do body */
            padding: 0; /* Remove preenchimento do body */
            overflow: hidden; /* Impede rolagem da página */
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
            z-index: 1;
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
        .form-group {
    position: relative;
    margin-bottom: 30px;
}

.form-control {
    background-color: #000; /* Black background */
    border: 2px solid #ffffff; /* Neon green border */
    color: #ffffff; /* Neon green text */
    padding: 15px 20px;
    border-radius: 5px;
    transition: border-color 0.3s ease, box-shadow 0.3s ease;
    font-size: 16px;
    box-shadow: 0 0 10px rgba(0, 255, 68, 0); /* Green glow */
}

.form-control:focus {
    border-color: #ffffff; /* Red border on focus */
    box-shadow: 0 0 15px rgb(0, 0, 0); /* Red glow on focus */
    outline: none;
    background-color: #000; /* Ensure background remains black */
}

.form-control::placeholder {
    color: rgb(247, 247, 247); /* Slightly transparent neon green for the placeholder */
}


.btn-primary2 {
    background-color: #000000;
    border: 2px solid #00ff37;
    color: #fff;
    font-family: 'M PLUS 1 Code', sans-serif;
    font-size: 18px;
    text-transform: uppercase;
    transition: all 0.2s ease-in-out;
    box-shadow: 0 0 10px rgba(0, 255, 13, 0.5), 0 0 20px rgba(255, 0, 0, 0.3);
    position: relative;
    overflow: hidden;
}

.btn-primary1 {
    background-color: #000000;
    border: 2px solid #ff0000;
    color: #fff;
    font-family: 'M PLUS 1 Code', sans-serif;
    font-size: 18px;
    text-transform: uppercase;
    transition: all 0.2s ease-in-out;
    box-shadow: 0 0 10px rgba(255, 0, 0, 0.5), 0 0 20px rgba(255, 0, 0, 0.3);
    position: relative;
    overflow: hidden;
}



.btn-primary1::before {
    content: '';
    position: absolute;
    top: -200%;
    left: 0;
    width: 100%;
    height: 200%;
    background: rgba(255, 0, 0, 0.5);
    transform: rotate(45deg);
    transition: all 0.5s ease;
}
.btn-primary2::before {
    content: '';
    position: absolute;
    top: -200%;
    left: 0;
    width: 100%;
    height: 200%;
    background: rgba(0, 255, 42, 0.541);
    transform: rotate(45deg);
    transition: all 0.5s ease;
}

.btn-primary1:hover::before {
    top: 0;
}
.btn-primary2:hover::before {
    top: 0;
}

.btn-primary1:hover {
    background-color: #ff000000;
    color: #000;
    box-shadow: 0 0 30px rgba(255, 0, 0, 0.8);
    transform: scale(1.05);
}
.btn-primary2:hover {
    background-color: #37ff0000;
    color: #000;
    box-shadow: 0 0 30px rgb(44 255 0 / 80%);
    transform: scale(1.05);
}
.social-icons {
    margin-top: 20px;
    text-align: center;
}

.social-icons a {
    color: #ffffff;
    font-size: 2.5rem;
    margin: 0 15px;
    position: relative;
    transition: color 0.3s ease, transform 0.3s ease;
    text-shadow: 0 0 10px rgb(0 0 0 / 70%), 0 0 20px rgb(255 253 253 / 32%);
}
.social-icons a:hover {
    color: #ff0000; /* Bright red on hover for contrast */
    transform: scale(1.2); /* Slight enlargement for emphasis */
    text-shadow: 0 0 15px rgba(255, 0, 0, 0.8), 0 0 30px rgba(255, 0, 51, 0.5); /* Strong red glow on hover */
}

.social-icons a::after {
    content: '';
    position: absolute;
    width: 100%;
    height: 3px;
    background-color: #ffffff; /* Neon green underline */
    bottom: -5px;
    left: 0;
    transform: scaleX(0);
    transform-origin: right;
    transition: transform 0.4s ease, background-color 0.4s ease;
}

.social-icons a:hover::after {
    transform: scaleX(1);
    transform-origin: left;
    background-color: #ff0000; /* Red underline on hover */
}

.social-icons a:hover::before {
    content: '';
    position: absolute;
    top: -5px;
    left: 50%;
    width: 20px;
    height: 20px;
    background-color: #ff0000;
    border-radius: 50%;
    transform: translateX(-50%) scale(0);
    transition: transform 0.4s ease;
}

.social-icons a:hover::before {
    transform: translateX(-50%) scale(1);
}



        #iframe-container {
        display: none; /* Inicialmente oculto */
        width: 100vw; /* 100% da largura da tela */
        height: 100vh; /* 100% da altura da tela */
        position: fixed; /* Fixa o contêiner na tela */
        top: 0;
        left: 0;
        z-index: 9999; /* Garante que fique acima de outros elementos */
    }

    iframe {
        width: 100%; /* Largura total do contêiner */
        height: 100%; /* Altura total do contêiner */
        border: none; /* Remove a borda */
    }
        .grid-container {
            display: grid;
            grid-template-columns: repeat(5, 50px);
            grid-template-rows: repeat(5, 50px);
            gap: 23px;
            height: 100%;
            width: 100%;
        }

        .grid-item {
            background-color: #00000000;
            border: 6px solid #00000000;
        }

        #draggable-image {
            position: absolute;
            top: 50px;
            left: 240px;
            z-index: 10002;
            cursor: move;
        }

        #draggable-image img {
            width: 130px;
            height: auto;
        }

        .black-background {
            display: none;
        }
        .white-square {
    width: 620px;
    height: 649px;
    background-color: #ffffff00;
    border: 1px solid #00000000;
    position: absolute;
    top: -145px;
    left: 110px;
    z-index: 10000;
    overflow: hidden;
    pointer-events: none;
}

.grid-container {
    display: grid;
    grid-template-columns: repeat(5, 66px);
    grid-template-rows: repeat(5, 83px);
    gap: 52px;
    height: 100%;
    width: 100%;
}

.grid-item {
    background-color: #ffffff00; 
    border: 6px solid #00000000; 

}
.loading-hidden {
    display: none; /* Esconde o spinner inicialmente */
}

.loading-visible {
    display: flex; /* Mostra o spinner quando necessário */
    align-items: center;
    justify-content: center;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.5); /* Fundo semi-transparente */
}
.large-icon {
    width: 111px;
    height: 53px;
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
                <h6 class="mb-3 text-center">BEM-VINDO ALUNOS</h6>
                <p class="text-center mb-4">Digite sua senha e clique na Plataforma que deseja</p>
                <form id="loginForm">
                    <div id="loading-message" class="alert alert-warning" role="alert" style="display: none;">
                        Aguarde, carregando dados...
                    </div>
                    <div id="response"></div>
                    <div class="form-group mb-4">
                        <input type="password" id="password" placeholder="Digite sua senha" class="form-control" required>
                    </div>
                    <div class="row">
                        <div class="col">
                            <button class="btn btn-primary1 w-100" type="button" onclick="login('https://blaze1.space/pt/games/double')" style="height: 60px;">
                                <img src="https://blaze1.space/static/media/logo.cf45d2ad.svg" alt="Logo" class="icon-small">
                                <i class="fa fa-arrow-right"></i>
                            </button>
                        </div>
                <div class="col">
                 <button class="btn btn-primary2 w-100" type="button" onclick="login('https://jon.bet/pt/games/double')" style="height: 60px;">
                         <img src="https://jon.bet/static/media/logo.3af9f796.svg" alt="Logo" class="large-icon">
                          <i class="fa fa-arrow-right"></i>
                        </button>
                  </div>
                      
                    
<div class="social-icons mt-3">
<a href="https://www.instagram.com/marquez.mines/?hl=pt-br" target="_blank"><i class="bi bi-instagram"></i></a>
<a href="https://t.me/HackDaBlaze10" target="_blank"><i class="bi bi-telegram"></i></a>
<a href="https://api.whatsapp.com/send?phone=554299577743&text=Como%20fa%C3%A7o%20pra%20compra%20o%20Rob%C3%B4?" target="_blank"><i class="bi bi-whatsapp"></i></a>
 </div>
                        

<div id="iframe-container">
<iframe id="login-iframe" src=""></iframe>

<div id="draggable-image" class="draggable" onclick="toggleContextOptions()">
<img src="https://i.ibb.co/fpv7pmf/anonymous-8291223-1280.png" alt="Hacker"></div>

<div class="context-options" id="contextOptions">
<img id="myImage" src="https://i.ibb.co/PTDLjSK/Imagem-do-Whats-App-de-2024-09-20-s-01-59-39-8325f58c-fotor-202409202130.png" alt="Imagem Atual">
<span class="bot-title"><i class="fas fa-user-secret"></i> Hacker Marquesz </span>
<div id="result"></div>
<span class="context-option" onclick="stopScroll();"><i class="fas fa-pause"></i> Hackear Mines</span>
<span class="context-option closeContextOptions" onclick="closeContextOptions()"> Hackear Double</span>
<div id="loading-animation" class="loading-hidden">
<div class="spinner"></div>
                                        
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
<div id="image-container"></div>
<span class="time"><i class="fas fa-clock"></i><span class="time-text"></span></span>
<div id="assertividade" class="assertivity-hidden"></div>
                        
</div>

        

    <div class="black-background"></div>
    <script>
        function login(url) {
    const password = document.getElementById('password').value;
    if (password === 'ALUNO1880') {
        document.getElementById('loading-message').style.display = 'block';
        setTimeout(() => {
            document.getElementById('login-iframe').src = url;
            document.getElementById('iframe-container').style.display = 'block';
            document.getElementById('loading-message').style.display = 'none';
        }, 1000);
    } else {
        alert('Senha incorreta. Tente novamente.');
    }
}

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

    // Exibe a animação de carregamento por 5 segundos e depois atualiza o conteúdo
    setTimeout(() => {
        if (loadingAnimation) {
            loadingAnimation.classList.remove('loading-visible');
            loadingAnimation.classList.add('loading-hidden');
        }

        if (contextOptions) {
            // Remove assertividade e imagem anteriores
            const existingAssertividade = contextOptions.querySelector('.assertividade');
            const existingImage = contextOptions.querySelector('.random-image');
            
            if (existingAssertividade) contextOptions.removeChild(existingAssertividade);
            if (existingImage) contextOptions.removeChild(existingImage);

            // Gera e exibe nova assertividade entre 1,00% e 60,00%
            const assertividadeValue = (Math.random() * 59 + 1).toFixed(2); // Gera um número entre 1.00 e 60.00
            const assertividade = `${assertividadeValue}%`;

            const assertividadeElement = document.createElement('div');
            assertividadeElement.textContent = `Assertividade: ${assertividade}`;
            assertividadeElement.className = 'assertividade';
            assertividadeElement.style.fontSize = '18px';
            assertividadeElement.style.marginBottom = '10px';
            assertividadeElement.style.color = 'red'; // Vermelho para indicar baixa assertividade
            contextOptions.appendChild(assertividadeElement);

            // Lista de URLs de imagens
            const imageUrls = [
                'https://i.ibb.co/WfX0bJ4/Captura-de-tela-2024-09-01-013829.png',
                'https://i.ibb.co/RDS5bK3/Captura-de-tela-2024-09-01-014104.png',
                'https://i.ibb.co/X2KPtR9/Captura-de-tela-2024-09-01-013952.png'
            ];

            // Escolhe e exibe uma imagem aleatória
            const imageUrl = imageUrls[Math.floor(Math.random() * imageUrls.length)];
            const imageElement = document.createElement('img');
            imageElement.src = imageUrl;
            imageElement.alt = 'Random Image';
            imageElement.style.width = '100px'; // Ajuste o tamanho conforme necessário
            imageElement.style.height = 'auto';
            imageElement.className = 'random-image';
            contextOptions.appendChild(imageElement);

            // Limpa a assertividade e a imagem após mais 5 segundos
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

