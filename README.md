<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rabia'dan Canım Anneme Sürpriz 🌸</title>
    <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@600;700&family=Playfair+Display:ital,wght@0,400;0,600;1,400&family=Poppins:wght@300;400;500;600&display=swap" rel="stylesheet">
    <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.6.0/dist/confetti.browser.min.js"></script>
    <style>
        :root {
            --rose-gold: #b76e79;
            --rose-gold-dark: #a15d68;
            --soft-pink: #fff5f7;
            --cream: #fffdfa;
            --text-dark: #3a3a3a;
        }
        
        * { box-sizing: border-box; margin: 0; padding: 0; }

        /* Giriş Animasyonu */
        #loader {
            position: fixed; top: 0; left: 0; width: 100vw; height: 100vh;
            background-color: var(--soft-pink); display: flex; flex-direction: column;
            justify-content: center; align-items: center; z-index: 9999;
            animation: fadeOut 0.8s ease 2s forwards;
        }
        .loader-heart { font-size: 5em; animation: heartbeat 1s infinite; }
        @keyframes heartbeat { 0%, 100% { transform: scale(1); } 50% { transform: scale(1.2); } }
        @keyframes fadeOut { to { opacity: 0; visibility: hidden; } }

        body { 
            font-family: 'Poppins', sans-serif; background-color: var(--soft-pink); 
            background-image: url('https://www.transparenttextures.com/patterns/p6.png');
            color: var(--text-dark); overflow-x: hidden; scroll-behavior: smooth;
        }

        /* Sabit Müzik Kontrol Paneli */
        #music-panel {
            position: fixed; bottom: 25px; right: 25px; z-index: 2000;
            background: white; padding: 15px 20px; border-radius: 50px;
            box-shadow: 0 10px 30px rgba(183, 110, 121, 0.3); border: 2px solid var(--rose-gold);
            display: flex; align-items: center; gap: 15px;
        }
        .music-btn {
            background: var(--rose-gold); color: white; border: none; padding: 10px 20px;
            border-radius: 30px; cursor: pointer; font-weight: 600; font-size: 0.8em;
            transition: 0.3s;
        }
        .music-btn:hover { background: var(--rose-gold-dark); transform: scale(1.05); }

        /* Hero Bölümü */
        header { 
            height: 100vh; display: flex; flex-direction: column; justify-content: center; align-items: center;
            background: linear-gradient(rgba(255,245,247,0.7), rgba(255,253,250,0.9)), url('https://images.unsplash.com/photo-1490750967868-88aa4486c946?q=80&w=1600&auto=format&fit=crop') center/cover;
            text-align: center; padding: 20px;
        }
        h1 { font-size: 4.5em; font-family: 'Dancing Script', cursive; color: var(--rose-gold-dark); margin-bottom: 10px; }
        .hero-desc { font-family: 'Playfair Display', serif; font-size: 1.6em; color: #555; font-style: italic; }

        /* Bölümler */
        .section { padding: 100px 20px; max-width: 1100px; margin: 0 auto; }
        .card { 
            background: var(--cream); padding: 50px; border-radius: 30px; 
            box-shadow: 0 15px 50px rgba(0,0,0,0.03); border: 1px solid rgba(183, 110, 121, 0.1);
            margin-bottom: 50px; opacity: 0; transform: translateY(40px); transition: 0.8s ease-out;
        }
        .card.visible { opacity: 1; transform: translateY(0); }

        h2 { font-family: 'Dancing Script', cursive; font-size: 3em; color: var(--rose-gold); margin-bottom: 40px; }

        /* Galeri */
        .gallery { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 30px; }
        .img-container { background: white; padding: 15px; border-radius: 15px; box-shadow: 0 8px 20px rgba(0,0,0,0.05); }
        .img-container img { width: 100%; height: 350px; object-fit: cover; border-radius: 10px; }
        .img-caption { padding-top: 15px; font-family: 'Dancing Script', cursive; font-size: 1.8em; color: var(--rose-gold); }

        /* Yetenek Barları */
        .skill-box { margin-bottom: 30px; text-align: left; }
        .skill-label { font-weight: 600; display: flex; justify-content: space-between; margin-bottom: 10px; color: var(--rose-gold-dark); }
        .bar-bg { width: 100%; height: 14px; background: #eee; border-radius: 20px; overflow: hidden; }
        .bar-fill { height: 100%; background: linear-gradient(90deg, #e6a8d7, var(--rose-gold)); width: 0; transition: 2s cubic-bezier(0.1, 0.5, 0.1, 1); }

        /* Hediye Çekleri */
        .coupon-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 25px; }
        .coupon { 
            background: #fff; border: 2px dashed var(--rose-gold); padding: 30px; border-radius: 20px;
            cursor: pointer; transition: 0.4s; display: flex; flex-direction: column; gap: 10px;
        }
        .coupon:hover { background: var(--rose-gold); color: white; transform: translateY(-10px); }
        .coupon i { font-size: 2em; margin-bottom: 10px; }

        /* Konfeti Butonu */
        .celebrate-btn {
            background: linear-gradient(135deg, var(--rose-gold), var(--rose-gold-dark));
            color: white; border: none; padding: 20px 40px; border-radius: 50px;
            font-size: 1.5em; font-family: 'Dancing Script', cursive; cursor: pointer;
            box-shadow: 0 10px 30px rgba(183, 110, 121, 0.4); margin-top: 40px;
        }

        footer { padding: 100px 20px; font-family: 'Dancing Script', cursive; font-size: 2.5em; color: var(--rose-gold); }
    </style>
</head>
<body>

    <div id="loader">
        <div class="loader-heart">❤️</div>
        <div class="loader-text">Rabia'nın ilk öğretmeni için hazırlanıyor...</div>
    </div>

    <audio id="mainAudio" loop>
        <source src="https://cdn.pixabay.com/audio/2022/10/25/audio_5f308354a8.mp3" type="audio/mpeg">
    </audio>

    <div id="music-panel">
        <span style="font-size: 0.8em; font-weight: 600; color: #777;">Huzur Modu:</span>
        <button class="music-btn" onclick="togglePlay()">🎵 Müzik Başlat</button>
    </div>

    <header>
        <h1>Canım Annem</h1>
        <p class="hero-desc">Hayatımın ilk öğretmeni, en büyük şansım...</p>
        <div style="margin-top: 30px; font-size: 2em; color: var(--rose-gold); animation: bounce 2s infinite;">↓</div>
    </header>

    <div class="section">
        <div class="card reveal">
            <h2>Bizim Hikayemiz</h2>
            <div class="gallery">
                <div class="img-container">
                    <img src="https://images.unsplash.com/photo-1490750967868-88aa4486c946?q=80&w=600&auto=format&fit=crop" alt="Sevgi">
                    <div class="img-caption">Dünyanın En İyi Annesi</div>
                </div>
                <div class="img-container">
                    <img src="https://images.unsplash.com/photo-1512820790803-83ca734da794?q=80&w=600&auto=format&fit=crop" alt="Öğretmenlik">
                    <div class="img-caption">İlham Veren Öğretmenim</div>
                </div>
            </div>
            <p style="margin-top: 40px; line-height: 1.8; font-style: italic; font-family: 'Playfair Display', serif; font-size: 1.2em;">
                Senin o kutsal öğretmenlik sabrın ve bitmek bilmeyen şefkatin olmasaydı, ben bugün bu yolları asla böyle emin adımlarla yürüyemezdim. Seninle izlediğimiz her C-Drama, okuduğun her sınav kağıdı, bana kattığın her kelime bugün benim en büyük hazinem.
            </p>
        </div>

        <div class="card reveal" id="stats-card">
            <h2>Süper Güç Analizi</h2>
            <div class="skill-box">
                <div class="skill-label"><span>Sonsuz Sabır Kapasitesi</span><span>100%</span></div>
                <div class="bar-bg"><div class="bar-fill" data-percent="100%"></div></div>
            </div>
            <div class="skill-box">
                <div class="skill-label"><span>Lezzet ve Mutfak Stratejisi</span><span>100%</span></div>
                <div class="bar-bg"><div class="bar-fill" data-percent="100%"></div></div>
            </div>
            <div class="skill-box">
                <div class="skill-label"><span>Öğrencilere (ve bana) Adanmış Bir Hayat</span><span>100%</span></div>
                <div class="bar-bg"><div class="bar-fill" data-percent="100%"></div></div>
            </div>
        </div>

        <div class="card reveal">
            <h2>Geleneksel Hediye Çeklerin 🎟️</h2>
            <div class="coupon-grid">
                <div class="coupon" onclick="claim(this)">
                    <span style="font-size: 2em;">📺</span>
                    <h3>C-Drama Gecesi</h3>
                    <p>Cheng Lei veya Xu Kai'nin o bebeksi yüzünü sabaha kadar izleme ve karakterleri beraber çekiştirme hakkı!</p>
                </div>
                <div class="coupon" onclick="claim(this)">
                    <span style="font-size: 2em;">☕</span>
                    <h3>E-Okul Mesaisi</h3>
                    <p>Sen notları girerken yanında hiç bitmeyen sıcak çay ve kahve servisi garantisi.</p>
                </div>
                <div class="coupon" onclick="claim(this)">
                    <span style="font-size: 2em;">🧹</span>
                    <h3>Ev İşleri Tatili</h3>
                    <p>Bugün tüm operasyonel işler bilgisayar mühendisi asistanına (bana) ait.</p>
                </div>
            </div>
        </div>

        <div style="text-align: center;">
            <button class="celebrate-btn" onclick="celebrate()">Seni Çok Seviyorum! (Tıkla ❤️)</button>
        </div>
    </div>

    <footer>
        Anneler Günün Kutlu Olsun Canım Annem... 🌸
    </footer>

    <script>
        const audio = document.getElementById('mainAudio');
        let playing = false;

        function togglePlay() {
            if(!playing) {
                audio.play().then(() => {
                    playing = true;
                    document.querySelector('.music-btn').innerText = "⏸️ Müziği Durdur";
                }).catch(e => alert("Lütfen cihaz sesini açın ve tekrar deneyin!"));
            } else {
                audio.pause();
                playing = false;
                document.querySelector('.music-btn').innerText = "🎵 Müziği Başlat";
            }
        }

        // Kaydırma Animasyonları
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if(entry.isIntersecting) {
                    entry.target.classList.add('visible');
                    if(entry.target.id === 'stats-card') {
                        entry.target.querySelectorAll('.bar-fill').forEach(bar => {
                            bar.style.width = bar.getAttribute('data-percent');
                        });
                    }
                }
            });
        }, { threshold: 0.2 });

        document.querySelectorAll('.reveal').forEach(el => observer.observe(el));

        function claim(el) {
            if(!el.classList.contains('used')) {
                el.style.background = '#e9ecef';
                el.style.color = '#adb5bd';
                el.style.textDecoration = 'line-through';
                el.innerHTML = "<h3>✅ İsteğin Alındı!</h3><p>Hemen işleme konuluyor...</p>";
                el.classList.add('used');
            }
        }

        function celebrate() {
            confetti({
                particleCount: 150,
                spread: 70,
                origin: { y: 0.6 },
                colors: ['#b76e79', '#fce4ec', '#ffffff']
            });
        }
    </script>
</body>
</html>
