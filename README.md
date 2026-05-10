# Premium Anneler Günü Web Sitesi (Tam Yenilenmiş Versiyon)

```html
<!DOCTYPE html>
<html lang="tr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Canım Annem 🌸</title>

<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600;700&family=Poppins:wght@300;400;500;600&family=Great+Vibes&display=swap" rel="stylesheet">
<script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.9.3/dist/confetti.browser.min.js"></script>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

body{
    font-family:'Poppins',sans-serif;
    overflow-x:hidden;
    color:#4b3d3d;
    background:linear-gradient(-45deg,#fff0f5,#fde2e4,#f8edeb,#fae1dd);
    background-size:400% 400%;
    animation:bg 15s ease infinite;
}

@keyframes bg{
    0%{background-position:0% 50%;}
    50%{background-position:100% 50%;}
    100%{background-position:0% 50%;}
}

#loader{
    position:fixed;
    inset:0;
    background:#fff0f5;
    z-index:9999;
    display:flex;
    flex-direction:column;
    justify-content:center;
    align-items:center;
    animation:fadeOut 1s ease 2.5s forwards;
}

.loader-flower{
    font-size:5rem;
    animation:pulse 1.2s infinite;
}

.loader-text{
    margin-top:20px;
    font-size:2rem;
    font-family:'Great Vibes',cursive;
    color:#b76e79;
    text-align:center;
    padding:0 20px;
}

@keyframes pulse{
    0%,100%{transform:scale(1);}
    50%{transform:scale(1.15);}
}

@keyframes fadeOut{
    to{
        opacity:0;
        visibility:hidden;
    }
}

.container{
    max-width:1100px;
    margin:auto;
    padding:30px 20px 80px;
}

.glass{
    background:rgba(255,255,255,0.45);
    backdrop-filter:blur(18px);
    border:1px solid rgba(255,255,255,0.5);
    border-radius:30px;
    box-shadow:0 10px 40px rgba(183,110,121,0.15);
}

header{
    text-align:center;
    padding:80px 20px 50px;
    animation:slideDown 1s ease 2.5s backwards;
}

@keyframes slideDown{
    from{
        opacity:0;
        transform:translateY(-40px);
    }
    to{
        opacity:1;
        transform:translateY(0);
    }
}

.hero-title{
    font-size:6rem;
    font-family:'Great Vibes',cursive;
    color:#b76e79;
    line-height:1.1;
    text-shadow:0 4px 20px rgba(255,255,255,0.7);
}

.hero-subtitle{
    margin-top:10px;
    font-size:1.4rem;
    color:#6d5d5d;
    font-family:'Playfair Display',serif;
    font-style:italic;
}

.music-box{
    padding:25px;
    margin-bottom:50px;
}

.music-title{
    text-align:center;
    margin-bottom:18px;
    font-size:1.2rem;
    color:#b76e79;
    font-weight:600;
}

.message{
    padding:50px;
    margin-bottom:60px;
    text-align:center;
    line-height:2.1;
    font-size:1.2rem;
    position:relative;
    font-family:'Playfair Display',serif;
}

.message::before,
.message::after{
    position:absolute;
    font-size:5rem;
    color:rgba(183,110,121,0.15);
}

.message::before{
    content:'❝';
    top:-15px;
    left:15px;
}

.message::after{
    content:'❞';
    bottom:-45px;
    right:20px;
}

.section-title{
    text-align:center;
    margin-bottom:35px;
    font-family:'Great Vibes',cursive;
    color:#b76e79;
    font-size:4rem;
}

.report-card{
    padding:40px;
    margin-bottom:60px;
}

.report-row{
    display:flex;
    justify-content:space-between;
    align-items:center;
    padding:18px 0;
    border-bottom:1px dashed rgba(183,110,121,0.3);
}

.report-row:last-child{
    border:none;
}

.grade{
    font-family:'Great Vibes',cursive;
    color:#b76e79;
    font-size:2rem;
}

.coupon-info{
    text-align:center;
    margin-bottom:25px;
    color:#7b6d6d;
    font-style:italic;
}

.coupon-grid{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
    gap:30px;
}

.coupon{
    padding:35px 25px;
    text-align:center;
    transition:0.4s;
    cursor:pointer;
}

.coupon:hover{
    transform:translateY(-12px) scale(1.02);
    background:rgba(255,255,255,0.65);
}

.coupon-icon{
    font-size:3rem;
    margin-bottom:15px;
}

.coupon h3{
    color:#b76e79;
    margin-bottom:15px;
    font-family:'Playfair Display',serif;
}

.coupon p{
    line-height:1.8;
    color:#5c4f4f;
}

.used{
    opacity:0.6;
    transform:none!important;
}

.memory-section{
    margin-top:70px;
    padding:45px;
}

.memory-text{
    text-align:center;
    line-height:2;
    font-size:1.1rem;
}

.big-button{
    display:block;
    margin:70px auto 30px;
    border:none;
    padding:22px 55px;
    border-radius:60px;
    background:linear-gradient(135deg,#b76e79,#e8a0bf);
    color:white;
    font-size:2.2rem;
    font-family:'Great Vibes',cursive;
    cursor:pointer;
    transition:0.4s;
    box-shadow:0 10px 30px rgba(183,110,121,0.3);
}

.big-button:hover{
    transform:scale(1.08);
}

footer{
    text-align:center;
    padding:50px 20px 20px;
    color:#b76e79;
    font-family:'Great Vibes',cursive;
    font-size:2.4rem;
}

.petal{
    position:fixed;
    top:-10vh;
    z-index:-1;
    pointer-events:none;
    opacity:0.7;
    animation:fall linear forwards;
}

@keyframes fall{
    to{
        transform:translateY(110vh) rotate(360deg);
    }
}

@media(max-width:768px){
    .hero-title{
        font-size:4rem;
    }

    .section-title{
        font-size:3rem;
    }

    .message{
        padding:30px;
        font-size:1rem;
    }

    .report-row{
        flex-direction:column;
        align-items:flex-start;
        gap:10px;
    }

    .grade{
        align-self:flex-end;
    }
}
</style>
</head>
<body>

<div id="loader">
    <div class="loader-flower">🌸</div>
    <div class="loader-text">Dünyanın en güzel annesi için hazırlanıyor...</div>
</div>

<div class="container">

<header>
    <h1 class="hero-title">Canım Annem</h1>
    <p class="hero-subtitle">Hayatıma sevgiyi, gücü ve umudu öğreten en güzel insan...</p>
</header>

<div class="music-box glass">
    <div class="music-title">🎧 Bu sayfa senin için hazırlandı...</div>

    <iframe style="border-radius:12px" src="https://open.spotify.com/embed/playlist/37i9dQZF1DX0SM0LYsmbMT?utm_source=generator" width="100%" height="152" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
</div>

<div class="message glass">
    Hayatımdaki en zor anlarda bile bana güç veren, yorulduğumda tek bakışıyla içimi huzurla dolduran canım annem... Sen sadece bir anne değil, aynı zamanda benim ilk öğretmenim, en yakın arkadaşım ve en güvenli limanımsın. Başkalarının hayatına ışık olurken bile benim mutluluğumu hiç unutmaman, beni her zaman sevginle koruman hayatımdaki en büyük şanslardan biri. İyi ki varsın. İyi ki benim annemsin. 🌸
</div>

<h2 class="section-title">Anne Karnesi</h2>

<div class="report-card glass">

<div class="report-row">
<span>Koşulsuz Sevgi</span>
<span class="grade">100/100</span>
</div>

<div class="report-row">
<span>Sabır ve Şefkat</span>
<span class="grade">100/100</span>
</div>

<div class="report-row">
<span>Hayat Boyu Destek</span>
<span class="grade">100/100</span>
</div>

<div class="report-row">
<span>Dünyanın En Güzel Annesi Olma</span>
<span class="grade">Sonsuz ⭐</span>
</div>

</div>

<h2 class="section-title">Sana Özel Kuponlar</h2>

<p class="coupon-info">İstediğin kupona dokunman yeterli ✨</p>

<div class="coupon-grid">

<div class="coupon glass" onclick="claim(this)">
<div class="coupon-icon">☕</div>
<h3>Kahve & Sohbet Günü</h3>
<p>Beraber uzun uzun kahve içip sohbet edeceğimiz tamamen sana ayrılmış özel bir gün.</p>
</div>

<div class="coupon glass" onclick="claim(this)">
<div class="coupon-icon">💆🏻‍♀️</div>
<h3>Yorgunluk Silme Paketi</h3>
<p>Çay servisi, omuz masajı ve tüm ev işlerinde tam destek hakkı.</p>
</div>

<div class="coupon glass" onclick="claim(this)">
<div class="coupon-icon">🍰</div>
<h3>Tatlı Kaçamağı</h3>
<p>Birlikte sevdiğimiz bir yere gidip tatlı yiyip güzel anılar biriktirme günü.</p>
</div>

<div class="coupon glass" onclick="claim(this)">
<div class="coupon-icon">💻</div>
<h3>Teknik Destek Premium</h3>
<p>Telefon, bilgisayar, televizyon, internet... O gün tüm teknik işler bende 😎</p>
</div>

</div>

<div class="memory-section glass">
<h2 class="section-title">Bir Şey Daha...</h2>

<p class="memory-text">
Belki bazen yeterince söylemiyorum ama senin emeğinin, sevgisinin ve fedakarlığının değerini biliyorum. Bugün olduğum her şeyde senin payın var. Bana her zaman inandığın için, beni her koşulda sevdiğin için teşekkür ederim. Dünyadaki hiçbir hediye seni anlatmaya yetmez ama umarım bu küçük sürpriz yüzünde güzel bir gülümseme bırakır. 🤍
</p>
</div>

<button class="big-button" onclick="celebrate()">Seni Çok Seviyorum ❤️</button>

<footer>
Anneler Günün Kutlu Olsun 🌸
</footer>

</div>

<script>
function claim(el){
    if(!el.classList.contains('used')){
        el.classList.add('used');

        el.innerHTML=`
        <div class="coupon-icon">✅</div>
        <h3>Kupon Kullanıldı!</h3>
        <p>Asistan hemen göreve başladı 😌</p>
        `;

        confetti({
            particleCount:70,
            spread:70,
            origin:{y:0.7}
        });
    }
}

function celebrate(){

    let duration=3500;
    let end=Date.now()+duration;

    (function frame(){

        confetti({
            particleCount:7,
            angle:60,
            spread:60,
            origin:{x:0}
        });

        confetti({
            particleCount:7,
            angle:120,
            spread:60,
            origin:{x:1}
        });

        if(Date.now()<end){
            requestAnimationFrame(frame);
        }

    })();
}

function createPetal(){

    const petal=document.createElement('div');
    petal.classList.add('petal');

    const emojis=['🌸','🤍','✨'];

    petal.innerText=emojis[Math.floor(Math.random()*emojis.length)];

    petal.style.left=Math.random()*100+'vw';
    petal.style.fontSize=Math.random()*20+16+'px';
    petal.style.animationDuration=Math.random()*5+7+'s';

    document.body.appendChild(petal);

    setTimeout(()=>{
        petal.remove();
    },12000);
}

setInterval(createPetal,1300);
</script>

</body>
</html>
```

Bu versiyon öncekinden çok daha premium his verir:

* Daha duygusal ve zarif metinler
* C-drama kısmı tamamen kaldırıldı
* Daha şık font kombinasyonları
* Daha modern animasyonlar
* Daha profesyonel renk paleti
* Daha duygusal anne odaklı içerik
* Mobil görünüm ciddi şekilde iyileştirildi
* Daha premium cam efekti
* Daha sinematik açılış hissi

Bunu GitHub Pages’e atarsan bayağı profesyonel görünür. Hatta insanlar hazır template sanabilir 😭
