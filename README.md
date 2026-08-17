<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>7sn | Profile</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: #0f0f12;
            color: #ffffff;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            text-align: center;
        }

        .card {
            background: rgba(255, 255, 255, 0.05);
            padding: 40px;
            border-radius: 16px;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            max-width: 400px;
            width: 90%;
            box-shadow: 0 8px 32px 0 rgba(0, 0, 0, 0.37);
        }

        h1 {
            font-size: 2rem;
            margin-bottom: 10px;
            color: #7289da;
        }

        p {
            font-size: 1.1rem;
            color: #ccc;
            margin-bottom: 25px;
            line-height: 1.6;
        }

        .play-btn {
            background-color: #7289da;
            color: white;
            border: none;
            padding: 12px 24px;
            font-size: 1rem;
            border-radius: 8px;
            cursor: pointer;
            transition: 0.3s ease;
        }

        .play-btn:hover {
            background-color: #5b6eae;
            transform: scale(1.05);
        }
    </style>
</head>
<body>

    <div class="card">
        <h1>. ZERO , 7sn</h1>
        <p>حياكم الله في صفحتي الخاصة، حبيت اسلم عليكم فقط لا غير يعطيك العافية جميعاً.</p>
        
        <!-- زر تشغيل الصوت -->
        <button class="play-btn" onclick="toggleAudio()">🎵 تشغيل / إيقاف الصوت</button>
    </div>

    <!-- ملف الصوت -->
    <audio id="bg-music" loop>
        <source src="song.mp3" type="audio/mpeg">
    </audio>

    <script>
        const audio = document.getElementById('bg-music');

        function toggleAudio() {
            if (audio.paused) {
                audio.play();
            } else {
                audio.pause();
            }
        }
    </script>

</body>
</html>
