<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Biricik Annem & En Değerli Öğretmenim 🌸</title>
    <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@700&family=Playfair+Display:ital,wght@0,400;0,700;1,400&display=swap" rel="stylesheet">
    <style>
        :root {
            --rose-gold: #b76e79;
            --soft-pink: #fff0f5;
            --cream: #fdfbf7;
            --text-dark: #4a4a4a;
        }
        
        body { 
            font-family: 'Playfair Display', serif; 
            background-color: var(--soft-pink); 
            color: var(--text-dark); 
            margin: 0; 
            padding: 0; 
            text-align: center; 
            overflow-x: hidden; 
        }
        
        /* Müzik Oynatıcı Butonu - Sabit ve Belirgin */
        #music-control {
            position: fixed;
            top: 20px;
            right: 20px;
            z-index: 2000;
            background: linear-gradient(135deg, #e6a8d7, var(--rose-gold));
            color: white;
            border: none;
            padding: 12px 24px;
            border-radius: 50px;
            font-family: 'Playfair Display', serif;
            font-size: 1em;
            cursor: pointer;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
            transition: all 0.3s ease;
        }
        #music-control:hover { transform: scale(1.1); box-shadow: 0 8px 20px rgba(0,0,0,0.3); }

        header { 
            background: linear-gradient(135deg, #fce4ec, var(--soft-pink));
            padding: 90px 20px; 
            border-bottom: 2px solid var(--rose-gold);
        }
        h1 { 
            font-size: 3.5em; 
            margin: 0; 
            font-family: 'Dancing Script', cursive; 
            color: var(--rose-gold);
            letter-spacing: 2px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.1);
        }
        p.subtitle { font-size: 1.3em; font-style: italic; color: #7f8c8d; }
        
        .container { 
            max-width: 850px; 
            margin: 50px auto; 
            padding: 40px; 
            background: var(--cream); 
            border-radius: 20px; 
            box-shadow: 0 15px 30px rgba(0,0,0,0.05); 
            border: 1px solid rgba(183, 110, 121, 0.1);
        }
        h2 { 
            color: var(--rose-gold); 
            border-bottom: 2px solid var(--rose-gold); 
            padding-bottom: 15px; 
            display: inline-block; 
            margin-bottom: 40px;
            font-family: 'Dancing Script', cursive;
            font-size: 2.8em;
        }

        /* YENİ: Kaydırmalı Albüm Alanı - Öğretmen Temalı Görseller */
        .gallery-wrapper {
            display: flex;
            overflow-x: auto;
            gap: 25px;
            padding: 20px 10px;
            scroll-snap-type: x mandatory;
            scrollbar-width: thin;
            scrollbar-color: var(--rose-gold) var(--cream);
        }
        .gallery-wrapper::-webkit-scrollbar { height: 8px; }
        .gallery-wrapper::-webkit-scrollbar-thumb { background: var(--rose-gold); border-radius: 10px; }
        
        .photo-frame {
            flex: 0 0 auto;
            scroll-snap-align: center;
            background-color: white;
            padding: 15px 15px 50px 15px;
            box-shadow: 0 8px 16px rgba(0,0,0,0.08);
            transition: transform 0.3s ease;
            position: relative;
            border: 1px solid #eee;
        }
        .photo-frame:nth-child(odd) { transform: rotate(-2deg); }
        .photo-frame:nth-child(even) { transform: rotate(2deg); }
        .photo-frame:hover { transform: rotate(0deg) scale(1.03); z-index: 5; }
        .photo-frame img {
            width: 300px;
            height: 300px;
            object-fit: cover; /* Resmi kutuya sığdırır */
            border: 1px solid #f1f1f1;
        }
        .photo-caption {
            position: absolute;
            bottom: 10px;
            width: calc(100% - 30px);
            text-align: center;
            font-family: 'Dancing Script', cursive;
            font-size: 1.6em;
            color: var(--text-dark);
        }

        /* Mektup Alanı */
        .letter {
            background-color: #fffaf0;
            padding: 40px;
            font-style: italic;
            text-align: left;
            line-height: 2.2;
            font-size: 1.2em;
            border-left: 5px solid var(--rose-gold);
            box-shadow: inset 0 0 20px rgba(0,0,0,0.02);
            position: relative;
        }
        .letter::before {
            content: '❝'; font-size: 5em; color: rgba(183, 110, 121, 0.1);
            position: absolute; top: -15px; left: 15px; font-family: serif;
        }

        /* Karne Alanı */
        .report-card {
            border: 3px double var(--rose-gold);
            padding: 5px;
            border-radius: 10px;
            background-color: white;
        }
        .report-card-inner {
            border: 1px solid var(--rose-gold);
            padding: 30px 50px;
        }
        .report-card-title {
            text-align: center; font-weight: bold; color: var(--rose-gold);
            font-size: 1.6em; margin-bottom: 25px; text-transform: uppercase;
        }
        .report-card-row {
            display: flex; justify-content: space-between;
            border-bottom: 1px solid rgba(183, 110, 121, 0.2);
            padding: 15px 0; font-size: 1.2em;
        }
        .report-card-row:last-child { border-bottom: none; }
        .grade { color: #2ecc71; font-weight: bold; font-family: 'Dancing Script', cursive; font-size: 1.5em;}

        /* Kuponlar */
        .coupons { 
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 25px;
            margin-top: 30px; 
        }
        .coupon { 
            background: white; 
            border: 2px dashed var(--rose-gold); 
            padding: 25px; 
            border-radius: 12px; 
            cursor: pointer; 
            transition: all 0.3s ease; 
            font-weight: bold; 
            color: var(--rose-gold);
            display: flex; align-items: center; justify-content: center;
            text-align: center; min-height: 100px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.03);
            font-size: 1.1em;
        }
        .coupon:hover { 
            background-color: var(--rose-gold); 
            color: white; 
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(183, 110, 121, 0.2);
        }
        .used { 
            background-color: #bdc3c7 !important; border-color: #95a5a6 !important; 
            color: white !important; cursor: not-allowed; 
            text-decoration: line-through; transform: translateY(0) !important;
            box-shadow: none !important; opacity: 0.7;
        }
        
        footer {
            padding: 60px; color: var(--rose-gold); 
            font-family: 'Dancing Script', cursive; font-size: 2.5em;
        }
        
        /* Uçuşan Objeler */
        .falling-item {
            position: fixed; top: -10vh; z-index: 1;
            animation: fall linear forwards; opacity: 0.6;
        }
        @keyframes fall {
            to { transform: translateY(110vh) rotate(360deg); }
        }
    </style>
</head>
<body>

    <audio id="bgMusic" loop>
        <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
        Tarayıcınız ses formatını desteklemiyor.
    </audio>

    <button id="music-control" onclick="toggleMusic()">🎵 Müziği Dinle</button>

    <header>
        <h1>Canım Annem</h1>
        <p class="subtitle">Hayatımın ilk öğretmeni, en değerli rehberim...</p>
    </header>
    
    <div class="container">
        <h2>Güzel Anılarımız</h2>
        <div class="gallery-wrapper">
            <div class="photo-frame">
                <img src="https://images.unsplash.com/photo-1518118042469-d41d15444e21?q=80&w=400&auto=format&fit=crop" alt="Öğretmen Gülleri">
                <div class="photo-caption">En Tatlı Rehber</div>
            </div>
            <div class="photo-frame">
                <img src="https://images.unsplash.com/photo-1512820790803-83ca734da794?q=80&w=400&auto=format&fit=crop" alt="Kitaplar ve Kalp">
                <div class="photo-caption">Bilgi Kaynağım</div>
            </div>
            <div class="photo-frame">
                <img src="https://images.unsplash.com/photo-1610472481747-d5d140e340b1?q=80&w=400&auto=format&fit=crop" alt="Anne ve Çocuk Elleri">
                <div class="photo-caption">Canım Annem</div>
            </div>
        </div>
        
        <div class="letter" style="margin-top: 50px;">
            Canım Annem,<br><br>
            Sen bana sadece yürümeyi, konuşmayı değil; sevmeyi, güçlü olmayı ve hayata gülümseyerek bakmayı da öğrettin. Nöbetçi olduğun günlerde, sınav okuduğun gecelerde bile bana ayıracak vaktin, verecek şefkatin hep vardı. Öğrencilerine ışık olurken, benim dünyamı da aydınlatmayı hiç unutmadın. İyi ki benim annem, iyi ki benim ilk ve en değerli öğretmenimsin.
        </div>
    </div>

    <div class="container">
        <h2>Annemin Yıl Sonu Karnesi</h2>
        <div class="report-card">
            <div class="report-card-inner">
                <div class="report-card-title">Dünyanın En İyi Annesi Diploması</div>
                <div class="report-card-row"><span>Sınırsız Sevgi:</span> <span class="grade">Peki (100)</span></div>
                <div class="report-card-row"><span>Sabır ve Anlayış:</span> <span class="grade">Peki (100)</span></div>
                <div class="report-card-row"><span>Muhteşem Yemekler:</span> <span class="grade">Peki (100)</span></div>
                <div class="report-card-row"><span>Hayat Rehberliği (Öğretmenlik):</span> <span class="grade">Peki (100)</span></div>
                <div class="report-card-row"><span>Fedakarlık:</span> <span class="grade">Yıldızlı Peki</span></div>
            </div>
        </div>
    </div>

    <div class="container">
        <h2>Öğretmenime Özel Hediye Çekleri</h2>
        <p style="margin-bottom: 40px; font-style: italic;">Kullanmak istediğin çekin üzerine tıkla. (Asistanın hemen yerine getirecek 😉)</p>
        <div class="coupons">
            <div class="coupon" onclick="useCoupon(this)">Sınav Okurken<br>Sınırsız Çay/Kahve ☕</div>
            <div class="coupon" onclick="useCoupon(this)">Yorgunluk Alıcı<br>Omuz Masajı 💆‍♀️</div>
            <div class="coupon" onclick="useCoupon(this)">Bugün Bütün Ev İşleri<br>Bende (Sen Dinlen) 🧹</div>
            <div class="coupon" onclick="useCoupon(this)">E-Okul Nöbetinde<br>Atıştırmalık Servisi 🍎</div>
        </div>
    </div>

    <footer>
        Öğrencilerin çok şanslı, ama en şanslısı benim! Seni çok seviyorum. 🌸
    </footer>

    <script>
        // Müzik Kontrolü - Güncellendi
        let isPlaying = false;
        const bgMusic = document.getElementById('bgMusic');
        const musicBtn = document.getElementById('music-control');
        
        // Ses seviyesini ayarla (tatlı bir fon müziği için)
        bgMusic.volume = 0.5;

        function toggleMusic() {
            if (isPlaying) {
                bgMusic.pause();
                musicBtn.innerHTML = '🎵 Müziği Dinle';
                musicBtn.style.background = 'linear-gradient(135deg, #e6a8d7, var(--rose-gold))';
            } else {
                // Tarayıcıların engellemesini aşmak için hata kontrolü
                bgMusic.play().catch(error => {
                    console.log("Müzik çalınamadı, tarayıcı engelledi: ", error);
                    alert("Lütfen müziği dinlemek için tekrar tıklayın veya tarayıcınızın ses izinlerini kontrol edin.");
                });
                musicBtn.innerHTML = '⏸️ Müziği Durdur';
                musicBtn.style.background = '#e74c3c'; // Durdurma rengi
            }
            isPlaying = !isPlaying;
        }

        // Hediye Çeki İşlemi
        function useCoupon(element) {
            if (!element.classList.contains('used')) {
                element.innerHTML = '✅ Talep Alındı!';
                element.classList.add('used');
                setTimeout(() => {
                    alert('Hediye çekin başarıyla işleme alındı! Nöbetçi asistanın hemen yerine getiriyor.');
                }, 200);
            }
        }

        // Uçuşan Objeler Efekti (Soft)
        function createFallingItem() {
            const item = document.createElement('div');
            item.classList.add('falling-item');
            const emojis = ['🌸', '✨', '📚', '🍎'];
            item.innerText = emojis[Math.floor(Math.random() * emojis.length)];
            
            item.style.left = Math.random() * 100 + 'vw';
            item.style.animationDuration = Math.random() * 5 + 5 + 's'; // Daha yavaş düşüş
            item.style.fontSize = (Math.random() * 1 + 1) + 'rem';
            
            document.body.appendChild(item);
            setTimeout(() => { item.remove(); }, 10000);
        }
        setInterval(createFallingItem, 800);
    </script>

</body>
</html>
