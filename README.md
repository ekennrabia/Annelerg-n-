<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Canım Annem & En Değerli Öğretmenim 🌸</title>
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
        
        * { box-sizing: border-box; }

        /* YENİ: Yükleniyor Ekranı (Splash Screen) */
        #loader {
            position: fixed; top: 0; left: 0; width: 100vw; height: 100vh;
            background-color: var(--soft-pink); display: flex; flex-direction: column;
            justify-content: center; align-items: center; z-index: 9999;
            animation: fadeOut 1s ease 2.5s forwards;
        }
        .loader-heart { font-size: 4em; animation: heartbeat 1s infinite; }
        .loader-text { font-family: 'Dancing Script', cursive; font-size: 2em; color: var(--rose-gold); margin-top: 20px; }
        
        @keyframes heartbeat { 0% { transform: scale(1); } 50% { transform: scale(1.2); } 100% { transform: scale(1); } }
        @keyframes fadeOut { to { opacity: 0; visibility: hidden; } }

        body { 
            font-family: 'Poppins', sans-serif; background-color: var(--soft-pink); 
            background-image: url('https://www.transparenttextures.com/patterns/p6.png');
            color: var(--text-dark); margin: 0; padding: 0; text-align: center; overflow-x: hidden; 
        }
        
        #music-control {
            position: fixed; top: 25px; right: 25px; z-index: 2000;
            background: linear-gradient(135deg, #e6a8d7 0%, var(--rose-gold) 100%);
            color: white; border: none; padding: 14px 28px; border-radius: 50px;
            font-family: 'Poppins', sans-serif; font-weight: 500; font-size: 0.95em;
            cursor: pointer; box-shadow: 0 6px 20px rgba(183, 110, 121, 0.3); transition: all 0.4s ease;
        }
        #music-control:hover { transform: scale(1.08) translateY(-2px); box-shadow: 0 8px 25px rgba(183, 110, 121, 0.4); }

        header { 
            background: linear-gradient(135deg, #fce4ec 0%, #fff1f3 100%);
            padding: 110px 20px; border-bottom: 1px solid rgba(183, 110, 121, 0.2); position: relative;
        }
        h1 { font-size: 4em; margin: 0 0 15px 0; font-family: 'Dancing Script', cursive; color: var(--rose-gold); text-shadow: 2px 3px 6px rgba(0,0,0,0.08); }
        p.subtitle { font-family: 'Playfair Display', serif; font-size: 1.4em; font-style: italic; color: var(--text-light); margin: 0; }
        
        .container { 
            max-width: 900px; margin: 60px auto; padding: 50px; background: var(--cream); 
            border-radius: 25px; box-shadow: 0 20px 50px rgba(0,0,0,0.04); border: 1px solid rgba(183, 110, 121, 0.08);
        }
        h2 { 
            color: var(--rose-gold); padding-bottom: 15px; display: inline-block; 
            margin: 0 0 50px 0; font-family: 'Dancing Script', cursive; font-size: 3em; position: relative;
        }
        h2::after { content: ''; position: absolute; bottom: 0; left: 50%; transform: translateX(-50%); width: 60%; height: 2px; background: linear-gradient(90deg, transparent, var(--rose-gold), transparent); }

        .gallery-wrapper { display: flex; gap: 30px; justify-content: center; flex-wrap: wrap; margin-bottom: 20px; }
        .photo-frame { background-color: white; padding: 12px; box-shadow: 0 10px 25px rgba(0,0,0,0.06); transition: all 0.4s ease; border-radius: 15px; border: 1px solid #f0f0f0; flex: 0 1 calc(33.333% - 20px); min-width: 250px; }
        .photo-frame:hover { transform: translateY(-10px) scale(1.02); box-shadow: 0 15px 35px rgba(183, 110, 121, 0.15); }
        .photo-frame img { width: 100%; height: 250px; object-fit: cover; border-radius: 10px; transition: all 0.4s ease;}
        .photo-caption { padding: 15px 5px 5px 5px; font-family: 'Dancing Script', cursive; font-size: 1.7em; color: var(--rose-gold-dark); font-weight: 600; }

        /* YENİ: Süper Güç Barları */
        .skills-container { text-align: left; padding: 0 20px; }
        .skill { margin-bottom: 25px; }
        .skill-name { font-weight: 600; font-size: 1.1em; color: var(--rose-gold-dark); display: flex; justify-content: space-between; margin-bottom: 8px; }
        .skill-bar { width: 100%; height: 12px; background-color: #f0e6e8; border-radius: 10px; overflow: hidden; }
        .skill-fill { height: 100%; background: linear-gradient(90deg, #e6a8d7, var(--rose-gold)); width: 0; transition: width 2s ease-in-out; border-radius: 10px; }

        .letter { background-color: #fffcf7; padding: 50px; font-style: italic; text-align: left; line-height: 2.3; font-size: 1.25em; border-left: 6px solid var(--rose-gold); position: relative; border-radius: 0 15px 15px 0; font-family: 'Playfair Display', serif; }
        .letter::before { content: '❝'; font-size: 6em; color: rgba(183, 110, 121, 0.1); position: absolute; top: -10px; left: 15px; font-family: serif; }

        .coupons { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 30px; margin-top: 40px; }
        .coupon { background: white; border: 2px dashed rgba(183, 110, 121, 0.4); padding: 30px; border-radius: 15px; cursor: pointer; transition: all 0.4s ease; color: var(--rose-gold-dark); display: flex; align-items: center; justify-content: center; text-align: center; min-height: 120px; box-shadow: 0 6px 15px rgba(0,0,0,0.02); font-size: 1.15em; font-weight: 500; }
        .coupon:hover { background-color: var(--rose-gold); color: white; transform: translateY(-7px); box-shadow: 0 12px 30px rgba(183, 110, 121, 0.2); border-style: solid; }
        .used { background-color: #bdc3c7 !important; color: white !important; cursor: not-allowed; text-decoration: line-through; opacity: 0.7; box-shadow: none !important; border-style: solid !important; }
        
        footer { padding: 80px 20px; color: var(--rose-gold); font-family: 'Dancing Script', cursive; font-size: 2.8em; font-weight: 700; position: relative; }
        
        .falling-item { position: fixed; top: -10vh; z-index: 1; animation: fall linear forwards; opacity: 0.5; pointer-events: none; }
        @keyframes fall { to { transform: translateY(110vh) rotate(360deg); } }
    </style>
</head>
<body>

    <div id="loader">
        <div class="loader-heart">❤️</div>
        <div class="loader-text">Dünyanın en iyi annesi için hazırlanıyor...</div>
    </div>

    <audio id="bgMusic" loop preload="auto">
        <source src="https://upload.wikimedia.org/wikipedia/commons/c/c8/Frederic_Chopin_-_Nocturne_Op._9%2C_No._2.ogg" type="audio/ogg">
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

    <div class="container" onmouseenter="fillBars()">
        <h2>Annemin Süper Güç Kapasitesi</h2>
        <div class="skills-container">
            <div class="skill">
                <div class="skill-name"><span>Sınırsız Sevgi & Şefkat</span><span>100%</span></div>
                <div class="skill-bar"><div class="skill-fill" id="bar1"></div></div>
            </div>
            <div class="skill">
                <div class="skill-name"><span>Öğretmen Sabrı (Benimle Uğraşma Kapasitesi)</span><span>100%</span></div>
                <div class="skill-bar"><div class="skill-fill" id="bar2"></div></div>
            </div>
            <div class="skill">
                <div class="skill-name"><span>Gizli Tariflerle Muhteşem Yemek Yapma</span><span>100%</span></div>
                <div class="skill-bar"><div class="skill-fill" id="bar3"></div></div>
            </div>
            <div class="skill">
                <div class="skill-name"><span>Yorgun Olsa Bile Gülücük Saçma</span><span>100%</span></div>
                <div class="skill-bar"><div class="skill-fill" id="bar4"></div></div>
            </div>
        </div>
    </div>

    <div class="container">
        <h2>Sana Özel Hediye Çekleri</h2>
        <p style="margin-bottom: 40px; font-style: italic; color: var(--text-light);">Kullanmak istediğin çekin üzerine tıkla. (Nöbetçi asistanın hemen yerine getirecek 😉)</p>
        <div class="coupons">
            <div class="coupon" onclick="useCoupon(this)">E-Okul Nöbetinde<br>Sınırsız Çay/Kahve ☕</div>
            <div class="coupon" onclick="useCoupon(this)">Benim o çok sevdiğim bebek yüzlü Cheng Lei veya Xu Kai'nin oynadığı C-Dramaları mısır eşliğinde birlikte izleme ve karakterleri çekiştirme gecesi 📺🍿</div>
            <div class="coupon" onclick="useCoupon(this)">Bugün Bütün Ev İşleri<br>Bende (Sen Dinlen) 🧹</div>
            <div class="coupon" onclick="useCoupon(this)">Yorgunluk Alıcı<br>Uzun Omuz Masajı 💆‍♀️</div>
        </div>
    </div>

    <footer>
        Seni Çok Seviyorum... 🌸
    </footer>

    <script>
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
                bgMusic.play().catch(error => {
                    alert("Tarayıcınız sesi engelledi. Lütfen bilgisayarınızın/telefonunuzun ses açık olduğundan emin olun.");
                });
                musicBtn.innerHTML = '⏸️ Müziği Durdur';
                musicBtn.style.background = '#e74c3c'; 
            }
            isPlaying = !isPlaying;
        }

        // Süper Güç Barlarını Doldurma Animasyonu
        let barsFilled = false;
        function fillBars() {
            if (!barsFilled) {
                document.getElementById('bar1').style.width = '100%';
                setTimeout(() => document.getElementById('bar2').style.width = '100%', 300);
                setTimeout(() => document.getElementById('bar3').style.width = '100%', 600);
                setTimeout(() => document.getElementById('bar4').style.width = '100%', 900);
                barsFilled = true;
            }
        }

        function useCoupon(element) {
            if (!element.classList.contains('used')) {
                element.innerHTML = '✅ İsteğin Alındı!';
                element.classList.add('used');
                element.style.animation = 'shake 0.5s';
                setTimeout(() => { element.style.animation = ''; }, 500);
            }
        }

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
        setInterval(createFallingItem, 1000); 
    </script>
</body>
</html>
