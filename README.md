<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Una Carta para Ti</title>
    <style>
        body {
            background-color: #2E8B57;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            font-family: 'Arial', sans-serif;
            color: white;
            text-align: center;
            overflow: hidden;
        }
        .sobre-container {
            position: relative;
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
        }
        .sobre {
            width: 150px;
            height: 100px;
            background: #D4AF37;
            cursor: pointer;
            display: flex;
            justify-content: center;
            align-items: center;
            border-radius: 5px;
            position: relative;
            animation: latir 1.5s infinite alternate;
            font-size: 1.2em;
            font-weight: bold;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.3);
        }
        @keyframes latir {
            from {
                transform: scale(1);
            }
            to {
                transform: scale(1.1);
            }
        }
        .carta {
            display: none;
            background: #FFF;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 0 15px rgba(0, 0, 0, 0.5);
            max-width: 600px;
            font-size: 1.2em;
            line-height: 1.6;
            color: black;
            text-align: left;
            overflow-y: auto;
            max-height: 80vh;
            position: relative;
        }
        .texto {
            display: none;
            font-family: 'Arial', sans-serif;
            font-size: 1.3em;
            margin-bottom: 10px;
        }
        .flores {
            margin-top: 20px;
            font-size: 2em;
            text-align: center;
            animation: florecer 2s ease-in-out infinite alternate;
        }
        @keyframes florecer {
            from { transform: scale(1); }
            to { transform: scale(1.2); }
        }
    </style>
    <script>
        function abrirCarta() {
            document.querySelector('.sobre-container').style.display = 'none';
            const carta = document.querySelector('.carta');
            carta.style.display = 'block';
            mostrarTexto(0);
        }
        function mostrarTexto(index) {
            const partes = document.querySelectorAll('.texto');
            if (index < partes.length) {
                partes[index].style.display = 'block';
                partes[index].scrollIntoView({ behavior: 'smooth', block: 'end' });
                setTimeout(() => mostrarTexto(index + 1), 2000);
            }
        }
    </script>
</head>
<body>
    <div class="sobre-container">
        <div class="sobre" onclick="abrirCarta()">📩 Presiona para abrir</div>
    </div>
    <div class="carta">
        <p class="texto">Holiiii, soy Mel, sorpresa!!</p>
        <p class="texto">No sé exactamente cómo empezar esto, pero quiero decirte algo que quizás no menciono lo suficiente o tal vez sí jajaj pero igual, gracias.</p>
        <p class="texto">Gracias por cada conversación, por tu tiempo, por ser como eres. A veces la vida nos pone caminos inciertos, momentos de dudas y retos que parecen demasiado grandes. Pero si hay alguien capaz de superarlos, eres tú.</p>
        <p class="texto">Tienes más fuerza de la que crees, más luz de la que imaginas. A veces el camino se siente pesado, lo sé, pero recuerda que cada paso que das, incluso los pequeños, cuentan. No tienes que correr todo el tiempo, a veces solo hace falta respirar y seguir.</p>
        <p class="texto">Quiero que sepas que hay muchas cosas para admirar de ti. Que aunque las palabras a veces no alcancen, aquí estoy para recordarte que vales, que eres increíble y que mereces todo lo bueno que venga.</p>
        <p class="texto">Hoy, en este Día de San Valentín y de la Amistad, quiero que recibas un poquito de ese cariño que el mundo tiene para ti. No sé qué nos depara el destino, pero sí sé que deseo que encuentres la felicidad en cada rincón, en cada día, en cada pequeña victoria.</p>
        <p class="texto">Ánimo, sigue adelante. Estoy segura de que puedes con todo.</p>
        <p class="texto">Feliz día pichurriiiis💚🌟 💚🌟</p>
        <p class="texto">PD: Chocalas choooocalas jajaja :D</p>
        <div class="flores">💙🌸💙🌸💙</div>
    </div>
</body>
</html>
