<!doctype html>
<html lang="id">
    <head>
        <meta charset="UTF-8" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />
        <title>💖 Untuk Sayangku 💖</title>

        <style>
            * {
                margin: 0;
                padding: 0;
                box-sizing: border-box;
                font-family: "Segoe UI", sans-serif;
            }

            body {
                overflow-x: hidden;
                min-height: 100vh;
                background: linear-gradient(135deg, #ffdde1, #ee9ca7, #ffd6e7);
                color: white;
            }

            /* INTRO */
            #intro {
                position: fixed;
                inset: 0;
                background: linear-gradient(135deg, #ff8fb1, #ffb6c1);
                display: flex;
                flex-direction: column;
                justify-content: center;
                align-items: center;
                z-index: 99999;
            }

            #intro h1 {
                font-size: 3rem;
                text-align: center;
                padding: 0 20px;
                margin-bottom: 20px;
            }

            #openBtn {
                padding: 15px 40px;
                border: none;
                border-radius: 50px;
                font-size: 18px;
                background: white;
                color: #ff4f93;
                font-weight: bold;
                cursor: pointer;
            }

            /* GLOW */
            .glow {
                position: fixed;
                border-radius: 50%;
                filter: blur(120px);
                opacity: 0.4;
                z-index: -1;
            }
            .g1 {
                width: 350px;
                height: 350px;
                background: #ff69b4;
                top: -100px;
                left: -100px;
            }
            .g2 {
                width: 300px;
                height: 300px;
                background: #fff0f5;
                right: -100px;
                top: 30%;
            }
            .g3 {
                width: 300px;
                height: 300px;
                background: #ffc0cb;
                bottom: -100px;
                left: 40%;
            }

            /* STAR */
            .star {
                position: fixed;
                background: white;
                border-radius: 50%;
                animation: blink 2s infinite;
                z-index: -2;
            }
            @keyframes blink {
                50% {
                    opacity: 0.2;
                }
            }

            /* FALL */
            .fall {
                position: fixed;
                top: -50px;
                font-size: 24px;
                animation: fall linear infinite;
                pointer-events: none;
            }
            @keyframes fall {
                from {
                    transform: translateY(-50px);
                }
                to {
                    transform: translateY(120vh);
                }
            }

            /* CONTAINER */
            .container {
                text-align: center;
                padding: 25px;
            }

            .title {
                font-size: 3rem;
                text-shadow: 0 0 15px rgba(255, 255, 255, 0.7);
            }

            .subtitle {
                margin: 10px 0 30px;
            }

            /* SLIDER */
            .slider {
                width: 300px;
                height: 300px;
                margin: auto;
                border-radius: 50%;
                overflow: hidden;
                border: 8px solid white;
                box-shadow: 0 10px 35px rgba(255, 255, 255, 0.4);
            }

            .slider img {
                width: 100%;
                height: 100%;
                object-fit: cover;
                image-rendering: auto;
            }

            /* CARD */
            .card {
                max-width: 850px;
                margin: 40px auto;
                padding: 30px;
                border-radius: 25px;
                background: rgba(255, 255, 255, 0.15);
                backdrop-filter: blur(20px);
                border: 1px solid rgba(255, 255, 255, 0.2);
            }

            .typing {
                min-height: 100px;
                margin-top: 15px;
            }
            .countdown {
                margin-top: 15px;
                font-weight: bold;
            }

            .love-btn {
                margin-top: 20px;
                padding: 15px;
                width: 100%;
                border: none;
                border-radius: 50px;
                background: #ff4f93;
                color: white;
                font-size: 16px;
            }

            /* MARQUEE */
            marquee {
                margin: 25px 0;
                font-weight: bold;
            }

            /* ===== GALLERY PREMIUM ===== */
            .gallery-title {
                text-align: center;
                margin-top: 50px;
            }

            .gallery-title h2 {
                font-size: 2.2rem;
            }

            .gallery {
                max-width: 1300px;
                margin: auto;
                padding: 15px;
                columns: 4 250px;
                column-gap: 15px;
            }

            .photo-card {
                background: white;
                border-radius: 20px;
                padding: 10px;
                margin-bottom: 15px;
                break-inside: avoid;
                cursor: pointer;
                transform: rotate(calc(var(--r) * 1deg));
                transition: 0.3s;
                box-shadow: 0 10px 25px rgba(0, 0, 0, 0.15);
            }

            .photo-card:hover {
                transform: rotate(0) scale(1.05);
                box-shadow: 0 20px 40px rgba(255, 105, 180, 0.4);
            }

            .photo-card img {
                width: 100%;
                border-radius: 15px;
            }

            .photo-caption {
                color: #ff4f93;
                font-weight: bold;
                text-align: center;
                margin-top: 8px;
            }

            /* LIGHTBOX */
            #lightbox {
                position: fixed;
                inset: 0;
                display: none;
                justify-content: center;
                align-items: center;
                background: rgba(0, 0, 0, 0.9);
                z-index: 999999;
            }

            #lightbox img {
                max-width: 90%;
                max-height: 90%;
                border-radius: 20px;
            }

            /* POPUP */
            .popup {
                display: none;
                position: fixed;
                top: 50%;
                left: 50%;
                transform: translate(-50%, -50%);
                background: white;
                color: #ff4f93;
                padding: 25px;
                border-radius: 20px;
                z-index: 99999;
            }

            /* BOTTOM NAV */
            .bottom-nav {
                position: fixed;
                bottom: 10px;
                left: 50%;
                transform: translateX(-50%);
                background: rgba(255, 255, 255, 0.2);
                backdrop-filter: blur(20px);
                border-radius: 50px;
                display: flex;
                gap: 25px;
                padding: 12px 18px;
                z-index: 999999;
            }

            .bottom-nav div {
                font-size: 22px;
                cursor: pointer;
            }

            .bottom-nav div:active {
                transform: scale(1.3);
            }

            /* HP MODE */
            @media (max-width: 768px) {
                body {
                    overflow-x: hidden;
                }

                .container {
                    padding: 15px;
                }

                .title {
                    font-size: 1.8rem;
                    line-height: 1.3;
                }

                .subtitle {
                    font-size: 14px;
                }

                .slider {
                    width: 95%;
                    max-width: 340px;
                    height: 340px;
                    border-radius: 20px;
                }

                .card {
                    width: 100%;
                    padding: 20px;
                    margin: 25px auto;
                }

                .card h2 {
                    font-size: 22px;
                }

                .typing {
                    font-size: 15px;
                    line-height: 1.8;
                }

                .countdown {
                    font-size: 15px;
                }

                .love-btn {
                    font-size: 16px;
                    padding: 14px;
                }

                .gallery-title h2 {
                    font-size: 1.7rem;
                }

                .gallery {
                    columns: 2;
                    column-gap: 10px;
                    padding: 10px;
                }

                .photo-card {
                    transform: none !important;
                    margin-bottom: 10px;
                }

                .photo-caption {
                    font-size: 13px;
                }

                marquee {
                    font-size: 14px;
                }

                .bottom-nav {
                    width: 92%;
                    justify-content: space-around;
                    gap: 10px;
                    padding: 12px;
                }

                .bottom-nav div {
                    font-size: 24px;
                }

                #intro h1 {
                    font-size: 2rem;
                    padding: 0 15px;
                }

                #openBtn {
                    width: 220px;
                    font-size: 16px;
                }
            }

            /* HP KECIL */
            @media (max-width: 480px) {
                .title {
                    font-size: 1.5rem;
                }

                .subtitle {
                    font-size: 13px;
                }

                .slider {
                    width: 95%;
                    height: 280px;
                }

                .gallery {
                    columns: 1;
                }

                .card {
                    padding: 15px;
                }

                .typing {
                    font-size: 14px;
                }

                .countdown {
                    font-size: 14px;
                }

                .bottom-nav {
                    width: 95%;
                }
            }
        </style>
    </head>

    <body>
        <!-- INTRO -->
        <div id="intro">
            <h1>🎁 Hadiah Untuk Kamu 💖</h1>
            <button id="openBtn">Buka ❤️</button>
        </div>

        <div class="glow g1"></div>
        <div class="glow g2"></div>
        <div class="glow g3"></div>

        <audio id="music" loop>
            <source src="lagu.mp3" />
        </audio>

        <div class="container">
            <h1 class="title">💖 Untuk Sayangku 💖</h1>
            <p class="subtitle">Website cinta spesial 🌸</p>

            <div class="slider">
                <img id="slide" src="olla 1.jpeg" />
            </div>

            <div class="card">
                <h2>💌 Surat Cinta</h2>
                <div class="typing" id="typing"></div>
                <div class="countdown" id="countdown"></div>
                <button class="love-btn" onclick="showLove()">
                    ❤️ Aku Sayang Kamu
                </button>
            </div>
        </div>

        <marquee>💖 Kamu Cantik 💖 Kamu Istimewa 💖 Aku Sayang Kamu 💖</marquee>

        <div class="gallery-title">
            <h2>📸 Galeri Kenangan 📸</h2>
        </div>

        <div class="gallery">
            <div class="photo-card" style="--r: -3" onclick="openPhoto(this)">
                <img src="olla 1.jpeg" />
                <div class="photo-caption">💖 Senyum</div>
            </div>

            <div class="photo-card" style="--r: 2" onclick="openPhoto(this)">
                <img src="olla 2.jpeg" />
                <div class="photo-caption">🌸 Cantik</div>
            </div>

            <div class="photo-card" style="--r: -2" onclick="openPhoto(this)">
                <img src="olla 3.jpeg" />
                <div class="photo-caption">✨ Momen</div>
            </div>

            <div class="photo-card" style="--r: 3" onclick="openPhoto(this)">
                <img src="olla 4.jpeg" />
                <div class="photo-caption">❤️ Kamu</div>
            </div>

            <div class="photo-card" style="--r: -3" onclick="openPhoto(this)">
                <img src="olla 5.jpeg" />
                <div class="photo-caption">🥰 Sayang</div>
            </div>

            <div class="photo-card" style="--r: 2" onclick="openPhoto(this)">
                <img src="olla 6.jpeg" />
                <div class="photo-caption">💞 Manis</div>
            </div>

            <div class="photo-card" style="--r: -2" onclick="openPhoto(this)">
                <img src="olla 7.jpeg" />
                <div class="photo-caption">🌷 Bidadari</div>
            </div>

            <div class="photo-card" style="--r: 3" onclick="openPhoto(this)">
                <img src="olla 8.jpeg" />
                <div class="photo-caption">💗 Istimewa</div>
            </div>

            <div class="photo-card" style="--r: -3" onclick="openPhoto(this)">
                <img src="olla 9.jpeg" />
                <div class="photo-caption">✨ Favorit</div>
            </div>

            <div class="photo-card" style="--r: 2" onclick="openPhoto(this)">
                <img src="olla 10.jpeg" />
                <div class="photo-caption">❤️ Forever</div>
            </div>
        </div>

        <div id="lightbox" onclick="closePhoto()">
            <img id="lightboxImg" />
        </div>

        <div class="popup" id="popup">
            <h2>❤️ Aku Juga Sayang Kamu ❤️</h2>
        </div>

        <!-- BOTTOM NAV -->
        <div class="bottom-nav">
            <div onclick="scrollToTop()">🏠</div>
            <div
                onclick="
                    document
                        .querySelector('.gallery-title')
                        .scrollIntoView({ behavior: 'smooth' })
                "
            >
                📸
            </div>
            <div
                onclick="
                    document
                        .querySelector('.card')
                        .scrollIntoView({ behavior: 'smooth' })
                "
            >
                💌
            </div>
            <div onclick="showLove()">❤️</div>
        </div>

        <script>
            /* OPEN */
            document.getElementById("openBtn").onclick = () => {
                document.getElementById("intro").style.display = "none";
                document.getElementById("music").play();
            };

            /* STAR */
            for (let i = 0; i < 80; i++) {
                let s = document.createElement("div");
                s.className = "star";
                s.style.width = Math.random() * 3 + "px";
                s.style.height = s.style.width;
                s.style.left = Math.random() * 100 + "vw";
                s.style.top = Math.random() * 100 + "vh";
                document.body.appendChild(s);
            }

            /* FALL */
            for (let i = 0; i < 30; i++) {
                let f = document.createElement("div");
                f.className = "fall";
                f.innerHTML = Math.random() > 0.5 ? "💖" : "🌸";
                f.style.left = Math.random() * 100 + "vw";
                f.style.animationDuration = 5 + Math.random() * 8 + "s";
                document.body.appendChild(f);
            }

            /* SLIDE */
            const photos = [
                "olla 1.jpeg",
                "olla 2.jpeg",
                "olla 3.jpeg",
                "olla 4.jpeg",
                "olla 5.jpeg",
                "olla 6.jpeg",
                "olla 7.jpeg",
                "olla 8.jpeg",
                "olla 9.jpeg",
                "olla 10.jpeg",
            ];
            let i = 0;
            setInterval(() => {
                i = (i + 1) % photos.length;
                document.getElementById("slide").src = photos[i];
            }, 2500);

            /* TYPE */
            const text =
                "Terima kasih sudah hadir di hidupku. Kamu adalah alasan aku bahagia setiap hari ❤️";
            let t = 0;
            function type() {
                if (t < text.length) {
                    document.getElementById("typing").innerHTML += text[t++];
                    setTimeout(type, 40);
                }
            }
            type();

            /* COUNT */
            const startDate = new Date("2025-01-01");
            setInterval(() => {
                let d = Math.floor((new Date() - startDate) / 86400000);
                document.getElementById("countdown").innerText =
                    "💞 " + d + " hari bersama 💞";
            }, 1000);

            /* LOVE */
            function showLove() {
                document.getElementById("popup").style.display = "block";
                setTimeout(
                    () =>
                        (document.getElementById("popup").style.display =
                            "none"),
                    3000,
                );
            }

            /* LIGHTBOX */
            function openPhoto(card) {
                document.getElementById("lightboxImg").src =
                    card.querySelector("img").src;
                document.getElementById("lightbox").style.display = "flex";
            }
            function closePhoto() {
                document.getElementById("lightbox").style.display = "none";
            }

            /* SCROLL */
            function scrollToTop() {
                window.scrollTo({ top: 0, behavior: "smooth" });
            }
        </script>
    </body>
</html>
