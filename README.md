<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Feliz Mêsversário de Namoro</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            background: linear-gradient(135deg, #ff9a9e 0%, #fecfef 100%);
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            text-align: center;
        }

        .form-container, .content-container {
            display: none;
            width: 90%;
            max-width: 600px;
            background-color: rgba(255, 255, 255, 0.2);
            border-radius: 15px;
            padding: 20px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }

        .form-container.active, .content-container.active {
            display: block;
        }

        h1 {
            font-size: 2.5em;
            margin-bottom: 20px;
            color: #fff;
        }

        h1 span {
            color: #ff6b6b;
        }

        input[type="text"] {
            padding: 10px;
            border-radius: 5px;
            border: none;
            width: 80%;
            margin-bottom: 20px;
            font-size: 1.1em;
        }

        button {
            padding: 10px 20px;
            background-color: #ff6b6b;
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 1.1em;
        }

        button:hover {
            background-color: #ff4b4b;
        }

        video {
            width: 100%;
            border-radius: 10px;
            margin-top: 20px;
        }

        @media (max-width: 600px) {
            h1 {
                font-size: 1.8em;
            }
        }
    </style>
</head>
<body>

    <!-- Formulário -->
    <div class="form-container active" id="form-container">
        <h1>Digite seu nome:</h1>
        <input type="text" id="name-input" placeholder="Seu nome">
        <button onclick="checkName()">Enviar</button>
    </div>

    <!-- Conteúdo principal -->
    <div class="content-container" id="content-container">
        <h1 id="message"></h1>
        <button onclick="showVideo()">Seguir</button>
    </div>

    <!-- Video e mensagem final -->
    <div class="content-container" id="video-container">
        <h1>Feliz Mêsversário de Namoro <span>❤️</span></h1>
        <video controls>
            <source src="video fofo.mp4" type="video/mp4">
            Seu navegador não suporta o vídeo.
        </video>
    </div>

    <script>
        function checkName() {
            var name = document.getElementById('name-input').value.toLowerCase();
            if (name === "leticia" || name === "leticia lucas") {
                document.getElementById('message').innerText = "Você é o Amor da vida do João e o Girassol dele 🌻";
                document.getElementById('form-container').classList.remove('active');
                document.getElementById('content-container').classList.add('active');
            } else {
                alert('Desculpe, você não tem acesso a este conteúdo.');
            }
        }

        function showVideo() {
            document.getElementById('content-container').classList.remove('active');
            document.getElementById('video-container').classList.add('active');
        }
    </script>

</body>
</html>
