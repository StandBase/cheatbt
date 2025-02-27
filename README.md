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
            overflow: hidden;
        }

        /* Видео на фоне */
        .background-video {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            object-fit: cover;
            z-index: -1;
        }

        h1 {
            color: #ffcc00;
            margin-bottom: 50px;
            font-size: 48px;
            text-shadow: 2px 2px 6px #000;
        }

        .buttons {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin-bottom: 40px;
            padding: 0;
            list-style-type: none;
        }

        .button {
            padding: 15px 30px;
            font-size: 20px;
            color: white;
            background: linear-gradient(135deg, #6a1b9a, #8e24aa);
            border: none;
            border-radius: 50px;
            text-decoration: none;
            transition: background-color 0.3s, transform 0.2s, box-shadow 0.4s;
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.2);
            text-align: center;
        }

        .button:hover {
            background: linear-gradient(135deg, #8e24aa, #6a1b9a);
            transform: translateY(-4px);
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.3);
        }

        .video-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 20px;
            justify-items: center;
        }

        .video {
            width: 100%;
            max-width: 320px;
            height: 180px;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.3);
            position: relative;
            animation: glow 1.5s infinite alternate;
        }

        iframe {
            width: 100%;
            height: 100%;
            border: none;
        }

        @keyframes glow {
            0% {
                box-shadow: 0 0 10px 3px rgba(138, 43, 226, 0.7);
            }

            100% {
                box-shadow: 0 0 20px 10px rgba(138, 43, 226, 0.7);
            }
        }
    </style>
</head>
<body>

    <!-- Видео фон -->
    <video class="background-video" autoplay muted loop>
        <source src="https://cdn.pixabay.com/video/2018/01/27/13949-253035804_large.mp4" type="video/mp4">
    </video>

    <h1>Hacker_TV</h1>

    <div class="buttons">
        <a href="https://t.me/cheatmro" class="button">Мир Читеров</a>
        <a href="https://t.me/cheatbt" class="button">Читы на брутал страйк</a>
        <a href="https://t.me/cheatshtbpm" class="button">Читы на БПМ</a>
        <a href="https://t.me/Specnaz117" class="button">ЛС</a>
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
    </div>

</body>
</html>
