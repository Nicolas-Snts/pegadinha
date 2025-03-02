<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>hack bank.Roubo</title>
    <style>
        body {
            background-color: black;
            color: #00FF00;
            font-family: 'Courier New', Courier, monospace;
            font-size: 20px;
            overflow: hidden;
            margin: 0;
            padding: 0;
        }
        .line {
            display: block;
        }
        #message {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            font-size: 28px;
            color: red;
            font-weight: bold;
            text-align: center;
            background-color: black; /* Fundo 100% preto */
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 20px rgba(255, 0, 0, 0.8); /* Sombras para destacar */
        }
    </style>
</head>
<body>
    <div id="hack-effect"></div>
    <div id="message"></div>

    <script>
        var lineElement = document.getElementById("hack-effect");
        var messageElement = document.getElementById("message");

        // Função para gerar caracteres aleatórios
        function randomChar() {
            var chars = "ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789!@#$%^&*()_+[]{}|;:,.<>?";
            return chars.charAt(Math.floor(Math.random() * chars.length));
        }

        // Função para simular o efeito de código maluco
        function generateRandomCode() {
            var randomCode = "";
            for (var i = 0; i < 100; i++) {
                randomCode += randomChar();
            }
            return randomCode;
        }

        var lineIndex = 0;
        
        function printLine() {
            if (lineIndex < 20) { // Número de linhas que aparecerão
                var newLine = document.createElement("div");
                newLine.className = "line";
                newLine.innerText = generateRandomCode(); // Texto aleatório
                lineElement.appendChild(newLine);
                lineIndex++;
            } else {
                lineIndex = 0;
                lineElement.innerHTML = ''; // Limpa as linhas para reiniciar
                showMessage();
            }
        }

        function showMessage() {
            messageElement.innerText = "Malware 'Cavalo de Troia for Strong Grip' executado com sucesso! Acessar/executar: roubo.nubank roubo.inter roubo.pagbank chamar: TRANFERENCIA_imediata conta exterior";
        }

        // Chama a função de gerar código aleatório rapidamente
        setInterval(printLine, 50); // Aumente a velocidade para deixar mais rápido
    </script>
</body>
</html>
