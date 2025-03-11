<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jardim do Boneco</title>
    <style>
        body { text-align: center; font-family: Arial, sans-serif; }
        #game-container { margin-top: 20px; }
        #boneco { font-size: 50px; }
        #planta { display: none; font-size: 40px; }
        button { padding: 10px; font-size: 16px; margin: 10px; cursor: pointer; }
    </style>
</head>
<body>
    <h1>Jardim do Boneco</h1>
    <p id="game-text">Clique no botão para começar!</p>
    <div id="game-container">
        <p id="boneco">🤖</p>
        <p id="planta">🌱</p>
    </div>
    <button onclick="proximaAcao()">Avançar</button>

    <script>
        let etapa = 0;

        function proximaAcao() {
            const texto = document.getElementById("game-text");
            const boneco = document.getElementById("boneco");
            const planta = document.getElementById("planta");

            etapa++;
            switch (etapa) {
                case 1:
                    texto.innerText = "O boneco anda.";
                    break;
                case 2:
                    texto.innerText = "O boneco encontra uma semente.";
                    break;
                case 3:
                    texto.innerText = "O boneco enterra a semente.";
                    planta.style.display = "inline";
                    planta.innerText = "🌱 (semente enterrada)";
                    break;
                case 4:
                    texto.innerText = "O boneco anda mais um pouco.";
                    break;
                case 5:
                    texto.innerText = "O boneco encontra um regador.";
                    break;
                case 6:
                    texto.innerText = "O boneco rega a semente.";
                    planta.innerText = "🌿 (regada)";
                    break;
                case 7:
                    texto.innerText = "A planta cresce!";
                    planta.innerText = "🌳";
                    break;
                case 8:
                    texto.innerText = "O boneco abraça a planta.";
                    boneco.innerText = "🤗";
                    break;
                default:
                    texto.innerText = "A história terminou!";
                    break;
            }
        }
    </script>
</body>
</html>
