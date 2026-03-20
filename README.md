<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>For My Bubu ❤️</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: linear-gradient(135deg, #000000 0%, #1a0000 100%);
            color: white;
            font-family: 'Courier New', monospace;
            overflow: hidden;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .container {
            text-align: center;
            position: relative;
            z-index: 10;
            padding: 20px;
            max-width: 600px;
        }

        #typing {
            font-size: 24px;
            white-space: pre-line;
            border-right: 3px solid gold;
            display: inline-block;
            padding: 20px;
            min-height: 150px;
            line-height: 1.6;
            animation: blink 1s infinite;
        }

        @keyframes blink {
            50% { border-right-color: transparent; }
        }

        .button-container {
            margin: 30px 0;
        }

        #startBtn {
            padding: 15px 40px;
            border-radius: 50px;
            border: 2px solid gold;
            background: gold;
            color: black;
            cursor: pointer;
            font-size: 18px;
            font-weight: bold;
            transition: all 0.3s ease;
            box-shadow: 0 0 20px rgba(255, 215, 0, 0.5);
        }

        #startBtn:hover {
            background: transparent;
            color: gold;
            transform: scale(1.05);
            box-shadow: 0 0 30px rgba(255, 215, 0, 0.8);
        }

        #startBtn:active {
            transform: scale(0.95);
        }

        .photos {
            display: none;
            margin-top: 30px;
            gap: 20px;
            justify-content: center;
            flex-wrap: wrap;
        }

        .photos.show {
            display: flex;
        }

        .photo-wrapper {
            position: relative;
        }

        .photos img {
            width: 200px;
            height: 250px;
            object-fit: cover;
            border-radius: 15px;
            border: 3px solid gold;
            opacity: 0;
            animation: fadeIn 2s ease forwards;
            box-shadow: 0 10px 30px rgba(255, 215, 0, 0.3);
            transition: transform 0.3s ease;
        }

        .photos img:hover {
            transform: scale(1.05);
        }

        .photos img:nth-child(2) {
            animation-delay: 0.5s;
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        #final {
            display: none;
            font-size: 20px;
            margin-top: 30px;
            padding: 20px;
            color: gold;
            animation: glowPulse 2s ease-in-out infinite;
            white-space: pre-wrap;
            line-height: 1.8;
            background: rgba(255, 215, 0, 0.1);
            border-radius: 10px;
            border-left: 4px solid gold;
        }

        #final.show {
            display: block;
        }

        @keyframes glowPulse {
            0%, 100% {
                text-shadow: 0 0 10px gold, 0 0 20px rgba(255, 215, 0, 0.5);
            }
            50% {
                text-shadow: 0 0 20px gold, 0 0 40px rgba(255, 215, 0, 0.8);
            }
        }

        .particle {
            position: fixed;
            width: 4px;
            height: 4px;
            background: gold;
            border-radius: 50%;
            pointer-events: none;
            box-shadow: 0 0 10px gold;
            animation: float 8s linear infinite;
        }

        @keyframes float {
            to {
                transform: translateY(-100vh) translateX(100px);
                opacity: 0;
            }
        }

        .loading {
            display: inline-block;
            width: 8px;
            height: 8px;
            background: gold;
            border-radius: 50%;
            animation: pulse 1.5s ease-in-out infinite;
            margin-left: 5px;
        }

        @keyframes pulse {
            0%, 100% { opacity: 0; }
            50% { opacity: 1; }
        }

        .music-toggle {
            position: fixed;
            top: 20px;
            right: 20px;
            background: gold;
            color: black;
            border: none;
            border-radius: 50%;
            width: 50px;
            height: 50px;
            cursor: pointer;
            font-size: 24px;
            z-index: 100;
            box-shadow: 0 0 15px rgba(255, 215, 0, 0.5);
            transition: all 0.3s ease;
        }

        .music-toggle:hover {
            box-shadow: 0 0 25px rgba(255, 215, 0, 0.8);
            transform: scale(1.1);
        }

        @media (max-width: 600px) {
            #typing {
                font-size: 18px;
            }

            .photos img {
                width: 150px;
                height: 200px;
            }

            #final {
                font-size: 16px;
            }
        }
    </style>
</head>
<body>
    <button class="music-toggle" id="musicToggle" title="Toggle Music">🎵</button>

    <div class="container">
        <div id="typing"></div>

        <div class="button-container">
            <button id="startBtn" onclick="startExperience()">Start ❤️</button>
        </div>

        <div class="photos" id="photos">
            <div class="photo-wrapper">
                <img src="https://via.placeholder.com/200x250/ff69b4/ffffff?text=Photo+1" alt="Memory 1">
            </div>
            <div class="photo-wrapper">
                <img src="https://via.placeholder.com/200x250/ff1493/ffffff?text=Photo+2" alt="Memory 2">
            </div>
        </div>

        <div id="final">
Eid muburak meine sameena jnav❤️😘
Meon khduai kre nai shft yme eid kei pss Bi kre ise kamyb IAS bnwin mh jdli Bi krn ise khndr jldi Kya kmi gse tms khdis😭🤲🏻🫂
Once Again meli jn mela bacha Eid Mubarak Mela bacha🥰😘
        </div>
    </div>

    <audio id="music" loop preload="none">
        <source src="https://www.fesliyanstudios.com/play-mp3/387" type="audio/mpeg">
        Your browser does not support the audio element.
    </audio>

    <script>
        const text = "Initializing Love System...\n\nLoading Memories...\n\nConnecting Heart...\n\nAccess Granted ❤️\n\nWelcome Sameena (Bubu)...";
        let currentIndex = 0;
        let isPlaying = false;

        function typeEffect() {
            const typingElement = document.getElementById("typing");
            if (currentIndex < text.length) {
                if (text.charAt(currentIndex) === '\n') {
                    typingElement.innerHTML += '<br>';
                } else {
                    typingElement.innerHTML += text.charAt(currentIndex);
                }
                currentIndex++;
                setTimeout(typeEffect, 50);
            }
        }

        function startExperience() {
            const startBtn = document.getElementById("startBtn");
            startBtn.disabled = true;
            startBtn.style.opacity = "0.6";
            
            const music = document.getElementById("music");
            music.play().catch(error => console.log("Audio autoplay prevented:", error));
            isPlaying = true;
            updateMusicButton();

            typeEffect();

            setTimeout(showPhotos, 4500);
        }

        function showPhotos() {
            const photosDiv = document.getElementById("photos");
            photosDiv.classList.add("show");
            setTimeout(showFinal, 3500);
        }

        function showFinal() {
            document.getElementById("typing").style.display = "none";
            document.getElementById("final").classList.add("show");
        }

        function updateMusicButton() {
            const btn = document.getElementById("musicToggle");
            const music = document.getElementById("music");
            btn.textContent = music.paused ? "🔇" : "🎵";
        }

        document.getElementById("musicToggle").addEventListener("click", function() {
            const music = document.getElementById("music");
            if (music.paused) {
                music.play().catch(error => console.log("Playback error:", error));
            } else {
                music.pause();
            }
            updateMusicButton();
        });

        // Create particles
        function createParticle() {
            const particle = document.createElement("div");
            particle.className = "particle";
            particle.style.left = Math.random() * 100 + "%";
            particle.style.top = "100vh";
            particle.style.animationDelay = Math.random() * 2 + "s";
            document.body.appendChild(particle);

            setTimeout(() => particle.remove(), 10000);
        }

        setInterval(createParticle, 150);

        // Update music button on load
        window.addEventListener("load", updateMusicButton);
    </script>
</body>
</html>
