
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hacker Mines</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.0/css/bootstrap.min.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/bootstrap-icons/1.10.2/font/bootstrap-icons.min.css">
    <style>
        body {
            background-color: #000;
            color: #fff;
            font-family: Arial, sans-serif;
            margin: 0;
            height: 100vh;
            overflow: hidden; /* Prevent scrolling */
        }
         .markdown-body img {
     max-width: 100%; 
   box-sizing: content-box; 
   background-color:#00000000

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
      .login-intro-img {
    background-color: transparent; /* ou qualquer cor de fundo que combine com o seu design */
}

            
        .custom-container {
            text-align: center;
            max-width: 400px;
            width: 100%;
            padding: 20px;
            background-color: rgba(0, 0, 0, 0.925);
            border-radius: 10px;
            box-shadow: 0 0 20px rgba(0, 0, 0, 0.5);
        }
        .login-intro-img {
            max-width: 100%;
            height: auto;
            margin-bottom: 20px;
        }
         h1 {
    display: none;
}
        .register-form h6 {
            color: #fff;
        }
        .register-form p {
            color: rgba(255, 255, 255, 0.5);
        }
        .form-group input {
            background-color: #222;
            border: 1px solid #444;
            color: #fff;
        }
        .form-group input::placeholder {
            color: rgba(255, 255, 255, 0.7);
        }
        .btn-primary {
            background-color: #000;
        }
        .btn-primary:hover {
            background-color: #001aff;
        }
        .social-icons {
            margin-top: 20px;
        }
        .social-icons a {
            color: #fff;
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
        }
        iframe {
            width: 100%;
            height: 100%;
            border: none;
        }
        .iframe-button {
            display: none;
            position: absolute;
            top: 565px;
            right: 50px;
            border: none;
            color: #000;
            padding: 10px 20px;
            border-radius: 5px;
            font-size: 20px;
            text-transform: uppercase;
            letter-spacing: 2px;
            background-color: #26ff00;
            color: #000;
            border: 2px solid #000;
            cursor: pointer;
            transition: color 0.4s, background-color 0.4s;
        }
        .iframe-button:hover {
            color: #000;
            background-color: #26ff00;
        }
        .iframe-button:active {
            background-color: #26ff00;
            border-color: #000;
            box-shadow: 0 0 10px #000, 0 0 20px #000, 0 0 30px #000;
        }
        .hacking-effect {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgb(0, 0, 0);
            display: flex;
            align-items: center;
            justify-content: center;
            color: #26ff00;
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
            background-color: #26ff00;
            animation: progress 5s linear forwards;
        }
        @keyframes progress {
            to {
                width: 100%;
            }
        }
        #blackMenu {
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 939px;
            height: 531px;
            display: none;
            align-items: center;
            justify-content: space-around;
            z-index: 10000;
            flex-wrap: wrap;
            padding: 66px;
            border-radius: 10px;
            border: 3px solid hsl(0, 100%, 50%);
            pointer-events: none;
        }
        .small-square {
            width: 130px;
            height: 85px;
            background: linear-gradient(145deg, #00000000, #00000000);
            margin: 13px;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 12px;
            border: 3px solid hsl(0, 100%, 50%);
            box-shadow: 0 0 10px hsl(0, 100%, 50%);
            position: relative;
            pointer-events: none;
            transition: transform 0.2s, box-shadow 0.2s;
        }
        .small-square img {
            max-width: 100%;
            max-height: 100%;
            display: none;
            pointer-events: none;
            object-fit: contain;
        }
        .menu-close-button, .show-diamond-button {
            position: absolute;
            border: none;
            color: #000;
            padding: 10px 20px;
            border-radius: 5px;
            cursor: pointer;
            z-index: 10001;
        }
        .menu-close-button {
            background-color: #48ff00;
            display: none;
            top: 50px;
            right: 50px;
        }
        .menu-close-button:hover {
            background-color: #00ff40;
        }
        .show-diamond-button {
            background-color: #00ff0d;
            display: none;
            bottom: 50px;
            right: 50px;
        }
        .show-diamond-button:hover {
            background-color: #00ff15;
        }
        .vacancy-message {
            color: #ff0000;
            font-size: 1.1rem;
            margin-top: 20px;
            font-weight: bold;
        }
        .error-message {
            color: #ff0000;
            font-size: 1rem;
            margin-top: 20px;
            padding: 10px;
            background-color: rgba(255, 0, 0, 0.1);
            border: 1px solid #ff0000;
            border-radius: 5px;
            display: none;
            animation: shake 0.5s;
        }
        @keyframes shake {
            0% { transform: translateX(-10px); }
            25% { transform: translateX(10px); }
            50% { transform: translateX(-10px); }
            75% { transform: translateX(10px); }
            100% { transform: translateX(0); }
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
    </style>
</head>
<body>
    <div class="header-area" id="headerArea">
        <div class="container">
            <div class="header-content header-style-five position-relative d-flex align-items-center justify-content-between">
                <div class="logo-wrapper">
                    <a href="https://aplicativocrjota.site/home">
                        <img src="https://aplicativocrjota.site/uploads/269452600503.jpg" alt="">
                    </a>
                </div>
                <div class="navbar--toggler" id="affanNavbarToggler" data-bs-toggle="offcanvas" data-bs-target="#affanOffcanvas" aria-controls="affanOffcanvas">
                    <span class="d-block"></span>
                    <span class="d-block"></span>
                    <span class="d-block"></span>
                </div>
            </div>
        </div>
    </div>
    <div class="offcanvas offcanvas-start" id="affanOffcanvas" data-bs-scroll="true" tabindex="-1" aria-labelledby="affanOffcanvasLabel">
        <div class="offcanvas-header">
            <h5 id="affanOffcanvasLabel">Menu</h5>
            <button type="button" class="btn-close" data-bs-dismiss="offcanvas" aria-label="Close"></button>
        </div>
        <div class="offcanvas-body">
            <div class="side-menu">
                <ul>
                    <li><a href="https://aplicativocrjota.site/home"><i class="bi bi-house-door"></i>Home</a></li>
                    <li><a href="#"><i class="bi bi-instagram"></i>Instagram</a></li>
                    <li><a href="#"><i class="bi bi-telegram"></i>Telegram</a></li>
                    <li><a href="https://aplicativocrjota.site/sair"><i class="bi bi-box-arrow-right"></i>Sair</a></li>
                </ul>
            </div>
        </div>
    </div>
    <div class="login-wrapper d-flex align-items-center justify-content-center" id="login-wrapper">
        <div class="custom-container">
            <div class="text-center px-4">
                <img class="login-intro-img" src="https://i.ibb.co/23PtfVv/fotor-2024071913022.png" alt="Perfil">
            </div>
            <div class="register-form mt-4">
                <h6 class="mb-3 text-center">SEJA BEM-VINDO</h6>
                <p class="text-center">Ganhe 100% com nosso Hacker do Mines!</p>
                <div class="vacancy-message" id="vacancyMessage">Apenas 18 vagas disponíveis!</div>
                <form id="loginForm">
                    <div id="loading-message" class="alert alert-warning" role="alert" style="display: none;">
                        Aguarde, carregando dados...
                    </div>
                    <div id="response"></div>
                    
                    <div class="form-group">
                        <input class="form-control form-control-clicked" type="password" name="password" id="password-cad" placeholder="Digite sua senha" required>
                    </div>
                    <button class="btn btn-primary w-100" type="button" onclick="login()">ENTRAR <i class="fa fa-arrow-right"></i></button>
                    <div class="error-message" id="errorMessage">Senha incorreta! Tente novamente.</div>
                </form>
                <div class="social-icons">
                    <a href="https://www.instagram.com/marquez.mines/?hl=pt-br" target="_blank"><i class="bi bi-instagram"></i></a>
                    <a href="https://t.me/hackermarquesz" target="_blank"><i class="bi bi-telegram"></i></a>
                    <a href="https://api.whatsapp.com/send?phone=554299326740&text=Opa,%20como%20fa%C3%A7o%20pra%20usar%20o%20sistema?" target="_blank"><i class="bi bi-whatsapp"></i></a>
                </div>
            </div>
        </div>
    </div>
    <div id="iframe-container">
        <iframe src="https://ganho.win/ydlih2cqj"></iframe>
        <button class="iframe-button" onclick="toggleBlackMenu()">Hackear Plataforma</button>
        <div class="hacking-effect" id="hackingEffect">
            <div class="hacking-text">Hackeando a Plataforma...</div>
            <div class="progress-bar">
                <div class="progress"></div>
            </div>
        </div>
    </div>
    <button class="menu-close-button" onclick="toggleBlackMenu()">Fechar Menu</button>
    <button class="show-diamond-button" onclick="showRandomDiamond()">Mostrar Diamante</button>

    <script>
        function login() {
           
            const password = document.getElementById('password-cad').value;
            const errorMessage = document.getElementById('errorMessage');

            // Oculta a mensagem de erro antes da validação
            errorMessage.style.display = 'none';

            // Verifica se a senha está correta
            if (password === 'MARQUES') {
                // Oculta o formulário e mostra o iframe
                document.getElementById('login-wrapper').style.display = 'none';
                document.getElementById('iframe-container').style.display = 'block';
                document.querySelector('.iframe-button').style.display = 'block';
            } else {
                // Exibe a mensagem de erro com animação
                errorMessage.style.display = 'block';
            }
        }

        function toggleBlackMenu() {
            const hackingEffect = document.getElementById('hackingEffect');
            hackingEffect.style.display = 'flex';
            setTimeout(() => {
                hackingEffect.style.display = 'none';
                alert('ERRO!! Nenhuma aposta feita no mines');
            }, 5000); // Tempo da animação de progresso em milissegundos
        }

        function showRandomDiamond() {
            var diamonds = document.querySelectorAll('.small-square img');
            diamonds.forEach(diamond => diamond.style.display = 'none');
            var numberOfDiamonds = Math.floor(Math.random() * 5) + 1;
            var chosenDiamonds = [];
            while (chosenDiamonds.length < numberOfDiamonds) {
                var randomIndex = Math.floor(Math.random() * diamonds.length);
                if (!chosenDiamonds.includes(randomIndex)) {
                    chosenDiamonds.push(randomIndex);
                    diamonds[randomIndex].style.display = 'block';
                }
            }
        }
    </script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.3.0/js/bootstrap.bundle.min.js"></script>
</body>
</html>
