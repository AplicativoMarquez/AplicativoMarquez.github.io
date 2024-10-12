<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login</title>
    <style>
        body, html {
            margin: 0;
            padding: 0;
            height: 100%;
            overflow: hidden;
        }
        .video-background {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            overflow: hidden;
        }
        video {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        .login-container {
            position: relative;
            z-index: 1;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100%;
            color: white;
            text-align: center;
        }
        .login-form {
            background: rgba(0, 0, 0, 0.5);
            padding: 20px;
            border-radius: 10px;
        }
    </style>
</head>
<body>
    <div class="video-background">
        <video autoplay muted loop>
            <source src="https://cdn.pixabay.com/video/2020/08/21/47802-451812879_large.mp4" type="video/mp4">
            Seu navegador não suporta o elemento de vídeo.
        </video>
    </div>
    <div class="login-container">
        <div class="login-form">
            <h1>Login</h1>
            <form>
                <input type="text" placeholder="Usuário" required>
                <input type="password" placeholder="Senha" required>
                <button type="submit">Entrar</button>
            </form>
        </div>
    </div>
</body>
</html>
