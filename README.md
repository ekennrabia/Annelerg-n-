<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Canım Annem & Biricik Öğretmenim 🌸</title>
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
            background-image: radial-gradient(var(--rose-gold) 0.5px, transparent 0.5px), radial-gradient(var(--rose-gold) 0.5px, var(--soft-pink) 0.5px);
            background-size: 20px 20px;
            background-position: 0 0, 10px 10px;
            color: var(--text-dark); 
            margin: 0; 
            padding: 0; 
            text-align: center; 
            overflow-x: hidden; 
        }
        header { 
            background: linear-gradient(135deg, #e6a8d7, var(--rose-gold));
            padding: 70px 20px; 
            color: white; 
            box-shadow: 0 4px 15px rgba(183, 110, 121, 0.3);
            position: relative;
            z-index: 10;
        }
        h1 { 
            font-size: 3.5em; 
            margin: 0; 
            font-family: 'Dancing Script', cursive; 
            letter-spacing: 2px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.1);
        }
        p.subtitle { font-size: 1.3em; font-style: italic; opacity: 0.9; }
        
        .container { 
            max-width: 800px; 
            margin: 40px auto; 
            padding: 40px; 
            background: var(--cream); 
            border-radius: 20px; 
            box-shadow: 0 15px 30px rgba(0,0,0,0.08); 
            position: relative;
            z-index: 10;
            border: 1px solid rgba(183, 110, 121, 0.2);
        }
        h2 { 
            color: var(--rose-gold); 
            border-bottom: 2px solid var(--rose-gold); 
            padding-bottom: 10px; 
            display: inline-block; 
            margin-bottom: 30px;
            font-family: 'Dancing Script', cursive;
            font-size: 2.5em;
        }

        /* Müzik Oynatıcı Butonu */
        .music-btn {
            background-color: var(--rose-gold);
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 30px;
            font-family: 'Playfair Display', serif;
            font-size: 1em;
            cursor: pointer;
            margin-top: 20px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
            transition: transform 0.3s ease;
        }
        .music-btn:hover { transform: scale(1.05); }

        /* Kaydırmalı Albüm Alanı */
        .gallery-wrapper {
            display: flex;
            overflow-x: auto;
            gap: 20px;
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
            padding: 15px 15px 40px 15px;
            box-shadow: 0 8px 16px rgba(0,0,0,0.1);
            transition: transform 0.3s ease;
            position: relative;
        }
        .photo-frame:nth-child(odd) { transform: rotate(-2deg); }
        .photo-frame:nth-child(even) { transform: rotate(2deg); }
        .photo-frame:hover { transform: rotate(0deg) scale(1.02); z-index: 5; }
        .photo-frame img {
            width: 280px;
            height: 280px;
            object-fit: cover;
            border: 1px solid #eee;
        }
        .photo-caption {
            position: absolute;
            bottom: 10px;
            width: calc(100% - 30px);
            text-align: center;
            font-family: 'Dancing Script', cursive;
            font-size: 1.5em;
            color: var(--text-dark);
        }

        /* Mektup Alanı */
        .letter {
            background: url('https://www.transparenttextures.com/patterns/cream-paper.png');
            background-color: #fffaf0;
            padding: 30px;
            font-style: italic;
            text-align: left;
            line-height: 2;
            font-size: 1.15em;
            border: 1px solid #e8d8c8;
            box-shadow: inset 0 0 20px rgba(0,0,0,0.03);
            position: relative;
        }
        .letter::before {
            content: '❝';
            font-size: 4em;
            color: rgba(183, 110, 121, 0.2);
            position: absolute;
            top: -10px;
            left: 10px;
            font-family: serif;
        }

        /* Karne Alanı */
        .report-card {
            border: 2px solid var(--rose-gold);
            padding: 2px;
            border-radius: 5px;
        }
        .report-card-inner {
            border: 1px solid var(--rose-gold);
            padding: 20px 40px;
            background-color: transparent;
        }
        .report-card-title {
            text-align: center;
            font-weight: bold;
            color: var(--rose-gold);
            font-size: 1.4em;
            margin-bottom: 20px;
            letter-spacing: 1px;
            text-transform: uppercase;
        }
        .report-card-row {
            display: flex;
            justify-content: space-between;
            border-bottom: 1px solid rgba(183, 110, 121, 0.3);
            padding: 12px 0;
            font-size: 1.1em;
        }
        .report-card-row:last-child { border-bottom: none; }
        .grade { color: var(--rose-gold); font-weight: bold; font-family: 'Dancing Script', cursive; font-size: 1.4em;}

        /* Kuponlar */
        .coupons { 
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 20px;
            margin-top: 20px; 
        }
        .coupon { 
            background: white; 
            border: 2px dashed var(--rose-gold); 
            padding: 20px; 
            border-radius: 8px; 
            cursor: pointer; 
            transition: all 0.3s ease; 
            font-weight: bold; 
            color: var(--rose-gold);
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            min-height: 80px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.05);
        }
        .coupon:hover { 
            background-color: var(--rose-gold); 
            color: white; 
            transform: translateY(-5px);
            box-shadow: 0 8px 15px rgba(183, 110, 121, 0.3);
        }
        .used { 
            background-color: #f5f5f5 !important; 
            border-color: #d3d3d3 !important; 
            color: #a9a9a9 !important; 
            cursor: not-allowed; 
            text-decoration: line-through; 
            transform: translateY(0) !important;
            box-shadow: none !important;
        }
        
        /* Uçuşan Objeler */
        .falling-item {
            position: fixed;
            top: -10vh;
            z-index: 1;
            animation: fall linear forwards;
            opacity: 0.7;
        }
        @keyframes fall {
            to { transform: translateY(110vh) rotate(360deg); }
        }
    </style>
