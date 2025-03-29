<!DOCTYPE html>  
<html lang="ru">  
<head>  
    <meta charset="UTF-8">  
    <meta name="viewport" content="width=device-width, initial-scale=1.0">  
    <title>Слайд-шоу Видео</title>  
    <style>  
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
            font-size: 48px;  
            color: #bb86fc;  
            margin-bottom: 50px;  
            text-shadow: 0 0 8px rgba(138, 43, 226, 1), 0 0 20px rgba(138, 43, 226, 0.8), 0 0 30px rgba(138, 43, 226, 0.6);  
            background: linear-gradient(135deg, #9c27b0, #6a1b9a);  
            -webkit-background-clip: text;  
            color: transparent;  
            transition: text-shadow 0.3s ease-in-out;  
        }  

        h1:hover {  
            text-shadow: 0 0 15px rgba(138, 43, 226, 1), 0 0 30px rgba(138, 43, 226, 0.8), 0 0 40px rgba(138, 43, 226, 0.6);  
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
        }  

        .button:hover {  
            background: linear-gradient(135deg, #8e24aa, #6a1b9a);  
            transform: translateY(-4px);  
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.3);  
        }  

        .slideshow-container {  
            position: relative;  
            width: 100%;  
            max-width: 600px;  
            margin: auto;  
            overflow: hidden;  
        }  

        .video {  
            display: none; /* Скрыть все видео по умолчанию */  
            width: 100%;  
            height: auto;  
        }  

        .active {  
            display: block; /* Показать текущее видео */  
            animation: fade 1s;  
        }  

        @keyframes fade {  
            from { opacity: 0; }  
            to { opacity: 1; }  
        }  
    </style>  
</head>  
<body>  

    <h1>Слайд-шоу Видео</h1>  

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

</body>  
</html>  
