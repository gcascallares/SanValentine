<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="icon" href="corazon.png" type="image/png">
    <title>Feliz San Valentín</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <style>
        body {
            background-color: pink;
            text-align: center;
            overflow: hidden;
            overflow-y: auto;  /* Permitir el desplazamiento vertical */
            min-height: 100vh;  /* Asegura que el contenido ocupe al menos toda la altura de la pantalla */
    display: flex;
    flex-direction: column;
    margin: 0;
        }
        .heart {
            position: absolute;
            color: red;
            font-size: 24px;
            animation: float 5s linear infinite;
        }
        main {
            flex: 1;  /* El contenido principal toma el espacio restante */
        }
        @keyframes float {
            0% { transform: translateY(100vh) scale(1); opacity: 1; }
            100% { transform: translateY(-30vh) scale(1.5); opacity: 0; }
        }
        .envelope-container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 15px;
            margin-top: 20px;
        }
        .envelope {
            width: 120px;
            cursor: pointer;
            transition: transform 0.5s;
            animation: bounce 2s infinite;
        }
        .envelope:hover {
            transform: scale(1.1);
        }
        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }
        /* .message {
            display: none;
            margin-top: 20px;
            animation: fadeIn 1s;
        }
        .message img, .message video, .message p {
            width: 100%;
            max-width: 300px;
            animation: floatImage 3s infinite alternate;
        } */
        .message {
    display: none;  /* Mantener ocultos por defecto */
    margin-top: 10px;
    animation: fadeIn 1s;
    max-width: 100%;
    padding: 15px;  /* Espacio interno */
    border: 2px solid #ff69b4;  /* Borde rosado */
    border-radius: 10px;  /* Esquinas redondeadas */
    background-color: white;  /* Fondo blanco para destacar */
    box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);  /* Sombra suave */
}

.message img, .message video {
    width: 100%;
    max-width: 300px;  /* Tamaño máximo de la imagen o video */
    margin: 0 auto;  /* Centrar la imagen o video */
}

.message p {
    text-align: center;  /* Centrar el texto */
    font-size: 18px;  /* Tamaño de texto */
    color: #333;  /* Color del texto */
}
.message video {
    width: 100%;
    max-width: 100%;  /* Asegura que el video no se desborde */
    height: auto;  /* Mantener la proporción original */
    margin: 0 auto;  /* Centrar el video */
    max-height: 400px;  /* Establecer un límite en la altura para que no bloquee el desplazamiento */
}
        @keyframes fadeIn {
            0% { opacity: 0; }
            100% { opacity: 1; }
        }
        @keyframes floatImage {
            0% { transform: translateY(0); }
            100% { transform: translateY(-10px); }
        }
        .hidden {
            display: none;
        }
        #message-container * {
            display: block !important;
            opacity: 1 !important;
            visibility: visible !important;
            color: black !important; /* Para texto */
        }
        #carouselExample {
    border: 3px solid #ff69b4;  /* Borde rosado */
    border-radius: 15px;  /* Esquinas redondeadas */
    background-color: white;  /* Fondo blanco */
    box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);  /* Sombra suave */
    padding: 10px;  /* Espacio interno */
    margin-top: 20px;
}

.carousel-inner {
    border-radius: 10px;  /* Redondeo de las esquinas */
    overflow: hidden;  /* Para que las imágenes no se desborden del carrusel */
}

.carousel-item img {
    border-radius: 10px;  /* Redondeo de las esquinas de las imágenes */
    width: 100%;  /* Asegurarse de que las imágenes ocupen todo el ancho disponible */
    height: auto;  /* Mantener la proporción de las imágenes */
}
.footer {
    background-color: #ff69b4;  /* Fondo rosado */
    color: white;  /* Texto blanco */
    font-family: 'Arial', sans-serif;  /* Tipografía simple */
    text-align: center;  /* Centrado del texto */
    position: relative;
    bottom: 0;
    width: 100%;
    padding-top: 20px;
    padding-bottom: 20px;
}

.footer p {
    margin: 5px 0;  /* Espaciado entre las líneas */
}

.footer a {
    color: white;
    text-decoration: none;
}
.container {
    max-width: 100%;  /* Para asegurarse de que el contenido no se estire fuera de la pantalla */
    padding: 0 15px;
}
    </style>