</head>
<body>

    <audio id="bgMusic" loop>
        <source src="https://assets.mixkit.co/music/preview/mixkit-beautiful-dream-493.mp3" type="audio/mpeg">
    </audio>

    <header>
        <h1>Anneler Günün Kutlu Olsun</h1>
        <p class="subtitle">Hayatımın en güzel detayı, en değerli öğretmenim...</p>
        <button class="music-btn" onclick="toggleMusic()">🎵 Müziği Başlat</button>
    </header>
    
    <div class="container">
        <h2>Güzel Anılarımız</h2>
        <div class="gallery-wrapper">
            <div class="photo-frame">
                <img src="https://images.unsplash.com/photo-1490750967868-88aa4486c946?q=80&w=400&auto=format&fit=crop" alt="Anı 1">
                <div class="photo-caption">En iyi arkadaşım</div>
            </div>
            <div class="photo-frame">
                <img src="https://images.unsplash.com/photo-1511895426328-dc8714191300?q=80&w=400&auto=format&fit=crop" alt="Anı 2">
                <div class="photo-caption">Rehberim</div>
            </div>
            <div class="photo-frame">
                <img src="https://images.unsplash.com/photo-1516684669134-de6f7c473a2a?q=80&w=400&auto=format&fit=crop" alt="Anı 3">
                <div class="photo-caption">Canım Annem</div>
            </div>
        </div>
        
        <div class="letter" style="margin-top: 40px;">
            Canım Annem,<br><br>
            Sen bana sadece yürümeyi, konuşmayı değil; sevmeyi, güçlü olmayı ve hayata gülümseyerek bakmayı da öğrettin. Yüzlerce çocuğun hayatına ışık olurken, eve geldiğinde benim dünyamı da aydınlatmayı hiç unutmadın. Sadece mükemmel bir anne değil, aynı zamanda harika bir insansın. İyi ki benim annem, iyi ki benim ilk ve en değerli öğretmenimsin.
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
        <h2>Sana Özel Hediye Çekleri</h2>
        <p style="margin-bottom: 30px; font-style: italic;">Kullanmak istediğin çekin üzerine tıkla. (Süresiz geçerlidir)</p>
        <div class="coupons">
            <div class="coupon" onclick="useCoupon(this)">Sınav Okurken Sınırsız<br>Kahve/Çay Servisi ☕</div>
            <div class="coupon" onclick="useCoupon(this)">Yorgunluk Alıcı<br>Omuz Masajı 💆‍♀️</div>
            <div class="coupon" onclick="useCoupon(this)">Bugün Bütün Ev İşleri<br>Bende (Sen Dinlen) 🧹</div>
            <div class="coupon" onclick="useCoupon(this)">İstediğin Diziyi/Filmi<br>İtirazsız İzleme Hakkı 📺</div>
        </div>
    </div>

    <footer style="padding: 40px; color: var(--rose-gold); text-align: center; font-family: 'Dancing Script', cursive; font-size: 2em;">
        Seni çok seviyorum... 🌸
    </footer>

    <script>
        // Müzik Kontrolü
        let isPlaying = false;
        const bgMusic = document.getElementById('bgMusic');
        bgMusic.volume = 0.4; // Sesi rahatsız etmeyecek seviyeye çektik

        function toggleMusic() {
            const btn = document.querySelector('.music-btn');
            if (isPlaying) {
                bgMusic.pause();
                btn.innerHTML = '🎵 Müziği Başlat';
            } else {
                bgMusic.play();
                btn.innerHTML = '⏸️ Müziği Durdur';
            }
            isPlaying = !isPlaying;
        }

        // Hediye Çeki İşlemi
        function useCoupon(element) {
            if (!element.classList.contains('used')) {
                element.innerHTML = 'Onaylandı! ❤️';
                element.classList.add('used');
                setTimeout(() => {
                    alert('Hediye çekin başarıyla işleme alındı! Asistanın hemen yerine getiriyor.');
                }, 200);
            }
        }

        // Uçuşan Objeler Efekti
        function createFallingItem() {
            const item = document.createElement('div');
            item.classList.add('falling-item');
            const emojis = ['🌸', '✨', '🤍', '🍎']; // Daha soft emojiler
            item.innerText = emojis[Math.floor(Math.random() * emojis.length)];
            
            item.style.left = Math.random() * 100 + 'vw';
            item.style.animationDuration = Math.random() * 4 + 4 + 's';
            item.style.fontSize = (Math.random() * 1 + 1) + 'rem';
            
            document.body.appendChild(item);
            setTimeout(() => { item.remove(); }, 8000);
        }
        setInterval(createFallingItem, 600);
    </script>

</body>
</html>
