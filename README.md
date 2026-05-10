<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Canım Annem & En Değerli Öğretmenim 🌸</title>
    <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@600;700&family=Playfair+Display:ital,wght@0,400;0,600;1,400&family=Poppins:wght@300;400;500&display=swap" rel="stylesheet">
    <style>
        :root {
            --rose-gold: #b76e79;
            --rose-gold-dark: #a15d68;
            --soft-pink: #fff5f7;
            --cream: #fffdfa;
            --text-dark: #3a3a3a;
            --text-light: #7f8c8d;
        }
        
        * { box-sizing: border-box; }

        body { 
            font-family: 'Poppins', sans-serif; /* Ana metin fontu */
            background-color: var(--soft-pink); 
            background-image: url('https://www.transparenttextures.com/patterns/p6.png'); /* Zarif doku */
            color: var(--text-dark); 
            margin: 0; padding: 0; text-align: center; overflow-x: hidden; 
            opacity: 0; animation: fadeInBody 1.5s forwards; /* Giriş animasyonu */
        }
        
        @keyframes fadeInBody { to { opacity: 1; } }

        /* Müzik Butonu - Modernize */
        #music-control {
            position: fixed; top: 25px; right: 25px; z-index: 2000;
            background: linear-gradient(135deg, #e6a8d7 0%, var(--rose-gold) 100%);
            color: white; border: none; padding: 14px 28px; border-radius: 50px;
            font-family: 'Poppins', sans-serif; font-weight: 500; font-size: 0.95em;
            cursor: pointer; box-shadow: 0 6px 20px rgba(183, 110, 121, 0.3);
            transition: all 0.4s ease; backdrop-filter: blur(5px);
        }
        #music-control:hover { transform: scale(1.08) translateY(-2px); box-shadow: 0 8px 25px rgba(183, 110, 121, 0.4); }

        header { 
            background: linear-gradient(135deg, #fce4ec 0%, #fff1f3 100%);
            padding: 110px 20px; border-bottom: 1px solid rgba(183, 110, 121, 0.2);
            position: relative;
        }
        header::after {
            content: ''; position: absolute; bottom: -1px; left: 50%; transform: translateX(-50%);
            width: 100px; height: 3px; background-color: var(--rose-gold); border-radius: 2px;
        }

        h1 { 
            font-size: 4em; margin: 0 0 15px 0; font-family: 'Dancing Script', cursive; 
            color: var(--rose-gold); text-shadow: 2px 3px 6px rgba(0,0,0,0.08);
            animation: slideInDown 1s ease;
        }
        p.subtitle { 
            font-family: 'Playfair Display', serif; font-size: 1.4em; font-style: italic; 
            color: var(--text-light); margin: 0; animation: fadeIn 1.5s ease 0.5s forwards; opacity: 0;
        }

        @keyframes fadeIn { to { opacity: 1; } }
        @keyframes slideInDown { from { transform: translateY(-30px); opacity: 0; } to { transform: translateY(0); opacity: 1; } }
        @keyframes slideInUp { from { transform: translateY(30px); opacity: 0; } to { transform: translateY(0); opacity: 1; } }
        
        .container { 
            max-width: 900px; margin: 60px auto; padding: 50px; 
            background: var(--cream); border-radius: 25px; 
            box-shadow: 0 20px 50px rgba(0,0,0,0.04); border: 1px solid rgba(183, 110, 121, 0.08);
            position: relative; animation: slideInUp 1s ease;
        }
        h2 { 
            color: var(--rose-gold); padding-bottom: 15px; display: inline-block; 
            margin: 0 0 50px 0; font-family: 'Dancing Script', cursive; font-size: 3em;
            position: relative;
        }
        h2::after {
            content: ''; position: absolute; bottom: 0; left: 50%; transform: translateX(-50%);
            width: 60%; height: 2px; background: linear-gradient(90deg, transparent, var(--rose-gold), transparent);
        }

        /* Modern Galeri */
        .gallery-wrapper {
            display: flex; gap: 30px; justify-content: center; flex-wrap: wrap; margin-bottom: 20px;
        }
        
        .photo-frame {
            background-color: white; padding: 12px 12px 12px 12px;
            box-shadow: 0 10px 25px rgba(0,0,0,0.06); transition: all 0.4s ease;
            border-radius: 15px; position: relative; border: 1px solid #f0f0f0;
            overflow: hidden; flex: 0 1 calc(33.333% - 20px); min-width: 250px;
        }
        .photo-frame:hover { transform: translateY(-10px) rotate(0deg) scale(1.02); box-shadow: 0 15px 35px rgba(183, 110, 121, 0.15); }
        
        .photo-frame img { width: 100%; height: 250px; object-fit: cover; border-radius: 10px; transition: all 0.4s ease;}
        .photo-frame:hover img { transform: scale(1.05); }

        .photo-caption {
            padding: 15px 5px 5px 5px; text-align: center;
            font-family: 'Dancing Script', cursive; font-size: 1.7em; color: var(--rose-gold-dark);
            font-weight: 600;
        }

        /* Mektup Alanı - Premium */
        .letter {
            background-color: #fffcf7; padding: 50px; font-style: italic;
            text-align: left; line-height: 2.3; font-size: 1.25em;
            border-left: 6px solid var(--rose-gold); position: relative;
            border-radius: 0 15px 15px 0; font-family: 'Playfair Display', serif;
            box-shadow: inset 0 0 30px rgba(0,0,0,0.01);
        }
        .letter::before {
            content: '❝'; font-size: 6em; color: rgba(183, 110, 121, 0.1);
            position: absolute; top: -10px; left: 15px; font-family: serif;
        }

        /* Karne Alanı */
        .report-card {
            border: 2px solid rgba(183, 110, 121, 0.3); padding: 5px; border-radius: 15px; background-color: white;
            box-shadow: 0 10px 30px rgba(0,0,0,0.03);
        }
        .report-card-inner { border: 1px solid rgba(183, 110, 121, 0.2); padding: 40px 60px; border-radius: 12px; }
        .report-card-title {
            text-align: center; font-weight: 600; color: var(--rose-gold);
            font-size: 1.7em; margin-bottom: 30px; text-transform: uppercase; letter-spacing: 2px;
            font-family: 'Poppins', sans-serif;
        }
        .report-card-row {
            display: flex; justify-content: space-between; align-items: center;
            border-bottom: 1px solid rgba(183, 110, 121, 0.15); padding: 18px 0; font-size: 1.2em;
        }
        .report-card-row span:first-child { font-weight: 400; color: var(--text-dark); }
        .grade { color: #2ecc71; font-weight: 700; font-family: 'Dancing Script', cursive; font-size: 1.6em;}

        /* Kuponlar - Modern Grid */
        .coupons { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 30px; margin-top: 40px; }
        .coupon { 
            background: white; border: 2px dashed rgba(183, 110, 121, 0.4); padding: 30px; 
            border-radius: 15px; cursor: pointer; transition: all 0.4s ease; color: var(--rose-gold-dark);
            display: flex; align-items: center; justify-content: center; text-align: center; min-height: 120px;
            box-shadow: 0 6px 15px rgba(0,0,0,0.02); font-size: 1.15em; font-weight: 500;
        }
        .coupon:hover { 
            background-color: var(--rose-gold); color: white; transform: translateY(-7px); 
            box-shadow: 0 12px 30px rgba(183, 110, 121, 0.2); border-style: solid;
        }
        .coupon:active { transform: translateY(-3px) scale(0.98); }
        
        .used { 
            background-color: #bdc3c7 !important; color: white !important; cursor: not-allowed; 
            text-decoration: line-through; opacity: 0.7; box-shadow: none !important; border-style: solid !important;
        }
        
        footer { 
            padding: 80px 20px; color: var(--rose-gold); 
            font-family: 'Dancing Script', cursive; font-size: 2.8em; font-weight: 700;
            position: relative;
        }
        footer::before {
            content: ''; position: absolute; top: 0; left: 50%; transform: translateX(-50%);
            width: 150px; height: 1px; background-color: rgba(183, 110, 121, 0.3);
        }
        
        /* Uçuşan Objeler - Daha Soft */
        .falling-item { position: fixed; top: -10vh; z-index: 1; animation: fall linear forwards; opacity: 0.5; pointer-events: none; }
        @keyframes fall { to { transform: translateY(110vh) rotate(360deg); } }
        
        /* Mobil Uyumluluk */
        @media (max-width: 768px) {
            h1 { font-size: 2.8em; }
            p.subtitle { font-size: 1.1em; }
            .container { padding: 30px; margin: 30px auto; }
            h2 { font-size: 2.2em; }
            .letter { padding: 30px; font-size: 1.1em; }
            .report-card-inner { padding: 20px 30px; }
            .report-card-row { font-size: 1em; }
            .grade { font-size: 1.3em; }
            #music-control { padding: 10px 20px; font-size: 0.85em; top: 15px; right: 15px; }
            .photo-frame { flex: 0 1 100%; }
        }
    </style>
</head>
<body>

    <audio id="bgMusic" loop>
        <source src="https://www.mfiles.co.uk/mp3-downloads/erik-satie-gymnopedie-no-1.mp3" type="audio/mpeg">
    </audio>

    <button id="music-control" onclick="toggleMusic()">🎵 Müziği Başlat</button>

    <header>
        <h1>Canım Annem</h1>
        <p class="subtitle">Hayatımın ilk öğretmeni, en değerli rehberim...</p>
    </header>
    
    <div class="container">
        <h2>Güzel Anılarımız</h2>
        <div class="gallery-wrapper">
            <div class="photo-frame">
                <img src="https://images.unsplash.com/photo-1596464716127-f2a82984de30?q=80&w=600&auto=format&fit=crop" alt="Anne ve Çocuk">
                <div class="photo-caption">En Güvenli Liman</div>
            </div>
            <div class="photo-frame">
                <img src="https://images.unsplash.com/photo-1532012197267-da84d127e765?q=80&w=600&auto=format&fit=crop" alt="Kitaplar ve Çiçek">
                <div class="photo-caption">Bilgi Kaynağım</div>
            </div>
            <div class="photo-frame">
                <img src="https://images.unsplash.com/photo-1526047932273-341f2a7631f9?q=80&w=600&auto=format&fit=crop" alt="Güller">
                <div class="photo-caption">Canım Annem</div>
            </div>
        </div>
        
        <div class="letter" style="margin-top: 60px;">
            Canım Annem,<br><br>
            Sen bana sadece yürümeyi, konuşmayı değil; sevmeyi, güçlü olmayı ve hayata gülümseyerek bakmayı da öğrettin. Nöbetçi olduğun günlerde, sınav okuduğun gecelerde bile bana ayıracak vaktin, verecek şefkatin hep vardı. Öğrencilerine ışık olurken, benim dünyamı da aydınlatmayı hiç unutmadın. İyi ki benim annem, iyi ki benim ilk ve en değerli öğretmenimsin.
        </div>
    </div>

    <div class="container">
        <h2>Annemin Yıl Sonu Karnesi</h2>
        <div class="report-card">
            <div class="report-card-inner">
                <div class="report-card-title">Dünyanın En İyi Annesi Diploması</div>
                <div class="report-card-row"><span>Sınırsız Sevgi:</span> <span class="grade">Peki (100) Yıldızlı</span></div>
                <div class="report-card-row"><span>Sabır ve Anlayış:</span> <span class="grade">Peki (100)</span></div>
                <div class="report-card-row"><span>Muhteşem Yemekler:</span> <span class="grade">Peki (100)</span></div>
                <div class="report-card-row"><span>Hayat Rehberliği (Öğretmenlik):</span> <span class="grade">Peki (100)</span></div>
                <div class="report-card-row"><span>Fedakarlık:</span> <span class="grade">Peki (100)</span></div>
            </div>
        </div>
    </div>

    <div class="container">
        <h2>Öğretmenime Özel Hediye Çekleri</h2>
        <p style="margin-bottom: 40px; font-style: italic; color: var(--text-light);">Kullanmak istediğin çekin üzerine tıkla. (Nöbetçi asistanın hemen yerine getirecek 😉)</p>
        <div class="coupons">
            <div class="coupon" onclick="useCoupon(this)">Sınav Okurken<br>Sınırsız Çay/Kahve ☕</div>
            <div class="coupon" onclick="useCoupon(this)">Yorgunluk Alıcı<br>Omuz Masajı 💆‍♀️</div>
            <div class="coupon" onclick="useCoupon(this)">Bugün Bütün Ev İşleri<br>Bende (Sen Dinlen) 🧹</div>
            <div class="coupon" onclick="useCoupon(this)">E-Okul Nöbetinde<br>Atıştırmalık Servisi 🍎</div>
        </div>
    </div>

    <footer>
        Seni Çok Seviyorum... 🌸
    </footer>

    <script>
        let isPlaying = false;
        const bgMusic = document.getElementById('bgMusic');
        const musicBtn = document.getElementById('music-control');
        
        bgMusic.volume = 0.4; // Tatlı bir fon sesi

        function toggleMusic() {
            if (isPlaying) {
                bgMusic.pause();
                musicBtn.innerHTML = '🎵 Müziği Başlat';
                musicBtn.style.background = 'linear-gradient(135deg, #e6a8d7 0%, var(--rose-gold) 100%)';
            } else {
                bgMusic.play().catch(error => {
                    alert("Müziği dinlemek için tarayıcınızın ses izinlerini kontrol edin veya tekrar tıklayın.");
                });
                musicBtn.innerHTML = '⏸️ Müziği Durdur';
                musicBtn.style.background = '#e74c3c'; // Durdurma rengi
            }
            isPlaying = !isPlaying;
        }

        // Hediye Çeki İşlemi - Geliştirildi
        function useCoupon(element) {
            if (!element.classList.contains('used')) {
                element.innerHTML = '✅ İsteğin Alındı!';
                element.classList.add('used');
                // Tatlı bir titreşim efekti
                element.style.animation = 'shake 0.5s';
                setTimeout(() => { element.style.animation = ''; }, 500);
            }
        }

        // shake animasyonu için style ekle
        const style = document.createElement('style');
        style.innerHTML = `
            @keyframes shake {
                0% { transform: translateX(0); }
                25% { transform: translateX(-5px); }
                50% { transform: translateX(5px); }
                75% { transform: translateX(-5px); }
                100% { transform: translateX(0); }
            }
        `;
        document.head.appendChild(style);

        // Uçuşan Objeler Efekti (Zarif)
        function createFallingItem() {
            const item = document.createElement('div');
            item.classList.add('falling-item');
            const emojis = ['🌸', '✨', '🤍', '🍎']; // Daha asil emojiler
            item.innerText = emojis[Math.floor(Math.random() * emojis.length)];
            
            item.style.left = Math.random() * 100 + 'vw';
            item.style.animationDuration = Math.random() * 5 + 6 + 's'; // Daha yavaş ve zarif
            item.style.fontSize = (Math.random() * 1 + 0.8) + 'rem'; // Daha küçük boyutlar
            
            document.body.appendChild(item);
            setTimeout(() => { item.remove(); }, 11000);
        }
        setInterval(createFallingItem, 1000); // Daha az sıklıkta
    </script>

</body>
</html>
