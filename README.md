<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Canım Annem 🌸</title>
    <style>
        body { 
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; 
            background-color: #fff0f5; 
            color: #4a4a4a; 
            margin: 0; 
            padding: 0; 
            text-align: center; 
        }
        header { 
            background-color: #ffb6c1; 
            padding: 60px 20px; 
            color: white; 
            box-shadow: 0 4px 6px rgba(0,0,0,0.05);
        }
        h1 { 
            font-size: 3em; 
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
        }
        h2 { 
            color: #db7093; 
            border-bottom: 2px dashed #ffb6c1; 
            padding-bottom: 10px; 
            display: inline-block; 
            margin-bottom: 20px;
        }
        .reasons { 
            text-align: left; 
            line-height: 2; 
            font-size: 1.1em; 
            padding: 0 40px; 
            list-style-type: '💖 ';
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
        }
    </style>
</head>
<body>

    <header>
        <h1>Anneler Günün Kutlu Olsun! ❤️</h1>
        <p>Dünyanın en muazzam annesine...</p>
    </header>
    
    <div class="container">
        <h2>Seni Sevmemin Bazı Nedenleri</h2>
        <ul class="reasons">
            <li>Bana her koşulda inandığın ve destek olduğun için.</li>
            <li>Dünyanın en güzel yemeklerini kendi gizli tariflerinle yaptığın için.</li>
            <li>Ne zaman yardıma ihtiyacım olsa hiç düşünmeden yanımda bittiğin için.</li>
            <li>Sadece harika bir anne değil, aynı zamanda en iyi sırdaşım olduğun için.</li>
        </ul>
    </div>

    <div class="container">
        <h2>Anneler Günü Hediye Çekleri 🎟️</h2>
        <p>Kullanmak istediğin çekin üzerine tıkla!</p>
        <div class="coupons">
            <div class="coupon" onclick="useCoupon(this)">☕ Özel Kahve/Çay Servisi</div>
            <div class="coupon" onclick="useCoupon(this)">🧹 Bugün Ev İşleri Bende</div>
            <div class="coupon" onclick="useCoupon(this)">🤗 Kocaman Bir Sarılma</div>
            <div class="coupon" onclick="useCoupon(this)">🎬 Birlikte Dizi/Film Gecesi</div>
        </div>
    </div>

    <footer>
        Seni çok seviyorum! 🌸
    </footer>

    <script>
        function useCoupon(element) {
            if (!element.classList.contains('used')) {
                element.innerHTML = '✅ Kullanıldı!';
                element.classList.add('used');
                // Tıklandığında ekrana tatlı bir uyarı çıkar
                setTimeout(() => {
                    alert('Hediye çekin başarıyla işleme alındı! Hemen yerine getiriyorum. 😉');
                }, 100);
            }
        }
    </script>

</body>
</html>
