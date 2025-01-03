# Cuento-Roc-o
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cuento de Rocío</title>
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
    <style>
        body {
            font-family: 'Comic Sans MS', cursive;
            background-color: #f9f9f9;
        }
        .page {
            display: none;
        }
        .page.active {
            display: block;
        }
        .book {
            perspective: 1000px;
        }
        .book-page {
            transition: transform 0.6s;
            transform-style: preserve-3d;
            position: relative;
        }
        .book-page img {
            max-width: 100%;
            border-radius: 10px;
        }
        .turn {
            display: inline-block;
            cursor: pointer;
            user-select: none;
        }
        .turn:hover {
            color: #3182ce;
        }
    </style>
</head>
<body class="flex items-center justify-center min-h-screen">
    <div class="container mx-auto p-4">
        <h1 class="text-3xl font-bold text-center mb-6">Cuento de Rocío</h1>
        <div id="book" class="book bg-white shadow-xl rounded-lg p-4">
            <div id="page1" class="page active">
                <img src="/attachments/6smVWWXLkfwkBgzMVewgB.jpeg" alt="Introducción: Rocío y sus amigos favoritos">
                <p class="mt-4 text-lg">Había una vez una niña llamada Rocío. Era una niña muy curiosa y alegre, ¡y hoy estaba llena de emoción! Rocío tenía muchos amigos especiales. Entre ellos estaban los valientes perros de la Patrulla Canina, el juguetón perro Bluey y Bartolito el gallo, quien siempre la hacía reír con su "quiquiriquí".</p>
            </div>
            <div id="page2" class="page">
                <img src="image2.jpg" alt="Un día especial en el parque">
                <p class="mt-4 text-lg">Un día soleado, Rocío y sus amigos decidieron ir al parque. El parque estaba lleno de árboles altos, flores de todos los colores y muchos animales amigables. Rocío corría y reía mientras jugaba con los perros de la Patrulla Canina, Bluey y Bartolito. Todos juntos disfrutaban de un día perfecto bajo el sol.</p>
            </div>
            <div id="page3" class="page">
                <img src="image3.jpg" alt="Una aventura inesperada">
                <p class="mt-4 text-lg">Mientras jugaban, Rocío y sus amigos encontraron un sendero misterioso escondido entre los arbustos. Rocío, siempre aventurera, sugirió seguir el sendero para ver a dónde los llevaría. Los perros de la Patrulla Canina, Bluey y Bartolito estaban de acuerdo, y juntos comenzaron a caminar por el sendero.</p>
            </div>
            <div id="page4" class="page">
                <img src="image4.jpg" alt="El encuentro con un nuevo amigo">
                <p class="mt-4 text-lg">Al final del sendero, Rocío y sus amigos encontraron a un animal mágico. Era un pequeño unicornio que parecía preocupado. El unicornio les contó que había perdido su camino y necesitaba ayuda para regresar a casa. Rocío y sus amigos decidieron ayudarlo de inmediato. ¡Sería una nueva aventura para todos!</p>
            </div>
        </div>
        <div class="flex justify-between mt-6">
            <span id="prev" class="turn text-2xl">&larr; Anterior</span>
            <span id="next" class="turn text-2xl">Siguiente &rarr;</span>
        </div>
    </div>
    <script>
        const pages = document.querySelectorAll('.page');
        let currentPage = 0;
        
        document.getElementById('next').addEventListener('click', () => {
            if (currentPage < pages.length - 1) {
                pages[currentPage].classList.remove('active');
                currentPage++;
                pages[currentPage].classList.add('active');
            }
        });
        
        document.getElementById('prev').addEventListener('click', () => {
            if (current
