# valentine-day
For Valentine Day
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>💖 My Eternal Valentine 💖</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Dancing+Script:wght@400;700&family=Montserrat:wght@300;400;600&display=swap');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Montserrat', sans-serif;
            background: #0a0a0a;
            min-height: 100vh;
            overflow-x: hidden;
            color: #fff;
        }

        /* Animated Background */
        .bg-gradient {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(125deg, #1a0b0b 0%, #2d1a1a 40%, #4a1e1e 100%);
            z-index: -2;
        }

        .bg-hearts {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle at 20% 50%, rgba(255, 107, 107, 0.1) 0%, transparent 50%),
                        radial-gradient(circle at 80% 80%, rgba(255, 158, 158, 0.1) 0%, transparent 50%);
            z-index: -1;
            animation: pulse 8s ease-in-out infinite;
        }

        @keyframes pulse {
            0%, 100% { opacity: 0.5; }
            50% { opacity: 1; }
        }

        /* Floating Hearts Premium */
        .floating-hearts {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 0;
        }

        .heart-premium {
            position: absolute;
            color: rgba(255, 182, 193, 0.3);
            font-size: 24px;
            filter: drop-shadow(0 0 10px rgba(255, 77, 141, 0.5));
            animation: floatPremium 15s infinite;
        }

        @keyframes floatPremium {
            0% {
                transform: translateY(100vh) rotate(0deg) scale(1);
                opacity: 0;
            }
            20% {
                opacity: 0.8;
            }
            80% {
                opacity: 0.8;
            }
            100% {
                transform: translateY(-100px) rotate(720deg) scale(0);
                opacity: 0;
            }
        }

        /* Main Container */
        .container {
            max-width: 1400px;
            margin: 0 auto;
            padding: 30px;
            position: relative;
            z-index: 2;
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            position: relative;
            margin-bottom: 50px;
        }

        .hero h1 {
            font-family: 'Dancing Script', cursive;
            font-size: 8em;
            background: linear-gradient(135deg, #ff758c, #ff7eb3, #ff9a9e);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 0 0 30px rgba(255, 117, 140, 0.5);
            margin-bottom: 20px;
            animation: titleGlow 3s ease-in-out infinite;
            position: relative;
        }

        @keyframes titleGlow {
            0%, 100% { filter: drop-shadow(0 0 20px rgba(255, 117, 140, 0.6)); }
            50% { filter: drop-shadow(0 0 50px rgba(255, 117, 140, 1)); }
        }

        .hero-subtitle {
            font-size: 2.5em;
            color: #fff;
            text-shadow: 0 0 20px rgba(255, 255, 255, 0.5);
            margin-bottom: 50px;
            font-weight: 300;
            letter-spacing: 3px;
        }

        .hero-name {
            font-family: 'Dancing Script', cursive;
            font-size: 4em;
            color: #ffb6c1;
            animation: fadeInUp 1.5s ease;
            margin-bottom: 30px;
        }

        /* 3D Love Cube */
        .love-cube-container {
            perspective: 1000px;
            margin: 80px 0;
        }

        .love-cube {
            width: 200px;
            height: 200px;
            margin: 0 auto;
            position: relative;
            transform-style: preserve-3d;
            animation: rotate 20s infinite linear;
        }

        .cube-face {
            position: absolute;
            width: 200px;
            height: 200px;
            background: linear-gradient(135deg, rgba(255, 107, 107, 0.9), rgba(255, 158, 158, 0.9));
            border: 3px solid #ffd700;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 3em;
            color: white;
            text-shadow: 0 0 10px rgba(0,0,0,0.5);
            box-shadow: 0 0 30px rgba(255, 215, 0, 0.3);
            backdrop-filter: blur(5px);
        }

        .front  { transform: translateZ(100px); }
        .back   { transform: rotateY(180deg) translateZ(100px); }
        .right  { transform: rotateY(90deg) translateZ(100px); }
        .left   { transform: rotateY(-90deg) translateZ(100px); }
        .top    { transform: rotateX(90deg) translateZ(100px); }
        .bottom { transform: rotateX(-90deg) translateZ(100px); }

        @keyframes rotate {
            from { transform: rotateX(0) rotateY(0); }
            to { transform: rotateX(360deg) rotateY(360deg); }
        }

        /* Love Letter Premium */
        .love-letter-premium {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 30px;
            padding: 60px;
            margin: 100px auto;
            max-width: 900px;
            box-shadow: 0 20px 50px rgba(0,0,0,0.5),
                        0 0 0 2px rgba(255, 107, 107, 0.3) inset;
            position: relative;
            overflow: hidden;
        }

        .love-letter-premium::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,107,107,0.1) 0%, transparent 70%);
            animation: rotate 20s linear infinite;
        }

        .love-letter-premium h2 {
            font-family: 'Dancing Script', cursive;
            font-size: 4em;
            color: #ffb6c1;
            margin-bottom: 30px;
            position: relative;
        }

        .love-letter-premium p {
            font-size: 1.3em;
            line-height: 2;
            color: rgba(255,255,255,0.9);
            margin-bottom: 25px;
            position: relative;
            text-align: justify;
        }

        .signature-premium {
            font-family: 'Dancing Script', cursive;
            font-size: 3em;
            color: #ffb6c1;
            text-align: right;
            margin-top: 50px;
            position: relative;
        }

        /* Timeline Gallery */
        .timeline {
            margin: 150px 0;
            position: relative;
        }

        .timeline::before {
            content: '';
            position: absolute;
            left: 50%;
            transform: translateX(-50%);
            width: 4px;
            height: 100%;
            background: linear-gradient(180deg, transparent, #ff758c, #ff7eb3, #ff758c, transparent);
        }

        .timeline-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin: 100px 0;
            position: relative;
        }

        .timeline-item:nth-child(even) {
            flex-direction: row-reverse;
        }

        .timeline-content {
            width: 45%;
            background: rgba(255,255,255,0.05);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 30px;
            border: 1px solid rgba(255,107,107,0.3);
            transition: all 0.5s ease;
        }

        .timeline-content:hover {
            transform: scale(1.05) translateY(-10px);
            border-color: #ff758c;
            box-shadow: 0 20px 40px rgba(255,107,107,0.3);
        }

        .timeline-date {
            font-size: 1.5em;
            color: #ff758c;
            margin-bottom: 15px;
            font-weight: 600;
        }

        .timeline-image {
            width: 200px;
            height: 200px;
            border-radius: 50%;
            background: linear-gradient(135deg, #ff758c, #ff9a9e);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 4em;
            box-shadow: 0 0 50px rgba(255,117,140,0.5);
            animation: pulse 3s ease-in-out infinite;
        }

        /* Love Statistics */
        .stats-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin: 100px 0;
        }

        .stat-card {
            background: rgba(255,255,255,0.03);
            backdrop-filter: blur(10px);
            border-radius: 30px;
            padding: 40px 20px;
            text-align: center;
            border: 1px solid rgba(255,107,107,0.2);
            transition: all 0.5s ease;
            position: relative;
            overflow: hidden;
        }

        .stat-card::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,107,107,0.1) 0%, transparent 70%);
            opacity: 0;
            transition: opacity 0.5s ease;
        }

        .stat-card:hover::before {
            opacity: 1;
        }

        .stat-card:hover {
            transform: translateY(-10px);
            border-color: #ff758c;
            box-shadow: 0 20px 40px rgba(255,107,107,0.2);
        }

        .stat-number {
            font-size: 4em;
            font-weight: 700;
            background: linear-gradient(135deg, #ff758c, #ffb6c1);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 10px;
        }

        .stat-label {
            font-size: 1.3em;
            color: rgba(255,255,255,0.8);
        }

        /* Interactive Love Letter */
        .interactive-letter {
            background: linear-gradient(135deg, #1a0b0b, #2d1a1a);
            border-radius: 30px;
            padding: 60px;
            margin: 100px 0;
            position: relative;
            border: 2px solid #ff758c;
            box-shadow: 0 0 50px rgba(255,117,140,0.3);
        }

        .interactive-letter h3 {
            font-size: 2.5em;
            color: #ffb6c1;
            margin-bottom: 30px;
        }

        .message-input {
            width: 100%;
            padding: 20px;
            background: rgba(255,255,255,0.05);
            border: 2px solid #ff758c;
            border-radius: 15px;
            color: white;
            font-size: 1.2em;
            margin-bottom: 20px;
            resize: none;
        }

        .message-input:focus {
            outline: none;
            box-shadow: 0 0 30px rgba(255,117,140,0.5);
        }

        .send-btn {
            background: linear-gradient(135deg, #ff758c, #ff9a9e);
            color: white;
            border: none;
            padding: 15px 40px;
            font-size: 1.3em;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 10px 20px rgba(255,117,140,0.3);
        }

        .send-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 20px 40px rgba(255,117,140,0.5);
        }

        .message-display {
            margin-top: 40px;
            padding: 30px;
            background: rgba(0,0,0,0.3);
            border-radius: 20px;
            border-left: 5px solid #ff758c;
            font-size: 1.3em;
            line-height: 1.8;
            color: rgba(255,255,255,0.9);
            min-height: 100px;
        }

        /* Music Player Premium */
        .music-player-premium {
            position: fixed;
            bottom: 30px;
            right: 30px;
            background: rgba(255,255,255,0.1);
            backdrop-filter: blur(10px);
            border-radius: 60px;
            padding: 15px 30px;
            border: 2px solid #ff758c;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
            z-index: 1000;
            cursor: pointer;
            display: flex;
            align-items: center;
            gap: 15px;
            transition: all 0.3s ease;
        }

        .music-player-premium:hover {
            transform: scale(1.1);
            background: #ff758c;
            border-color: white;
        }

        .music-icon {
            font-size: 2em;
            animation: spin 3s linear infinite;
        }

        @keyframes spin {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }

        /* Love Quiz */
        .quiz-container {
            background: rgba(255,255,255,0.05);
            backdrop-filter: blur(10px);
            border-radius: 30px;
            padding: 60px;
            margin: 100px 0;
            border: 2px solid #ff758c;
        }

        .quiz-question {
            font-size: 2em;
            color: #ffb6c1;
            margin-bottom: 30px;
        }

        .quiz-options {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
        }

        .quiz-option {
            background: rgba(255,255,255,0.03);
            border: 2px solid #ff758c;
            border-radius: 15px;
            padding: 20px;
            color: white;
            font-size: 1.2em;
            cursor: pointer;
            transition: all 0.3s ease;
            text-align: left;
        }

        .quiz-option:hover {
            background: #ff758c;
            transform: translateX(10px);
            box-shadow: 0 10px 20px rgba(255,117,140,0.3);
        }

        .quiz-option.correct {
            background: #4CAF50;
            border-color: white;
        }

        .quiz-feedback {
            margin-top: 30px;
            font-size: 1.5em;
            color: #ffb6c1;
            min-height: 60px;
        }

        /* 3D Heart */
        .heart-3d {
            width: 300px;
            height: 300px;
            margin: 100px auto;
            position: relative;
            transform-style: preserve-3d;
            animation: heartBeat 2s ease-in-out infinite;
        }

        @keyframes heartBeat {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.1); }
        }

        /* Responsive */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 4em;
            }
            
            .hero-subtitle {
                font-size: 1.5em;
            }
            
            .timeline::before {
                left: 30px;
            }
            
            .timeline-item,
            .timeline-item:nth-child(even) {
                flex-direction: column;
            }
            
            .timeline-content {
                width: 90%;
                margin-left: 50px;
            }
            
            .quiz-options {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="bg-gradient"></div>
    <div class="bg-hearts"></div>
    
    <!-- Premium Floating Hearts -->
    <div class="floating-hearts" id="premiumHearts"></div>

    <!-- Music Player Premium -->
    <div class="music-player-premium" onclick="togglePremiumMusic()">
        <span class="music-icon">💝</span>
        <span id="premiumMusicStatus">Play Love Songs</span>
    </div>

    <!-- Main Container -->
    <div class="container">
        <!-- Hero Section -->
        <section class="hero">
            <h1>Happy Valentine's Day</h1>
            <div class="hero-subtitle">Untuk Cinta Sejatiku</div>
            <div class="hero-name" id="nameAnimation"></div>
            
            <!-- 3D Love Cube -->
            <div class="love-cube-container">
                <div class="love-cube">
                    <div class="cube-face front">❤️</div>
                    <div class="cube-face back">💖</div>
                    <div class="cube-face right">💕</div>
                    <div class="cube-face left">💗</div>
                    <div class="cube-face top">💓</div>
                    <div class="cube-face bottom">💘</div>
                </div>
            </div>
        </section>

        <!-- Love Letter Premium -->
        <section class="love-letter-premium">
            <h2>My Eternal Love Letter</h2>
            <p>My Dearest Love,</p>
            <p>Sejak pertama kali aku melihatmu, dunia ini berubah menjadi lebih indah. Kamu adalah puisi terindah yang pernah Tuhan tulis, lukisan paling sempurna yang pernah ada. Setiap detik bersamamu adalah anugerah yang tak ternilai.</p>
            <p>Di hari Valentine ini, aku ingin kamu tahu bahwa cintaku padamu bukan hanya hari ini, tapi selamanya. Kamu adalah rumah bagiku, tempat aku pulang, tempat aku merasa aman dan dicintai.</p>
            <p>Aku mencintai caramu tersenyum, caramu tertawa, caramu membuat segalanya terasa istimewa. Kamu adalah alasan aku bangun setiap pagi dan mimpi indahku setiap malam.</p>
            <p>Tak ada kata yang cukup untuk menggambarkan betapa berharganya dirimu bagiku. Kamu adalah segalanya, kamu adalah duniaku.</p>
            <p>I love you more than all the stars in the universe, more than all the sand on every beach, more than anything in this world and beyond.</p>
            <div class="signature-premium">Forever Yours, 💝</div>
        </section>

        <!-- Timeline Gallery -->
        <section class="timeline">
            <h2 style="text-align: center; font-size: 3.5em; font-family: 'Dancing Script', cursive; color: #ffb6c1; margin-bottom: 80px;">Our Love Story</h2>
            
            <div class="timeline-item">
                <div class="timeline-content">
                    <div class="timeline-date">Pertama Bertemu</div>
                    <p>Hari itu, di sebuah kafe kecil, takdir mempertemukan kita. Aku tidak pernah percaya pada cinta pada pandangan pertama, sampai aku melihatmu.</p>
                </div>
                <div class="timeline-image">☕</div>
            </div>

            <div class="timeline-item">
                <div class="timeline-content">
                    <div class="timeline-date">First Date</div>
                    <p>Kencan pertama kita yang tak terlupakan. Kita bicara berjam-jam tentang segalanya, dan aku tahu saat itu kamu adalah orang yang tepat.</p>
                </div>
                <div class="timeline-image">🌹</div>
            </div>

            <div class="timeline-item">
                <div class="timeline-content">
                    <div class="timeline-date">Jadi Pacar</div>
                    <p>Hari terindah ketika kamu bilang "Iya" dan dunia terasa begitu sempurna. Aku orang paling beruntung di dunia.</p>
                </div>
                <div class="timeline-image">💑</div>
            </div>

            <div class="timeline-item">
                <div class="timeline-content">
                    <div class="timeline-date">Today & Forever</div>
                    <p>Setiap hari bersamamu adalah petualangan baru. Aku tidak sabar untuk menghabiskan sisa hidupku bersamamu.</p>
                </div>
                <div class="timeline-image">✨</div>
            </div>
        </section>

        <!-- Love Statistics -->
        <section class="stats-container">
            <div class="stat-card">
                <div class="stat-number" id="daysTogether">0</div>
                <div class="stat-label">Hari Bersama</div>
            </div>
            <div class="stat-card">
                <div class="stat-number" id="kissCount">0</div>
                <div class="stat-label">Kali Bilang I Love You</div>
            </div>
            <div class="stat-card">
                <div class="stat-number" id="smileCount">0</div>
                <div class="stat-label">Senyumanmu</div>
            </div>
            <div class="stat-card">
                <div class="stat-number">∞</div>
                <div class="stat-label">Cintaku Padamu</div>
            </div>
        </section>

        <!-- Interactive Love Letter -->
        <section class="interactive-letter">
            <h3>Tulis Pesan Spesial 💌</h3>
            <textarea class="message-input" id="loveMessage" rows="4" placeholder="Tulis pesan untukku..."></textarea>
            <button class="send-btn" onclick="sendLoveMessage()">Kirim Pesan 💕</button>
            <div class="message-display" id="messageDisplay">
                Pesan spesial akan muncul di sini...
            </div>
        </section>

        <!-- Love Quiz -->
        <section class="quiz-container">
            <h2 style="font-size: 2.5em; color: #ffb6c1; margin-bottom: 40px;">Love Quiz 💭</h2>
            <div class="quiz-question" id="quizQuestion">Di mana kita pertama kali bertemu?</div>
            <div class="quiz-options">
                <div class="quiz-option" onclick="checkAnswer(this, 'Di Kafe')">Di Kafe</div>
                <div class="quiz-option" onclick="checkAnswer(this, 'Di Taman')">Di Taman</div>
                <div class="quiz-option" onclick="checkAnswer(this, 'Di Kampus')">Di Kampus</div>
                <div class="quiz-option" onclick="checkAnswer(this, 'Di Mall')">Di Mall</div>
            </div>
            <div class="quiz-feedback" id="quizFeedback"></div>
        </section>

        <!-- 3D Heart Animation -->
        <div class="heart-3d">
            <!-- Will be filled with Three.js -->
        </div>
    </div>

    <script>
        // Generate premium floating hearts
        function createPremiumHearts() {
            const container = document.getElementById('premiumHearts');
            const heartSymbols = ['❤️', '💖', '💕', '💗', '💓', '💘', '💝', '💟', '💞', '💌'];
            
            for (let i = 0; i < 100; i++) {
                const heart = document.createElement('div');
                heart.className = 'heart-premium';
                heart.innerHTML = heartSymbols[Math.floor(Math.random() * heartSymbols.length)];
                heart.style.left = Math.random() * 100 + '%';
                heart.style.animationDuration = (Math.random() * 10 + 10) + 's';
                heart.style.fontSize = (Math.random() * 30 + 20) + 'px';
                heart.style.animationDelay = Math.random() * 10 + 's';
                heart.style.opacity = Math.random() * 0.5 + 0.3;
                container.appendChild(heart);
            }
        }

        // Animate name typing
        const names = ['Sayang', 'Cinta', 'Bidadari', 'My Love', 'My Everything'];
        let nameIndex = 0;
        let charIndex = 0;
        let isDeleting = false;
        
        function typeName() {
            const currentName = names[nameIndex];
            const element = document.getElementById('nameAnimation');
            
            if (isDeleting) {
                element.textContent = currentName.substring(0, charIndex - 1);
                charIndex--;
            } else {
                element.textContent = currentName.substring(0, charIndex + 1);
                charIndex++;
            }
            
            if (!isDeleting && charIndex === currentName.length) {
                isDeleting = true;
                setTimeout(typeName, 2000);
            } else if (isDeleting && charIndex === 0) {
                isDeleting = false;
                nameIndex = (nameIndex + 1) % names.length;
                setTimeout(typeName, 500);
            } else {
                setTimeout(typeName, isDeleting ? 100 : 200);
            }
        }

        // Calculate days together
        function updateDaysTogether() {
            const firstDate = new Date('2024-01-01'); // Ubah sesuai tanggal pertama
            const today = new Date();
            const diffTime = Math.abs(today - firstDate);
            const diffDays = Math.ceil(diffTime / (1000 * 60 * 60 * 24));
            
            document.getElementById('daysTogether').textContent = diffDays;
            document.getElementById('kissCount').textContent = diffDays * 10;
            document.getElementById('smileCount').textContent = diffDays * 50;
        }

        // Music player
        let isMusicPlaying = false;
        let audioContext = null;
        
        function togglePremiumMusic() {
            if (!audioContext) {
                audioContext = new (window.AudioContext || window.webkitAudioContext)();
            }
            
            if (isMusicPlaying) {
                audioContext.close();
                audioContext = null;
                document.getElementById('premiumMusicStatus').textContent = 'Play Love Songs';
                isMusicPlaying = false;
            } else {
                audioContext.resume();
                // Create a beautiful melody
                playLoveMelody();
                document.getElementById('premiumMusicStatus').textContent = '💖 Playing...';
                isMusicPlaying = true;
            }
        }

        function playLoveMelody() {
            if (!audioContext) return;
            
            const now = audioContext.currentTime;
            const notes = [523.25, 659.25, 783.99, 1046.50, 783.99, 659.25, 523.25];
            const durations = [0.5, 0.5, 0.5, 1, 0.5, 0.5, 1];
            
            notes.forEach((freq, i) => {
                const osc = audioContext.createOscillator();
                const gain = audioContext.createGain();
                
                osc.type = 'sine';
                osc.frequency.value = freq;
                
                gain.gain.setValueAtTime(0.1, now + i * 0.5);
                gain.gain.exponentialRampToValueAtTime(0.01, now + i * 0.5 + durations[i]);
                
                osc.connect(gain);
                gain.connect(audioContext.destination);
                
                osc.start(now + i * 0.5);
                osc.stop(now + i * 0.5 + durations[i]);
            });
            
            if (isMusicPlaying) {
                setTimeout(playLoveMelody, 4000);
            }
        }

        // Send love message
        function sendLoveMessage() {
            const message = document.getElementById('loveMessage').value;
            const display = document.getElementById('messageDisplay');
            
            if (message.trim() === '') {
                display.innerHTML = 'Tulis sesuatu dulu dong sayang... 💕';
            } else {
                display.innerHTML = `💌 Pesan spesial: "${message}"<br><br>I love you too! 💖`;
                document.getElementById('loveMessage').value = '';
                
                // Create confetti effect
                createConfetti();
            }
        }

        // Love Quiz
        function checkAnswer(element, answer) {
            const correctAnswer = 'Di Kafe';
            const feedback = document.getElementById('quizFeedback');
            const options = document.querySelectorAll('.quiz-option');
            
            options.forEach(opt => opt.classList.remove('correct'));
            
            if (answer === correctAnswer) {
                element.classList.add('correct');
                feedback.innerHTML = '✨ Benar! Kamu ingat! I love you! ✨';
                createConfetti();
            } else {
                feedback.innerHTML = '💔 Aduh, lupa ya? Kita pertama kali ketemu di kafe!';
            }
        }

        // Confetti effect
        function createConfetti() {
            for (let i = 0; i < 50; i++) {
                const confetti = document.createElement('div');
                confetti.style.position = 'fixed';
                confetti.style.left = Math.random() * 100 + '%';
                confetti.style.top = -10 + 'px';
                confetti.style.color = ['#ff758c', '#ffb6c1', '#ffd700', '#ff9a9e'][Math.floor(Math.random() * 4)];
                confetti.style.fontSize = (Math.random() * 20 + 10) + 'px';
                confetti.style.zIndex = '9999';
                confetti.style.pointerEvents = 'none';
                confetti.innerHTML = ['❤️', '💖', '💕', '💗', '✨', '⭐'][Math.floor(Math.random() * 6)];
                confetti.style.animation = `confettiFall ${Math.random() * 3 + 2}s linear`;
                document.body.appendChild(confetti);
                
                setTimeout(() => confetti.remove(), 5000);
            }
        }

        // Add confetti animation style
        const style = document.createElement('style');
        style.textContent = `
            @keyframes confettiFall {
                0% { transform: translateY(-10px) rotate(0deg); opacity: 1; }
                100% { transform: translateY(100vh) rotate(720deg); opacity: 0; }
            }
        `;
        document.head.appendChild(style);

        // PHP Integration
        <?php
        session_start();
        
        // Get current date and time
        $currentDate = date('l, d F Y H:i:s');
        
        // Check if it's Valentine's Day
        $isValentine = (date('m-d') == '02-14');
        
        // Visitor counter
        if (!isset($_SESSION['visitor_count'])) {
            $_SESSION['visitor_count'] = 1;
        } else {
            $_SESSION['visitor_count']++;
        }
        
        // Get user info
        $userAgent = $_SERVER['HTTP_USER_AGENT'];
        $ipAddress = $_SERVER['REMOTE_ADDR'];
        
        // Special Valentine's Day message
        $valentineMessage = $isValentine ? "💝 SELAMAT HARI VALENTINE SAYANG! 💝" : "Menunggu Hari Valentine...";
        
        // Time until next Valentine
        $nextValentine = mktime(0, 0, 0, 2, 14, date('Y') + (date('m-d') > '02-14' ? 1 : 0));
        $timeUntil = $nextValentine - time();
        $daysUntil = floor($timeUntil / (60 * 60 * 24));
        ?>

        // Display PHP info in console
        console.log("💖 Valentine Website 💖");
        console.log("Current Date: <?php echo $currentDate; ?>");
        console.log("Visitor #<?php echo $visitorCount; ?>");
        console.log("Days until next Valentine: <?php echo $daysUntil; ?>");
        
        // Add PHP info to page
        const phpInfoDiv = document.createElement('div');
        phpInfoDiv.style.cssText = `
            position: fixed;
            bottom: 30px;
            left: 30px;
            background: rgba(255,255,255,0.1);
            backdrop-filter: blur(10px);
            padding: 10px 20px;
            border-radius: 30px;
            color: #ffb6c1;
            font-size: 0.9em;
            border: 1px solid #ff758c;
            z-index: 1000;
        `;
        phpInfoDiv.innerHTML = `👀 Visitor #<?php echo $visitorCount; ?> | ${new Date().toLocaleDateString('id-ID')}`;
        document.body.appendChild(phpInfoDiv);

        // Special Valentine effect
        <?php if ($isValentine): ?>
        document.body.classList.add('valentine-mode');
        showValentineSurprise();
        <?php endif; ?>

        function showValentineSurprise() {
            setTimeout(() => {
                alert("💝 Happy Valentine's Day Sayang! 💝\nI LOVE YOU FOREVER!");
                createConfetti();
                createConfetti();
            }, 2000);
        }

        // Initialize everything
        window.onload = function() {
            createPremiumHearts();
            typeName();
            updateDaysTogether();
            setInterval(updateDaysTogether, 86400000); // Update every day
            
            // Welcome message
            setTimeout(() => {
                const welcome = document.createElement('div');
                welcome.style.cssText = `
                    position: fixed;
                    top: 50%;
                    left: 50%;
                    transform: translate(-50%, -50%);
                    background: linear-gradient(135deg, #ff758c, #ff9a9e);
                    padding: 40px;
                    border-radius: 30px;
                    color: white;
                    font-size: 2em;
                    text-align: center;
                    z-index: 10000;
                    animation: fadeOut 3s forwards;
                    box-shadow: 0 0 100px rgba(255,117,140,0.8);
                    border: 3px solid white;
                `;
                welcome.innerHTML = '💖 Welcome My Love! 💖';
                document.body.appendChild(welcome);
                
                setTimeout(() => welcome.remove(), 3000);
            }, 500);
        };

        // Add fadeOut animation
        const fadeOutStyle = document.createElement('style');
        fadeOutStyle.textContent = `
            @keyframes fadeOut {
                0% { opacity: 1; }
                70% { opacity: 1; }
                100% { opacity: 0; }
            }
        `;
        document.head.appendChild(fadeOutStyle);
    </script>

    <!-- Add Three.js for 3D Heart -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
    <script>
        // Initialize 3D Heart
        function init3DHeart() {
            const container = document.querySelector('.heart-3d');
            const width = container.clientWidth;
            const height = container.clientHeight;
            
            const scene = new THREE.Scene();
            const camera = new THREE.PerspectiveCamera(75, width / height, 0.1, 1000);
            const renderer = new THREE.WebGLRenderer({ alpha: true });
            
            renderer.setSize(width, height);
            renderer.setClearColor(0x000000, 0);
            container.appendChild(renderer.domElement);
            
            // Create heart shape particles
            const particles = [];
            const particleCount = 1000;
            const geometry = new THREE.BufferGeometry();
            const positions = new Float32Array(particleCount * 3);
            const colors = new Float32Array(particleCount * 3);
            
            for (let i = 0; i < particleCount; i++) {
                // Heart parametric equation
                const t = Math.random() * Math.PI * 2;
                const x = 16 * Math.pow(Math.sin(t), 3);
                const y = 13 * Math.cos(t) - 5 * Math.cos(2*t) - 2 * Math.cos(3*t) - Math.cos(4*t);
                const z = (Math.random() - 0.5) * 10;
                
                positions[i*3] = x * 0.5;
                positions[i*3+1] = y * 0.5;
                positions[i*3+2] = z;
                
                // Colors
                colors[i*3] = 1.0;
                colors[i*3+1] = 0.4 + Math.random() * 0.3;
                colors[i*3+2] = 0.5 + Math.random() * 0.3;
            }
            
            geometry.setAttribute('position', new THREE.BufferAttribute(positions, 3));
            geometry.setAttribute('color', new THREE.BufferAttribute(colors, 3));
            
            const material = new THREE.PointsMaterial({
                size: 0.3,
                vertexColors: true,
                blending: THREE.AdditiveBlending,
                transparent: true
            });
            
            const heart = new THREE.Points(geometry, material);
            scene.add(heart);
            
            camera.position.z = 30;
            
            function animate() {
                requestAnimationFrame(animate);
                
                heart.rotation.y += 0.005;
                heart.rotation.x += 0.002;
                
                renderer.render(scene, camera);
            }
            
            animate();
        }

        // Call 3D heart init when element is ready
        setTimeout(init3DHeart, 1000);
    </script>

    <style>
        /* Additional premium styles */
        .valentine-mode .hero h1 {
            animation: valentineGlow 1s ease-in-out infinite alternate;
        }
        
        @keyframes valentineGlow {
            from { text-shadow: 0 0 30px #ff758c; }
            to { text-shadow: 0 0 80px #ff1493; }
        }
        
        ::-webkit-scrollbar {
            width: 12px;
            background: #1a0b0b;
        }
        
        ::-webkit-scrollbar-thumb {
            background: linear-gradient(135deg, #ff758c, #ff9a9e);
            border-radius: 6px;
            border: 3px solid #1a0b0b;
        }
        
        ::-webkit-scrollbar-thumb:hover {
            background: linear-gradient(135deg, #ff9a9e, #ff758c);
        }
        
        /* Loading animation */
        .loading-heart {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: #0a0a0a;
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 99999;
            transition: opacity 1s ease;
        }
        
        .loading-heart.fade-out {
            opacity: 0;
            pointer-events: none;
        }
        
        .heart-loader {
            width: 100px;
            height: 100px;
            background: #ff758c;
            position: relative;
            transform: rotate(45deg);
            animation: heartbeat 1.4s infinite;
        }
        
        .heart-loader::before,
        .heart-loader::after {
            content: '';
            width: 100px;
            height: 100px;
            background: #ff758c;
            border-radius: 50%;
            position: absolute;
        }
        
        .heart-loader::before {
            left: -50px;
        }
        
        .heart-loader::after {
            top: -50px;
        }
        
        @keyframes heartbeat {
            0% { transform: rotate(45deg) scale(1); }
            25% { transform: rotate(45deg) scale(1.1); }
            50% { transform: rotate(45deg) scale(1); }
            75% { transform: rotate(45deg) scale(1.1); }
            100% { transform: rotate(45deg) scale(1); }
        }
    </style>

    <!-- Loading Screen -->
    <div class="loading-heart" id="loadingScreen">
        <div class="heart-loader"></div>
    </div>

    <script>
        // Remove loading screen
        window.addEventListener('load', function() {
            setTimeout(() => {
                document.getElementById('loadingScreen').classList.add('fade-out');
            }, 2000);
        });
    </script>
</body>
</html>
