<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>_by : 76n</title>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@700;900&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Cairo', sans-serif;
        }

        body {
            /* خلفية الشاشة بالكامل مع تظليل مظلم لزيادة الغموض */
            background: linear-gradient(rgba(0, 0, 0, 0.75), rgba(0, 0, 0, 0.85)), 
                        url('bg.jpg') no-repeat center center fixed;
            background-size: cover;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
            color: #ff003c;
        }

        .container {
            text-align: center;
            padding: 40px 30px;
            background: rgba(0, 0, 0, 0.65);
            border: 1px solid rgba(255, 0, 60, 0.3);
            border-radius: 20px;
            backdrop-filter: blur(8px);
            box-shadow: 0 0 30px rgba(255, 0, 60, 0.2);
            max-width: 450px;
            width: 90%;
            animation: fadeIn 2s ease-in-out;
        }

        .main-text {
            font-size: 2.2rem;
            font-weight: 900;
            color: #ff1a1a;
            text-shadow: 0 0 15px rgba(255, 0, 0, 0.8), 0 0 30px rgba(139, 0, 0, 0.6);
            margin-bottom: 10px;
            letter-spacing: 1px;
        }

        .sub-text {
            font-size: 1.4rem;
            font-weight: 700;
            color: #e60000;
            text-shadow: 0 0 10px rgba(230, 0, 0, 0.7);
            direction: ltr;
            margin-bottom: 30px;
        }

        /* زر مشغل الصوت */
        .audio-control {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
            background: rgba(20, 0, 0, 0.8);
            border: 1px solid #ff003c;
            color: #ff3333;
            padding: 12px 28px;
            border-radius: 30px;
            cursor: pointer;
            font-size: 1rem;
            font-weight: bold;
            transition: all 0.3s ease;
            box-shadow: 0 0 15px rgba(255, 0, 60, 0.2);
        }

        .audio-control:hover {
            background: #ff003c;
            color: #000;
            box-shadow: 0 0 25px rgba(255, 0, 60, 0.8);
            transform: scale(1.05);
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body>

    <div class="container">
        <h1 class="main-text">تم شخلكم من قبل</h1>
        <div class="sub-text">_by : 76n</div>

        <button class="audio-control" onclick="toggleAudio()" id="play-btn">
            <span id="btn-icon">▶</span> <span id="btn-text">تشغيل الصوت</span>
        </button>
    </div>

    <!-- ملف الصوتية -->
    <audio id="bg-music" loop>
        <source src="audio.mp3" type="audio/mpeg">
    </audio>

    <script>
        const audio = document.getElementById('bg-music');
        const btnIcon = document.getElementById('btn-icon');
        const btnText = document.getElementById('btn-text');

        function toggleAudio() {
            if (audio.paused) {
                audio.play();
                btnIcon.innerHTML = '⏸';
                btnText.innerHTML = 'إيقاف الصوت';
            } else {
                audio.pause();
                btnIcon.innerHTML = '▶';
                btnText.innerHTML = 'تشغيل الصوت';
            }
        }
    </script>

</body>
</html>