</head>
<body>
    <main>
    <img src="titulo.png" alt="Feliz San Valentín" class="img-fluid mt-3">
    <button class="btn btn-danger mt-3" onclick="document.getElementById('music').play()">🎵 Reproducir música</button>
    
    <audio id="music" loop>
        <source src="Ke Personajes  Entre Beso y Beso.mp3" type="audio/mp3">
    </audio>
    
    <!-- Carrusel de Fotos -->
    <div id="carouselExample" class="carousel slide mt-4" data-bs-ride="carousel">
        <div class="carousel-inner">
            <div class="carousel-item">
                <img src="IMG_20241128_103409836_HDR.jpg" class="d-block w-50 mx-auto" alt="">
            </div>
            <div class="carousel-item active">
                <img src="IMG_20200208_192407248.jpg" class="d-block w-50 mx-auto" alt="">
            </div>
            <div class="carousel-item">
                <img src="IMG-20180128-WA0001.jpeg" class="d-block w-50 mx-auto" alt="">
            </div>
            <div class="carousel-item">
                <img src="IMG-20230706-WA0009.jpg" class="d-block w-50 mx-auto" alt="">
            </div>
        </div>
        <a class="carousel-control-prev" href="#carouselExample" role="button" data-bs-slide="prev">
            <span class="carousel-control-prev-icon" aria-hidden="true"></span>
            <span class="visually-hidden">Anterior</span>
        </a>
        <a class="carousel-control-next" href="#carouselExample" role="button" data-bs-slide="next">
            <span class="carousel-control-next-icon" aria-hidden="true"></span>
            <span class="visually-hidden">Siguiente</span>
        </a>
    </div>
    
    <!-- Sobres interactivos -->
    <div class="envelope-container">
        <img src="regalo.png" class="envelope" onclick="showMessage(0)" alt="Sobre 1">
        <img src="regalo.png" class="envelope" onclick="showMessage(1)" alt="Sobre 2">
        <img src="regalo.png" class="envelope" onclick="showMessage(2)" alt="Sobre 3">
        <img src="regalo.png" class="envelope" onclick="showMessage(3)" alt="Sobre 4">
        <img src="regalo.png" class="envelope" onclick="showMessage(4)" alt="Sobre 5">
        <img src="regalo.png" class="envelope" onclick="showMessage(5)" alt="Sobre 6">
    </div>
    
    <div id="messages">
        <div class="message hidden"><img src="mjs.png" alt=""></div>
        <div class="message hidden"><img src="20181117_225438-ANIMATION.gif" alt=""></div>
        <div class="message hidden"><img src="IMG_20241128_121719026_HDR.jpg" alt=""></div>
        <div class="message hidden"><video controls><source src="VID_20241126_234611497~3.mp4" type="video/mp4"></video></div>
        <div class="message hidden"><p>Que decirte que no sepas poolita, muchas gracias por estar a mi lado, gracias por siempre acompañarme en esta vida, por la hermosa familia que formamos juntos y ser mi compañera tanto en las buenas como en las malas(que fueron mayoria jajajaja)❤️</p></div>
        <div class="message hidden"><p>Ya lo dije una vez, pero quiero estar con vos la vida entera, aun nose porque elejiste estar conmigo, porque mucho no tenia para ofrecer, pero aunque nunca lo dije me comprometi a convertirme en un gran hombre, uno del que puedas estar orgullosa, un hombre que pueda darte todo lo que mereces y mucho mas, si algo tiene este mundo ese algo yo lo voy a tomar para regalartelo, y si hoy te pido que seas mi esposa es porque creo que lo estoy logrando ❤️</p></div>
    </div>

    
    <div id="message-container" class="message-container"></div>    
    <script>
        function showMessage(index) {
            const messages = document.querySelectorAll(".message");
            const messageContainer = document.getElementById("message-container");
            messageContainer.innerHTML = "";
            const selectedMessage = messages[index].cloneNode(true); 
            selectedMessage.classList.remove("hidden"); 
            messageContainer.appendChild(selectedMessage); 
        }
        function createHeart() {
            const heart = document.createElement("div");
            heart.classList.add("heart");
            heart.style.left = Math.random() * 100 + "vw";
            heart.style.animationDuration = Math.random() * 2 + 3 + "s";
            heart.innerHTML = "❤️";
            document.body.appendChild(heart);
            setTimeout(() => heart.remove(), 5000);
        }
        setInterval(createHeart, 500);
    </script>
    
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
</main>
        <!-- Footer -->
    <footer class="footer mt-5 pt-4 pb-4">
        <div class="container text-center">
            <p class="m-0" style="font-size: 16px;">❤️ ¡Gracias por visitar Pooli! ❤️</p>
            <p class="m-0" style="font-size: 14px;">Creado con amor San Valentín de mi parte Gabrielito.</p>
        </div>
    </footer>
</body>
</html>
