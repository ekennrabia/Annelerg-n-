<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Canım Annem & Biricik Öğretmenim 🌸</title>
    
    <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@600;700&family=Playfair+Display:ital,wght@0,400;0,600&family=Poppins:wght@300;400;500;600&display=swap" rel="stylesheet">
    
    <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.6.0/dist/confetti.browser.min.js"></script>
    
    <style>
        * { box-sizing: border-box; margin: 0; padding: 0; }

        body { 
            font-family: 'Poppins', sans-serif; 
            /* Çok yumuşak, hareketli pastel bir arka plan */
            background: linear-gradient(-45deg, #fce4ec, #fbc2eb, #e6e9f0, #fdfbfb);
            background-size: 400% 400%;
            animation: gradientBG 15s ease infinite;
            color: #4a4a4a; overflow-x: hidden;
        }
        @keyframes gradientBG { 
            0% {background-position: 0% 50%;} 
            50% {background-position: 100% 50%;} 
            100% {background-position: 0% 50%;} 
        }

        /* Yükleniyor Ekranı (İlk açılışta çıkar) */
        #loader {
            position: fixed; top: 0; left: 0; width: 100vw; height: 100vh;
            background: #fce4ec; display: flex; flex-direction: column;
            justify-content: center; align-items: center; z-index: 9999;
            animation: fadeOut 1s ease 2s forwards;
        }
        .loader-heart { font-size: 5em; animation: heartbeat 1s infinite; }
        .loader-text { font-family: 'Dancing Script', cursive; font-size: 2.2em; color: #a15d68; margin-top: 20px; text-align: center; padding: 0 20px;}
        @keyframes heartbeat { 0%, 100% { transform: scale(1); } 50% { transform: scale(1.15); } }
        @keyframes fadeOut { to { opacity: 0; visibility: hidden; } }

        /* Ana Konteyner ve Cam Efekti Sınıfı */
        .container { max-width: 1000px; margin: 0 auto; padding: 40px 20px; }
        
        .glass {
            background: rgba(255, 255, 255, 0.55);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
            border-radius: 24px;
            border: 1px solid rgba(255, 255, 255, 0.6);
            box-shadow: 0 10px 40px rgba(183, 110, 121, 0.15);
            padding: 40px;
            margin-bottom: 50px;
        }

        /* Başlıklar */
        header { text-align: center; padding: 40px 20px 30px; animation: slideDown 1s ease 2s backwards; }
        @keyframes slideDown { from { opacity: 0; transform: translateY(-30px); } to { opacity: 1; transform: translateY(0); } }
        h1 { font-family: 'Dancing Script', cursive; font-size: 4.8em; color: #a15d68; margin-bottom: 5px; text-shadow: 2px 2px 10px rgba(255,255,255,0.8); line-height: 1.2;}
        .subtitle { font-family: 'Playfair Display', serif; font-size: 1.5em; font-style: italic; color: #666; }

        /* Spotify Bölümü */
        .spotify-container { max-width: 700px; margin: 0 auto 50px; padding: 20px; text-align: center; border-radius: 24px;}
        .spotify-title { margin-bottom: 15px; font-weight: 600; color: #a15d68; font-family: 'Playfair Display', serif; font-size: 1.2em;}

        /* Özel Mesaj Mektubu */
        .message-box { 
            text-align: center; line-height: 2.2; font-size: 1.25em; 
            font-family: 'Playfair Display', serif; font-style: italic; color: #444; 
            position: relative;
        }
        .message-box::before, .message-box::after { content: '❝'; font-size: 4em; color: rgba(161, 93, 104, 0.15); position: absolute; font-family: sans-serif; }
        .message-box::before { top: -10px; left: 10px; }
        .message-box::after { content: '❞'; bottom: -40px; right: 10px; }

        h2 { font-family: 'Dancing Script', cursive; font-size: 3.5em; color: #a15d68; text-align: center; margin-bottom: 30px; }

        /* Karne Alanı */
        .report-row { display: flex; justify-content: space-between; align-items: center; padding: 18px 0; border-bottom: 1px dashed rgba(161, 93, 104, 0.3); font-size: 1.15em; }
        .report-row:last-child { border-bottom: none; }
        .grade { font-weight: 700; color: #a15d68; font-family: 'Dancing Script', cursive; font-size: 1.6em; }

        /* Kuponlar */
        .coupon-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 30px; }
        .coupon { 
            cursor: pointer; transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            display: flex; flex-direction: column; align-items: center; justify-content: center;
            text-align: center; position: relative; overflow: hidden;
        }
        .coupon:hover { transform: translateY(-12px) scale(1.02); background: rgba(255, 255, 255, 0.8); border-color: #fff; box-shadow: 0 20px 40px rgba(183, 110, 121, 0.2);}
        .coupon i { font-size: 3em; margin-bottom: 15px; text-shadow: 2px 2px 5px rgba(0,0,0,0.1);}
        .coupon h3 { font-size: 1.4em; margin-bottom: 12px; color: #a15d68; font-family: 'Playfair Display', serif;}
        .coupon p { font-size: 0.95em; color: #555; line-height: 1.6; }
        
        .used { background: rgba(230, 230, 230, 0.5) !important; transform: none !important; box-shadow: none !important; cursor: not-allowed; border-color: transparent !important;}
        .used h3, .used p, .used i { color: #999 !important; text-decoration: line-through; text-shadow: none; }

        /* Büyük Kutlama Butonu */
        .btn-celebrate {
            display: block; margin: 70px auto 30px; padding: 20px 50px; border: none;
            background: linear-gradient(135deg, #a15d68, #e6a8d7); color: white;
            font-family: 'Dancing Script', cursive; font-size: 2.2em; border-radius: 50px;
            cursor: pointer; box-shadow: 0 10px 25px rgba(161, 93, 104, 0.4); transition: 0.4s;
        }
        .btn-celebrate:hover { transform: scale(1.08); box-shadow: 0 15px 35px rgba(161, 93, 104, 0.5); }

        footer { text-align: center; padding: 40px; font-family: 'Dancing Script', cursive; font-size: 2em; color: #a15d68; }

        /* Uçuşan Çiçekler */
        .petal { position: fixed; top: -10vh; z-index: -1; animation: fall linear forwards; opacity: 0.6; pointer-events: none; font-size: 1.5em;}
        @keyframes fall { to { transform: translateY(110vh) rotate(360deg); } }
        
        /* Mobil Uyum */
        @media (max-width: 600px) {
            h1 { font-size: 3.5em; }
            .glass { padding: 25px; }
            .report-row { flex-direction: column; align-items: flex-start; gap: 5px; }
            .grade { align-self: flex-end; }
        }
    </style>
</head>
<body>

    <div id="loader">
        <div class="loader-heart">🌸</div>
        <div class="loader-text">Dünyanın en kıymetli öğretmeni için hazırlanıyor...</div>
    </div>

    <div class="container">
        
        <header>
            <h1>Canım Annem</h1>
            <p class="subtitle">Hayatımın en güzel detayı, en güvenli limanım...</p>
        </header>

        <div class="spotify-container glass">
            <p class="spotify-title">🎧 Okumadan önce müziğimizi başlat...</p>
            <iframe style="border-radius:12px" src="https://open.spotify.com/embed/playlist/37i9dQZF1DWV7EzJMK2FUI?utm_source=generator&theme=0" width="100%" height="152" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
        </div>

        <div class="message-box glass">
            Hayatımdaki en karmaşık kodları bile bir bakışınla çözen, bana her zaman en büyük ilham olan canım annem... Sen bana sadece yürümeyi, konuşmayı değil; sevmeyi, güçlü olmayı ve hayata daima umutla bakmayı öğrettin. Öğrencilerine ışık olurken, benim dünyamı aydınlatmayı hiç ihmal etmedin. İyi ki benim annem, iyi ki benim ilk ve en değerli öğretmenimsin!
        </div>

        <h2>Öğretmen Karnesi</h2>
        <div class="report-card glass">
            <div class="report-row"><span>Sabır, Anlayış ve Şefkat</span> <span class="grade">Peki (100)</span></div>
            <div class="report-row"><span>Gizli Tariflerle Muhteşem Yemekler</span> <span class="grade">Peki (100)</span></div>
            <div class="report-row"><span>Hayat Rehberliği ve Kılavuzluk</span> <span class="grade">Peki (100)</span></div>
            <div class="report-row"><span>Benim Kahrımı Çekme Kapasitesi</span> <span class="grade">Yıldızlı Peki (100)</span></div>
        </div>

        <h2>Sana Özel Hediye Çekleri</h2>
        <p style="text-align: center; color: #777; margin-bottom: 30px; font-style: italic;">İstediğin çekin üzerine tıkla. (Asistanın hemen devreye girecek 😉)</p>
        
        <div class="coupon-grid">
            
            <div class="coupon glass" onclick="claim(this)">
                <i>💻</i>
                <h3>7/24 Teknik & Ev Asistanı</h3>
                <p>Telefonda bir şey bozulduğunda, akıllı tahta donduğunda veya o gün ev işleri biriktiğinde... Tüm işler bilgisayar mühendisi kızına emanet!</p>
            </div>

            <div class="coupon glass" onclick="claim(this)">
                <i>☕</i>
                <h3>Beyoğlu'nda Baş Başa</h3>
                <p>Beraber Beyoğlu sokaklarında harika bir yürüyüş yapıp, tatlı eşliğinde kahvelerimizi içerken uzun uzun sohbet edip dertleşme günü.</p>
            </div>

            <div class="coupon glass" onclick="claim(this)">
                <i>📺</i>
                <h3>Dizi Gecesi</h3>
                <p>Xu Kai veya Cheng Lei'nin o bebeksi yüzünü ekranda izleyip, mısır eşliğinde saatlerce dizi kritiği yapıp karakterleri çekiştirme hakkı!</p>
            </div>

            <div class="coupon glass" onclick="claim(this)">
                <i>📝</i>
                <h3>E-Okul & Sınav Terapisi</h3>
                <p>Sen yığınla sınav kağıdı okurken veya e-okul notları girerken; sınırsız sıcak çay/kahve servisi ve yorgunluk alıcı uzun omuz masajı.</p>
            </div>

        </div>

        <button class="btn-celebrate" onclick="celebrate()">Seni Çok Seviyorum! ❤️</button>
    </div>

    <footer>
        Anneler Günün Kutlu Olsun... 🌸
    </footer>

    <script>
        // Kupon Kullanma Efekti
        function claim(el) {
            if(!el.classList.contains('used')) {
                el.innerHTML = "<i>✅</i><h3>Sipariş Alındı!</h3><p>Hemen işleme konuluyor...</p>";
                el.classList.add('used');
                confetti({ particleCount: 40, spread: 60, origin: { y: 0.7 }, colors: ['#a15d68', '#fbc2eb', '#ffffff'] });
            }
        }

        // Büyük Buton Kutlaması
        function celebrate() {
            var duration = 3000;
            var end = Date.now() + duration;

            (function frame() {
                confetti({ particleCount: 5, angle: 60, spread: 55, origin: { x: 0 }, colors: ['#a15d68', '#fce4ec', '#ffd700'] });
                confetti({ particleCount: 5, angle: 120, spread: 55, origin: { x: 1 }, colors: ['#a15d68', '#fce4ec', '#ffd700'] });
                if (Date.now() < end) requestAnimationFrame(frame);
            }());
        }

        // Arka Planda Uçuşan Taç Yapraklar
        function createPetal() {
            const petal = document.createElement('div');
            petal.classList.add('petal');
            const emojis = ['🌸', '✨', '🤍'];
            petal.innerText = emojis[Math.floor(Math.random() * emojis.length)];
            petal.style.left = Math.random() * 100 + 'vw';
            petal.style.animationDuration = Math.random() * 5 + 7 + 's'; 
            document.body.appendChild(petal);
            setTimeout(() => { petal.remove(); }, 12000);
        }
        setInterval(createPetal, 1500);
    </script>
</body>
</html>
