<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Canım Annem & Biricik Öğretmenim 🌸</title>
    <style>
        body { 
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; 
            background-color: #fff0f5; 
            color: #4a4a4a; 
            margin: 0; 
            padding: 0; 
            text-align: center; 
            overflow-x: hidden; 
        }
        header { 
            background-color: #ffb6c1; 
            padding: 60px 20px; 
            color: white; 
            box-shadow: 0 4px 6px rgba(0,0,0,0.05);
            position: relative;
            z-index: 10;
        }
        h1 { 
            font-size: 2.5em; 
            margin: 0; 
            font-family: 'Georgia', serif; 
            font-style: italic; 
            letter-spacing: 1px;
        }
        p { font-size: 1.2em; }
        .container { 
            max-width: 800px; 
            margin: 30px auto; 
            padding: 30px; 
            background: white; 
            border-radius: 15px; 
            box-shadow: 0 10px 20px rgba(0,0,0,0.05); 
            position: relative;
            z-index: 10;
        }
        h2 { 
            color: #db7093; 
            border-bottom: 2px dashed #ffb6c1; 
            padding-bottom: 10px; 
            display: inline-block; 
            margin-bottom: 20px;
        }
        
        /* Fotoğraf Alanı */
        .photo-frame {
            background-color: white;
            padding: 10px 10px 30px 10px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            transform: rotate(-2deg);
            display: inline-block;
            margin-bottom: 20px;
            transition: transform 0.3s ease;
        }
        .photo-frame:hover {
            transform: rotate(0deg) scale(1.05);
        }
        .photo-frame img {
            max-width: 250px;
            height: auto;
            border: 1px solid #eee;
        }

        /* Mektup Alanı */
        .letter {
            background-color: #fff9e6;
            border-left: 5px solid #ffb6c1;
            padding: 20px 30px;
            font-family: 'Georgia', serif;
            font-style: italic;
            text-align: left;
            line-height: 1.8;
            color: #555;
            margin-top: 10px;
            box-shadow: inset 0 0 10px rgba(0,0,0,0.02);
            font-size: 1.1em;
        }

        /* Karne Alanı */
        .report-card {
            background-color: #fdf5e6;
            border: 3px double #db7093;
            border-radius: 10px;
            padding: 20px 40px;
            margin-top: 20px;
            text-align: left;
        }
        .report-card-title {
            text-align: center;
            font-weight: bold;
            color: #c71585;
            font-size: 1.3em;
            margin-bottom: 15px;
        }
        .report-card-row {
            display: flex;
            justify-content: space-between;
            border-bottom: 1px dotted #ccc;
            padding: 10px 0;
            font-size: 1.1em;
        }
        .report-card-row:last-child { border-bottom: none; }
        .grade { color: #27ae60; font-weight: bold; }

        .reasons { 
            text-align: left; 
            line-height: 2; 
            font-size: 1.1em; 
            padding: 0 40px; 
            list-style-type: '🍎 ';
        }
        .coupons { 
            display: flex; 
            flex-wrap: wrap; 
            gap: 15px; 
            justify-content: center; 
            margin-top: 20px; 
        }
        .coupon { 
            background-color: #ffe4e1; 
            border: 2px dashed #db7093; 
            padding: 20px; 
            border-radius: 10px; 
            cursor: pointer; 
            transition: all 0.3s ease; 
            width: 220px; 
            font-weight: bold; 
            color: #db7093;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            min-height: 60px;
        }
        .coupon:hover { 
            background-color: #ffb6c1; 
            color: white; 
            transform: scale(1.05);
        }
        .used { 
            background-color: #f5f5f5 !important; 
            border-color: #d3d3d3 !important; 
            color: #a9a9a9 !important; 
            cursor: not-allowed; 
            text-decoration: line-through; 
            transform: scale(1) !important;
        }
        footer {
            margin-top: 50px;
            padding: 20px;
            color: #a9a9a9;
            font-size: 0.9em;
            position: relative;
            z-index: 10;
        }
        
        /* Uçuşan Objeler Efekti */
        .falling-item {
            position: fixed;
            top: -10vh;
            font-size: 1.5rem;
            z-index: 1;
            animation: fall linear forwards;
        }
        @keyframes fall {
            to {
                transform: translateY(110vh) rotate(360deg);
            }
        }
    </style>
</head>
<body>

    <header>
        <h1>Anneler Günün Kutlu Olsun! 👩‍🏫❤️</h1>
        <p>Sadece okuldaki öğrencilerin değil, benim de hayatımın en iyi öğretmenine...</p>
    </header>
    
    <div class="container">
        <div class="photo-frame">
            <img src="https://images.unsplash.com/photo-1490750967868-88aa4486c946?q=80&w=400&auto=format&fit=crop" alt="Annemle Ben">
        </div>
        
        <div class="letter">
            Canım Annem,<br><br>
            Sen bana sadece yürümeyi, konuşmayı değil; sevmeyi, güçlü olmayı ve hayata gülümseyerek bakmayı da öğrettin. Yüzlerce çocuğun hayatına ışık olurken, eve geldiğinde benim dünyamı da aydınlatmayı hiç unutmadın. İyi ki benim annem, iyi ki benim ilk ve en değerli öğretmenimsin.
        </div>
    </div>

    <div class="container">
        <h2>Annemin Yıl Sonu Karnesi 📝</h2>
        <div class="report-card">
            <div class="report-card-title">Dünyanın En İyi Annesi Diploması</div>
            <div class="report-card-row"><span>Sınırsız Sevgi:</span> <span class="grade">100 (Peki)</span></div>
            <div class="report-card-row"><span>Sabır ve Anlayış:</span> <span class="grade">100 (Peki)</span></div>
            <div class="report-card-row"><span>Muhteşem Yemekler:</span> <span class="grade">100 (Peki)</span></div>
            <div class="report-card-row"><span>Hayat Rehberliği (Öğretmenlik):</span> <span class="grade">100 (Peki)</span></div>
            <div class="report-card-row"><span>Fedakarlık:</span> <span class="grade">100 (Peki) Yıldızlı</span></div>
        </div>
    </div>

    <div class="container">
        <h2>Seni Neden Bu Kadar Çok Seviyorum?</h2>
        <ul class="reasons">
            <li>Benim her hatamda bir öğretmen sabrıyla doğruları gösterdiğin için.</li>
            <li>Okuldaki onca yorgunluğuna rağmen bana her zaman vakit ayırdığın için.</li>
            <li>Dünyanın en güzel ve şefkatli gülümsemesine sahip olduğun için.</li>
        </ul>
    </div>

    <div class="container">
        <h2>Öğretmenime Özel Hediye Çekleri 🎟️</h2>
        <p>Kullanmak istediğin çekin üzerine tıkla! (Not: Süresiz geçerlidir 😉)</p>
        <div class="coupons">
            <div class="coupon" onclick="useCoupon(this)">☕ Sınav Okurken Sınırsız Kahve/Çay Servisi</div>
            <div class="coupon" onclick="useCoupon(this)">💆‍♀️ Yorgunluk Alıcı Omuz Masajı</div>
            <div class="coupon" onclick="useCoupon(this)">🧹 Bugün Bütün Ev İşleri Bende (Sen Dinlen)</div>
            <div class="coupon" onclick="useCoupon(this)">📺 İstediğin Diziyi/Filmi İtirazsız İzleme Hakkı</div>
        </div>
    </div>

    <footer>
        Öğrencilerin çok şanslı, ama en şanslıları benim! Seni çok seviyorum. 🌸
    </footer>

    <script>
        // Hediye çeki kullanma fonksiyonu
        function useCoupon(element) {
            if (!element.classList.contains('used')) {
                element.innerHTML = '✅ İsteğin Alındı!';
                element.classList.add('used');
                setTimeout(() => {
                    alert('Hediye çekin başarıyla işleme alındı! Nöbetçi asistanın hemen yerine getiriyor. 🏃‍♂️💨');
                }, 100);
            }
        }

        // Uçuşan kalpler, elmalar ve kitaplar fonksiyonu
        function createFallingItem() {
            const item = document.createElement('div');
            item.classList.add('falling-item');
            
            // Öğretmen ve anne temalı emojiler
            const emojis = ['❤️', '🌸', '💖', '🍎', '📚', '✨'];
            item.innerText = emojis[Math.floor(Math.random() * emojis.length)];
            
            item.style.left = Math.random() * 100 + 'vw';
            item.style.animationDuration = Math.random() * 3 + 3 + 's'; // 3 ile 6 saniye arası
            item.style.fontSize = (Math.random() * 1 + 1) + 'rem'; // Farklı boyutlar
            
            document.body.appendChild(item);
            
            // Ekrandan çıkanları sil
            setTimeout(() => {
                item.remove();
            }, 6000);
        }

        // Her 400 milisaniyede bir yeni obje oluştur
        setInterval(createFallingItem, 400);
    </script>

</body>
</html>
