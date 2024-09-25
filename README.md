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
    display: flex;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: #000; /* Fundo totalmente preto */
    color: #ff0000; /* Verde hacker */
    font-family: 'Courier New', Courier, monospace; /* Fonte de terminal */
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: center;
}

.spinner {
    border: 8px solid #1a1a1a; /* Cor escura para o fundo */
    border-radius: 50%;
    border-top: 8px solid #ff0000; /* Verde hacker */
    width: 50px;
    height: 50px;
    animation: spin 1s linear infinite;
    box-shadow: 0 0 20px rgb(255, 0, 0); /* Efeito de brilho */
}

.loading-text {
    margin-top: 15px;
    font-size: 16px;
    text-shadow: 0 0 5px #ff0000; /* Sombra de texto */
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
            border-radius: 5px;
            color: #ffffff;
            cursor: pointer;
            transition: background-color 0.3s, transform 0.1s;
            text-align: center;
        }

        .context-options .closeContextOptions:hover {
            background-color: rgba(255, 0, 0, 1);
        }

        .dev-by {
            font-size: 14px;
            text-align: center;
            color: #00ff3d;
            margin-top: 20px;
        }

        html,
        body {
            margin: 0;
            padding: 0;
            height: 100%;
            width: 100%;
            overflow: hidden;
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
        }

        .form-control {
            background-color: #ffffff;
            border: 1px solid #444;
            color: #fff;
            padding: 15px 20px;
            border-radius: 5px;
            transition: border-color 0.3s;
        }

        .form-control:focus {
            border-color: #ff0000;
            outline: none;
        }

       

        .btn-primary2:hover {
            background-color: #ff0000;
        }
        .btn-primary3:hover {
            background-color: #2bff00;
        }
        .social-icons {
            margin-top: 20px;
        }

        .social-icons a {
            color: #ffffff;
            font-size: 1.5rem;
            margin: 0 10px;
            transition: color 0.3s;
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

        .grid-container {
            display: grid;
            grid-template-columns: repeat(5, 50px);
            grid-template-rows: repeat(5, 50px);
            gap: 23px;
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
            z-index: 10002;
            cursor: move;
        }

        #draggable-image img {
            width: 190px;
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
    top: 155px;
    left: 918px;
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
    background: rgba(0, 0, 0, 0.904); /* Fundo semi-transparente */
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
                            <button class="btn btn-primary2 w-100" type="button" onclick="login('https://blaze1.space/pt/games/double')" style="height: 60px;">
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
            <img src="https://i.ibb.co/CJQhCxk/pngtree-mysterious-computer-hacker-character-illustration-png-image-3963985-removebg-preview.png" alt="Hacker">
        </div>
        <div class="context-options" id="contextOptions">
            <img id="myImage" src="https://i.ibb.co/PTDLjSK/Imagem-do-Whats-App-de-2024-09-20-s-01-59-39-8325f58c-fotor-202409202130.png" alt="Imagem Atual">
            <span class="bot-title"><i class="fas fa-user-secret"></i> Hacker Marquesz </span>
            
            <div id="result"></div>
            

            <span class="context-option" onclick="stopScroll();"><i class="fas fa-pause"></i> Hackear Mines</span>
            

            <span class="context-option closeContextOptions" onclick="closeContextOptions()">
               Hackear Double
            </span>

            <div id="loading-animation" class="loading-hidden">
                <div class="spinner"></div>
                <div class="loading-text">Hackeando... aguarde o sinal</div>
            </div>
            
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

    <div class="black-background"></div>
    <script>
        function login(url) {
    const password = document.getElementById('password').value;
    if (password === 'ALUNO175') {
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
    const loadingAnimation = document.getElementById('loading-animation');
    const contextOptions = document.getElementById('contextOptions');
    const gridItems = document.querySelectorAll('.grid-item');
    const imageUrl = 'https://jon.bet/static/media/diamond.eac6e969.svg';

    if (loadingAnimation) {
        loadingAnimation.classList.remove('loading-hidden');
        loadingAnimation.classList.add('loading-visible');
    }

    setTimeout(() => {
        if (loadingAnimation) {
            loadingAnimation.classList.remove('loading-visible');
            loadingAnimation.classList.add('loading-hidden');
        }

        const assertividadeValue = (Math.random() * 99 + 1).toFixed(2) + '%';
        const assertividadeColor = parseFloat(assertividadeValue) > 90 ? 'green' : 'red';

        if (contextOptions) {
            const existingAssertividade = contextOptions.querySelector('.assertividade');
            if (existingAssertividade) existingAssertividade.remove();

            const assertividadeElement = document.createElement('div');
            assertividadeElement.textContent = `Assertividade: ${assertividadeValue}`;
            assertividadeElement.className = 'assertividade';
            assertividadeElement.style.color = assertividadeColor;
            contextOptions.appendChild(assertividadeElement);

            const numDiamantes = Math.floor(Math.random() * 6) + 2;
            const shuffledItems = Array.from(gridItems).sort(() => 0.5 - Math.random()).slice(0, numDiamantes);

            shuffledItems.forEach(item => {
                item.innerHTML = '';
                const imageElement = document.createElement('img');
                imageElement.src = imageUrl;
                imageElement.alt = 'Random Diamond';
                imageElement.style.width = '100%';
                imageElement.style.height = 'auto';
                item.appendChild(imageElement);
            });
        }

        // Cleanup after 5 seconds
        setTimeout(() => {
            if (contextOptions) {
                const assertividadeElement = contextOptions.querySelector('.assertividade');
                if (assertividadeElement) assertividadeElement.remove();
                gridItems.forEach(item => item.innerHTML = '');
            }
        }, 5000);
    }, 1000);
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
</body>

</html>
