<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hacker_TV</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            color: #f4f4f4;
            text-align: center;
            margin: 0;
            padding: 0;
            overflow-x: hidden; /* Чтобы предотвратить горизонтальную прокрутку */
            background-color: #111; /* Темный фон для контраста */
        }

        h1 {
            font-size: 2.5em;
            margin-top: 20px;
            color: #fff;
            text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.7);
        }

        .slideshow-container {
            position: relative;
            width: 100%;
            max-width: 800px;
            margin: auto;
            overflow: hidden;
            margin-top: 30px;
            border-radius: 15px; /* Скругленные углы для слайд-шоу */
        }

        .video-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 20px;
            justify-items: center;
            margin-top: 20px;
        }

        .video {
            display: none; /* Скрыть все видео по умолчанию */
            width: 100%;
            height: auto;
            max-width: 320px;
            height: 180px;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.3);
            opacity: 0; /* Скрываем видео изначально */
            animation: fadeIn 1s forwards; /* Анимация плавного появления */
        }

        .active {
            display: block; /* Показать текущее видео */
            animation: fade 1s;
        }

        /* На каждый видео элемент будет назначена задержка анимации */
        .video:nth-child(1) { animation-delay: 0s; }
        .video:nth-child(2) { animation-delay: 0.5s; }
        .video:nth-child(3) { animation-delay: 1s; }
        .video:nth-child(4) { animation-delay: 1.5s; }
        .video:nth-child(5) { animation-delay: 2s; }
        .video:nth-child(6) { animation-delay: 2.5s; }

        iframe {
            width: 100%;
            height: 100%;
            border: none;
            border-radius: 10px;
        }

        /* Стиль для фона видео */
        .background-video {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            object-fit: cover;
            z-index: -1; /* Видео на фоне */
        }

        .button {
            background-color: #3a3a3a;
            color: #fff;
            padding: 15px 30px;
            margin: 10px;
            border-radius: 30px;
            text-decoration: none;
            display: inline-block;
            font-size: 1.2em;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
            transition: background-color 0.3s, transform 0.3s, box-shadow 0.3s;
        }

        .button:hover {
            background-color: #0066cc;
            transform: scale(1.05);
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.4);
        }

        /* Эффект для кнопок */
        .buttons {
            margin-top: 20px;
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        @keyframes fade {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        /* Скроллинг страницы */
        .scrollable-content {
            max-height: 80vh;
            overflow-y: auto;
            padding: 20px;
            margin-top: 30px;
            border-radius: 10px;
            background-color: rgba(0, 0, 0, 0.5);
        }

        /* Эффект для кнопок при наведении */
        .button:active {
            transform: scale(0.98);
        }

    </style>
</head>
<body>
    <h1>Hacker_TV</h1>
    <div class="slideshow-container">
        <video class="video active" loop muted>
            <source src="video1.mp4" type="video/mp4">
            Ваш браузер не поддерживает видео.
        </video>
        <video class="video">
            <source src="video2.mp4" type="video/mp4">
            Ваш браузер не поддерживает видео.
        </video>
        <video class="video">
            <source src="video3.mp4" type="video/mp4">
            Ваш браузер не поддерживает видео.
        </video>
        <video class="video">
            <source src="video4.mp4" type="video/mp4">
            Ваш браузер не поддерживает видео.
        </video>
    </div>

    <video class="background-video" autoplay muted loop>
        <source src="https://cdn.pixabay.com/video/2018/01/27/13949-253035804_large.mp4" type="video/mp4">
    </video>

    <script>
        let currentIndex = 0;
        const videos = document.querySelectorAll('.video');

        function showVideo(index) {
            videos.forEach((video, i) => {
                video.classList.remove('active');
                if (i === index) {
                    video.classList.add('active');
                    video.play(); // Воспроизводим текущее видео
                } else {
                    video.pause(); // Останавливаем остальные видео
                }
            });
        }

        function nextVideo() {
            currentIndex = (currentIndex + 1) % videos.length;
            showVideo(currentIndex);
        }

        setInterval(nextVideo, 5000); // Меняйте видео каждые 5 секунд
    </script>

    <div class="scrollable-content">
        <div class="buttons">
            <a href="https://t.me/cheatmro" class="button">Мир Читеров</a>
            <a href="https://t.me/cheatbt" class="button">Читы на брутал страйк</a>
            <a href="https://t.me/cheatshtbpm" class="button">Читы на БПМ</a>
            <a href="https://t.me/Specnaz117" class="button">ЛС</a>
        </div>
    </div>

    <div class="video-container">
        <div class="video">
            <iframe src="https://www.youtube.com/embed/GrUbjuzMzng" title="YouTube video player" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        </div>
        <div class="video">
            <iframe src="https://www.youtube.com/embed/7pbz0znGQ2I" title="YouTube video player" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        </div>
        <div class="video">
            <iframe src="https://www.youtube.com/embed/PZB4qxcJNks" title="YouTube video player" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        </div>
        <div class="video">
            <iframe src="https://www.youtube.com/embed/dgqIryzuBxo" title="YouTube video player" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        </div>
        <div class="video">
            <iframe src="https://www.youtube.com/embed/Xo1dJ-g6MMM" title="YouTube video player" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        </div>
        <div class="video">
            <iframe src="https://www.youtube.com/embed/4mdNJxcPjo8" title="YouTube video player" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        </div>
    </div>
</body>
</html>
