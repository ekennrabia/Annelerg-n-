<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Canım Annem & Biricik Öğretmenim 🌸</title>
    <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@600;700&family=Playfair+Display:ital,wght@0,400;0,600;1,400&family=Poppins:wght@300;400;500;600&display=swap" rel="stylesheet">
    <style>
        :root {
            --rose-gold: #b76e79;
            --rose-gold-dark: #a15d68;
            --soft-pink: #fff5f7;
            --cream: #fffdfa;
            --text-dark: #3a3a3a;
            --text-light: #7f8c8d;
        }
        
        * { box-sizing: border-box; margin: 0; padding: 0; }

        /* Yükleniyor Ekranı */
        #loader {
            position: fixed; top: 0; left: 0; width: 100vw; height: 100vh;
            background-color: var(--soft-pink); display: flex; flex-direction: column;
            justify-content: center; align-items: center; z-index: 9999;
            animation: fadeOut 1s ease 2.5s forwards;
        }
        .loader-heart { font-size: 4em; animation: heartbeat 1s infinite; }
        .loader-text { font-family: 'Dancing Script', cursive; font-size: 2em; color: var(--rose-gold); margin-top: 20px; text-align: center; padding: 0 20px; }
        
        @keyframes heartbeat { 0% { transform: scale(1); } 50% { transform: scale(1.2); } 100% { transform: scale(1); } }
        @keyframes fadeOut { to { opacity: 0; visibility: hidden; } }

        body { 
            font-family: 'Poppins', sans-serif; background-color: var(--soft-pink); 
            background-image: url('https://www.transparenttextures.com/patterns/p6.png');
            color: var(--text-dark); overflow-x: hidden; scroll-behavior: smooth;
        }

        /* Sabit Müzik Butonu */
        #music-control {
            position: fixed; top: 20px; right: 20px; z-index: 2000;
            background: linear-gradient(135deg, #e6a8d7 0%, var(--rose-gold) 100%);
            color: white; border: none; padding: 12px 25px; border-radius: 50px;
            font-family: 'Poppins', sans-serif; font-weight: 500; font-size: 0.9em;
            cursor: pointer; box-shadow: 0 6px 20px rgba(183, 110, 121, 0.3); transition: all 0.4s ease;
        }
        #music-control:hover { transform: scale(1.05) translateY(-2px); box-shadow: 0 8px 25px rgba(183, 110, 121, 0.4); }

        /* Hero (Giriş) Bölümü */
        header { 
            height: 100vh; display: flex; flex-direction: column; justify-content: center; align-items: center;
            background: linear-gradient(to bottom, rgba(255,245,247,0.8), rgba(255,253,250,1)), url('https://images.unsplash.com/photo-1518118042469-d41d15444e21?q=80&w=1600&auto=format&fit=crop') center/cover;
            text-align: center; padding: 20px;
        }
        h1 { font-size: 5vw; margin-bottom: 10px; font-family: 'Dancing Script', cursive; color: var(--rose-gold-dark); text-shadow: 2px 2px 10px rgba(255,255,255,0.8); }
        @media (max-width: 768px) { h1 { font-size: 3.5em; } }
        p.subtitle { font-family: 'Playfair Display', serif; font-size: 1.5em; font-style: italic; color: #555; background: rgba(255,255,255,0.7); padding: 10px 20px; border-radius: 30px; }
        
        .scroll-down { position: absolute; bottom: 30px; font-size: 2em; color: var(--rose-gold); animation: bounce 2s infinite; }
        @keyframes bounce { 0%, 20%, 50%, 80%, 100% { transform: translateY(0); } 40% { transform: translateY(-20px); } 60% { transform: translateY(-10px); } }

        /* Ortak Konteyner Yapısı */
        .section { padding: 80px 20px; display: flex; justify-content: center; }
        .container { 
            max-width: 1000px; width: 100%; padding: 50px; background: var(--cream); 
            border-radius: 25px; box-shadow: 0 15px 40px rgba(0,0,0,0.05); border: 1px solid rgba(183, 110, 121, 0.1);
            text-align: center; transform: translateY(30px); opacity: 0; transition: all 0.8s ease-out;
        }
        .container.visible { transform: translateY(0); opacity: 1; }

        h2 { 
            color: var(--rose-gold); padding-bottom: 15px; display: inline-block; 
            margin-bottom: 40px; font-family: 'Dancing Script', cursive; font-size: 3em; position: relative;
        }
        h2::after { content: ''; position: absolute; bottom: 0; left: 50%; transform: translateX(-50%); width: 60%; height: 2px; background: linear-gradient(90deg, transparent, var(--rose-gold), transparent); }

        /* Fotoğraf Galerisi */
        .gallery { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 30px; }
        .photo-frame { background-color: white; padding: 15px; box-shadow: 0 10px 25px rgba(0,0,0,0.06); transition: all 0.4s ease; border-radius: 15px; border: 1px solid #f0f0f0; }
        .photo-frame:hover { transform: translateY(-10px) scale(1.02); box-shadow: 0 15px 35px rgba(183, 110, 121, 0.15); z-index: 2; }
        .photo-frame img { width: 100%; height: 300px; object-fit: cover; border-radius: 10px; }
        .photo-caption { padding-top: 15px; font-family: 'Dancing Script', cursive; font-size: 1.8em; color: var(--rose-gold-dark); font-weight: 600; }

        /* Mektup */
        .letter { background-color: #fffcf7; padding: 40px; font-style: italic; text-align: left; line-height: 2.2; font-size: 1.2em; border-left: 5px solid var(--rose-gold); position: relative; border-radius: 0 15px 15px 0; font-family: 'Playfair Display', serif; }

        /* Süper Güç Barları */
        .skills-container { text-align: left; padding: 20px 0; }
        .skill { margin-bottom: 25px; }
        .skill-name { font-weight: 600; font-size: 1.1em; color: var(--rose-gold-dark); display: flex; justify-content: space-between; margin-bottom: 8px; font-family: 'Playfair Display', serif;}
        .skill-bar { width: 100%; height: 12px; background-color: #f0e6e8; border-radius: 10px; overflow: hidden; }
        .skill-fill { height: 100%; background: linear-gradient(90deg, #e6a8d7, var(--rose-gold)); width: 0; transition: width 2s ease-in-out; border-radius: 10px; }

        /* Karne Tablosu */
        .report-card { border: 2px dashed rgba(183, 110, 121, 0.4); padding: 30px; border-radius: 15px; background-color: white; }
        .report-card-row { display: flex; justify-content: space-between; align-items: center; border-bottom: 1px solid rgba(183, 110, 121, 0.1); padding: 15px 0; font-size: 1.1em; text-align: left;}
        .report-card-row:last-child { border-bottom: none; }
        .grade { color: #2ecc71; font-weight: 700; font-family: 'Dancing Script', cursive; font-size: 1.5em;}

        /* Kuponlar */
        .coupons { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 25px; }
        .coupon { background: white; border: 2px solid rgba(183, 110, 121, 0.2); padding: 30px 20px; border-radius: 15px; cursor: pointer; transition: all 0.4s ease; color: var(--rose-gold-dark); display: flex; align-items: center; justify-content: center; text-align: center; min-height: 120px; box-shadow: 0 5px 15px rgba(0,0,0,0.03); font-size: 1.1em; font-weight: 500; }
        .coupon:hover { background-color: var(--rose-gold); color: white; transform: translateY(-7px); box-shadow: 0 12px 30px rgba(183, 110, 121, 0.2); }
        .used { background-color: #e0e0e0 !important; color: #888 !important; cursor: not-allowed; text-decoration: line-through; transform: translateY(0) !important; box-shadow: none !important; border-color: #ccc !important;}
        
        footer { padding: 60px 20px; color: var(--rose-gold); font-family: 'Dancing Script', cursive; font-size: 2.5em; font-weight: 700; text-align: center; background: rgba(255,255,255,0.5);}
        
        /* Arka plan animasyonu */
        .falling-item { position: fixed; top: -10vh; z-index: -1; animation: fall linear forwards; opacity: 0.4; pointer-events: none; }
        @keyframes fall { to { transform: translateY(110vh) rotate(360deg); } }
    </style>
</head>
<body>

    <div id="loader">
        <div class="loader-heart">❤️</div>
        <div class="loader-text">Dünyanın en iyi annesi için sevgiyle hazırlanıyor...</div>
    </div>

    <audio id="bgMusic" loop preload="auto">
        <source src="https://upload.wikimedia.org/wikipedia/commons/c/c8/Frederic_Chopin_-_Nocturne_Op._9%2C_No._2.ogg" type="audio/ogg">
    </audio>

    <button id="music-control" onclick="toggleMusic()">🎵 Müziği Başlat</button>

    <header>
        <h1>Canım Annem</h1>
        <p class="subtitle">Hayatımın ilk öğretmeni, en güvenli limanım...</p>
        <div class="scroll-down">↓</div>
    </header>
    
    <section class="section">
        <div class="container animate-on-scroll">
            <h2>Seninle Her Anımız Özel</h2>
            <div class="gallery">
                <div class="photo-frame">
                    <img src="https://images.unsplash.com/photo-1596464716127-f2a82984de30?q=80&w=600&auto=format&fit=crop" alt="Anne ve Çocuk">
                    <div class="photo-caption">En Güçlü Destekçim</div>
                </div>
                <div class="photo-frame">
                    <img src="https://images.unsplash.com/photo-1532012197267-da84d127e765?q=80&w=600&auto=format&fit=crop" alt="Kitaplar ve Çiçek">
                    <div class="photo-caption">Biricik Öğretmenim</div>
                </div>
            </div>
            
            <div class="letter" style="margin-top: 50px;">
                Bana sadece yürümeyi, konuşmayı değil; sevmeyi, güçlü olmayı ve hayata gülümseyerek bakmayı da sen öğrettin. Nöbetçi olduğun o yorucu günlerde, sınav kağıdı okuduğun uykusuz gecelerde bile bana ayıracak vaktin, verecek şefkatin hep vardı. Öğrencilerine ışık olurken, eve gelip benim dünyamı da aydınlatmayı hiç unutmadın. İyi ki benim annemsin!
            </div>
        </div>
    </section>

    <section class="section">
        <div class="container animate-on-scroll" id="skills-section">
            <h2>Annemin Kapasite Raporu</h2>
            <div class="skills-container">
                <div class="skill">
                    <div class="skill-name"><span>Sınırsız Sevgi & Şefkat</span><span>%100</span></div>
                    <div class="skill-bar"><div class="skill-fill" data-width="100%"></div></div>
                </div>
                <div class="skill">
                    <div class="skill-name"><span>Öğretmen Sabrı (Benimle Uğraşma Kapasitesi)</span><span>%100</span></div>
                    <div class="skill-bar"><div class="skill-fill" data-width="100%"></div></div>
                </div>
                <div class="skill">
                    <div class="skill-name"><span>Gizli Tariflerle Muhteşem Yemek Yapma</span><span>%100</span></div>
                    <div class="skill-bar"><div class="skill-fill" data-width="100%"></div></div>
                </div>
            </div>

            <h2 style="margin-top: 50px;">2026 Yılı Değerlendirme Karnesi</h2>
            <div class="report-card">
                <div class="report-card-row"><span>Sabır ve Anlayış</span> <span class="grade">Peki (100)</span></div>
                <div class="report-card-row"><span>Muhteşem Yemekler</span> <span class="grade">Peki (100)</span></div>
                <div class="report-card-row"><span>Hayat Rehberliği (Öğretmenlik)</span> <span class="grade">Peki (100)</span></div>
                <div class="report-card-row"><span>Fedakarlık</span> <span class="grade">Yıldızlı Peki (100)</span></div>
            </div>
        </div>
    </section>

    <section class="section">
        <div class="container animate-on-scroll">
            <h2>Sana Özel Hediye Çekleri</h2>
            <p style="margin-bottom: 40px; font-style: italic; color: var(--text-light);">Kullanmak istediğin çekin üzerine tıkla. (Nöbetçi evladın hemen yerine getirecek 😉)</p>
            <div class="coupons">
                <div class="coupon" onclick="useCoupon(this)">E-Okul Nöbetinde<br>Sınırsız Çay/Kahve Servisi ☕</div>
                <div class="coupon" onclick="useCoupon(this)">Cheng Lei veya Xu Kai'nin o bebeksi yüzünü izleyip karakterleri çekiştireceğimiz C-Drama Maratonu 📺🍿</div>
                <div class="coupon" onclick="useCoupon(this)">Bugün Bütün Ev İşleri<br>Bende (Sen Sadece Dinlen) 🧹</div>
                <div class="coupon" onclick="useCoupon(this)">Okul Yorgunluğunu Alıcı<br>Uzun Omuz Masajı 💆‍♀️</div>
            </div>
        </div>
    </section>

    <footer>
        Seni Çok Seviyorum... 🌸
    </footer>

    <script>
        // Müzik Kontrolü
        let isPlaying = false;
        const bgMusic = document.getElementById('bgMusic');
        const musicBtn = document.getElementById('music-control');
        bgMusic.volume = 0.4; 

        function toggleMusic() {
            if (isPlaying) {
                bgMusic.pause();
                musicBtn.innerHTML = '🎵 Müziği Başlat';
                musicBtn.style.background = 'linear-gradient(135deg, #e6a8d7 0%, var(--rose-gold) 100%)';
            } else {
                bgMusic.play().catch(() => alert("Lütfen cihazınızın sesinin açık olduğundan emin olun."));
                musicBtn.innerHTML = '⏸️ Müziği Durdur';
                musicBtn.style.background = '#e74c3c'; 
            }
            isPlaying = !isPlaying;
        }

        // Çek Kullanma Fonksiyonu
        function useCoupon(element) {
            if (!element.classList.contains('used')) {
                element.innerHTML = '✅ İsteğin Alındı!';
                element.classList.add('used');
                element.style.transform = 'scale(0.95)';
                setTimeout(() => { element.style.transform = 'scale(1)'; }, 200);
            }
        }

        // Scroll (Kaydırma) Animasyonları
        const observerOptions = { root: null, rootMargin: '0px', threshold: 0.2 };
        const observer = new IntersectionObserver((entries, observer) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                    // Eğer Süper Güçler bölümüyse barları doldur
                    if (entry.target.id === 'skills-section') {
                        const fills = entry.target.querySelectorAll('.skill-fill');
                        fills.forEach((fill, index) => {
                            setTimeout(() => { fill.style.width = fill.getAttribute('data-width'); }, index * 300);
                        });
                    }
                    observer.unobserve(entry.target);
                }
            });
        }, observerOptions);

        document.querySelectorAll('.animate-on-scroll').forEach(el => observer.observe(el));

        // Arka Plan Efekti
        function createFallingItem() {
            const item = document.createElement('div');
            item.classList.add('falling-item');
            const emojis = ['🌸', '✨', '🤍']; 
            item.innerText = emojis[Math.floor(Math.random() * emojis.length)];
            item.style.left = Math.random() * 100 + 'vw';
            item.style.animationDuration = Math.random() * 5 + 6 + 's'; 
            item.style.fontSize = (Math.random() * 1 + 0.8) + 'rem'; 
            document.body.appendChild(item);
            setTimeout(() => { item.remove(); }, 11000);
        }
        setInterval(createFallingItem, 1200); 
    </script>
</body>
</html>
