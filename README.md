<!DOCTYPE html>
<html lang="tr">

<head>

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Canım Annem 💖</title>

<link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Poppins:wght@300;400;500;600&family=Playfair+Display:wght@400;600&display=swap" rel="stylesheet">

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

    background:linear-gradient(-45deg,#fff0f5,#ffe0ea,#ffd6e7,#fff5f8);

    background-size:400% 400%;

    animation:bgMove 15s ease infinite;

    color:#5c4d4d;

}

@keyframes bgMove{

    0%{
        background-position:0% 50%;
    }

    50%{
        background-position:100% 50%;
    }

    100%{
        background-position:0% 50%;
    }

}

body::before{

    content:'';

    position:fixed;

    inset:0;

    background:
    radial-gradient(circle at top left, rgba(255,255,255,0.5), transparent 30%),
    radial-gradient(circle at bottom right, rgba(255,192,203,0.25), transparent 30%);

    z-index:-2;

    pointer-events:none;

}

.container{

    max-width:1150px;

    margin:auto;

    padding:40px 20px 100px;

}

.glass{

    background:rgba(255,255,255,0.35);

    backdrop-filter:blur(18px);

    border:1px solid rgba(255,255,255,0.4);

    border-radius:35px;

    box-shadow:
    0 10px 40px rgba(255,105,145,0.12);

}

#loader{

    position:fixed;

    inset:0;

    background:#fff0f5;

    z-index:9999;

    display:flex;

    justify-content:center;

    align-items:center;

    flex-direction:column;

    animation:fadeOut 1s ease 2.5s forwards;

}

.loader-heart{

    font-size:5rem;

    animation:pulse 1.2s infinite;

}

.loader-text{

    margin-top:20px;

    font-family:'Great Vibes',cursive;

    font-size:2.3rem;

    color:#d96c92;

}

@keyframes pulse{

    0%,100%{
        transform:scale(1);
    }

    50%{
        transform:scale(1.15);
    }

}

@keyframes fadeOut{

    to{
        opacity:0;
        visibility:hidden;
    }

}

header{

    text-align:center;

    padding:80px 20px 60px;

}

.hero-title{

    font-size:6rem;

    font-family:'Great Vibes',cursive;

    color:#d96c92;

    text-shadow:0 5px 25px rgba(255,255,255,0.9);

}

.hero-subtitle{

    margin-top:15px;

    font-size:1.3rem;

    color:#786565;

    font-family:'Playfair Display',serif;

    font-style:italic;

}

.music-box{

    padding:25px;

    margin-bottom:55px;

}

.music-title{

    text-align:center;

    margin-bottom:18px;

    color:#d96c92;

    font-weight:600;

}

.message{

    padding:55px;

    text-align:center;

    line-height:2.2;

    font-size:1.15rem;

    margin-bottom:60px;

    font-family:'Playfair Display',serif;

    position:relative;

}

.message::before{

    content:'❝';

    position:absolute;

    top:-10px;

    left:15px;

    font-size:5rem;

    color:#d96c92;

    opacity:0.15;

}

.message::after{

    content:'❞';

    position:absolute;

    bottom:-40px;

    right:20px;

    font-size:5rem;

    color:#d96c92;

    opacity:0.15;

}

.section-title{

    text-align:center;

    margin-bottom:35px;

    font-size:4rem;

    color:#d96c92;

    font-family:'Great Vibes',cursive;

}

.report-card{

    padding:45px;

    margin-bottom:70px;

}

.report-row{

    display:flex;

    justify-content:space-between;

    align-items:center;

    padding:18px 0;

    border-bottom:1px dashed rgba(217,108,146,0.25);

}

.report-row:last-child{

    border:none;

}

.grade{

    font-size:2rem;

    color:#d96c92;

    font-family:'Great Vibes',cursive;

}

.coupon-info{

    text-align:center;

    margin-bottom:25px;

    color:#7d6969;

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

    transform:translateY(-12px) scale(1.03);

    background:rgba(255,255,255,0.5);

}

.coupon-icon{

    font-size:3rem;

    margin-bottom:15px;

}

.coupon h3{

    margin-bottom:15px;

    color:#d96c92;

    font-family:'Playfair Display',serif;

}

.coupon p{

    line-height:1.8;

}

.love-notes{

    margin-top:70px;

    padding:45px;

}

.notes-grid{

    display:grid;

    grid-template-columns:repeat(auto-fit,minmax(220px,1fr));

    gap:25px;

    margin-top:30px;

}

.note-card{

    background:rgba(255,255,255,0.3);

    border:1px solid rgba(255,255,255,0.35);

    border-radius:25px;

    padding:30px 20px;

    text-align:center;

    transition:0.4s;

}

.note-card:hover{

    transform:translateY(-10px) scale(1.03);

    background:rgba(255,255,255,0.5);

}

.note-emoji{

    font-size:2.7rem;

    margin-bottom:15px;

}

.note-card h3{

    margin-bottom:12px;

    color:#d96c92;

    font-family:'Playfair Display',serif;

}

.note-card p{

    line-height:1.8;

}

.memory-section{

    margin-top:70px;

    padding:55px;

    text-align:center;

    line-height:2.2;

    position:relative;

}

.memory-section::before{

    content:'💖';

    position:absolute;

    top:20px;

    right:30px;

    font-size:2rem;

    opacity:0.5;

}

.memory-section::after{

    content:'🌸';

    position:absolute;

    bottom:20px;

    left:30px;

    font-size:2rem;

    opacity:0.5;

}

.big-button{

    display:block;

    margin:80px auto 40px;

    border:none;

    padding:24px 65px;

    border-radius:70px;

    background:linear-gradient(135deg,#ff7aa2,#ffb6cb);

    color:white;

    font-size:2.6rem;

    font-family:'Great Vibes',cursive;

    cursor:pointer;

    transition:0.4s;

    box-shadow:
    0 10px 35px rgba(255,105,145,0.3);

    position:relative;

    overflow:hidden;

}

.big-button:hover{

    transform:scale(1.08);

}

.big-button::before{

    content:'';

    position:absolute;

    width:200%;
    height:200%;

    background:rgba(255,255,255,0.18);

    top:-50%;
    left:-50%;

    transform:rotate(25deg);

    animation:shine 4s linear infinite;

}

@keyframes shine{

    0%{
        transform:translateX(-100%) rotate(25deg);
    }

    100%{
        transform:translateX(100%) rotate(25deg);
    }

}

footer{

    text-align:center;

    padding:40px 20px;

    font-size:2.5rem;

    color:#d96c92;

    font-family:'Great Vibes',cursive;

}

.heart{

    position:fixed;

    pointer-events:none;

    animation:floatUp linear forwards;

    z-index:999;

}

@keyframes floatUp{

    0%{

        transform:translateY(0) scale(0.8);

        opacity:0;

    }

    20%{

        opacity:1;

    }

    100%{

        transform:translateY(-120vh) scale(1.4);

        opacity:0;

    }

}

.sparkle{

    position:fixed;

    pointer-events:none;

    animation:fallDown linear forwards;

    z-index:-1;

}

@keyframes fallDown{

    0%{

        transform:translateY(0) rotate(0deg);

    }

    100%{

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

        padding:35px;

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

<div class="loader-heart">
💖
</div>

<div class="loader-text">
Canım annem için hazırlanıyor...
</div>

</div>

<div class="container">

<header>

<h1 class="hero-title">
Canım Annem 💖
</h1>

<p class="hero-subtitle">
Hayatıma sevgiyi, gücü ve umudu öğreten en güzel insan...
</p>

</header>

<div class="music-box glass">

<div class="music-title">
🎧 Bu sayfa sadece senin için hazırlandı...
</div>

<iframe
style="border-radius:12px"
src="https://open.spotify.com/embed/playlist/37i9dQZF1DX0SM0LYsmbMT?utm_source=generator"
width="100%"
height="152"
frameBorder="0"
allowfullscreen=""
allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture"
loading="lazy">
</iframe>

</div>

<div class="message glass">

Hayatımdaki en zor anlarda bile bana güç veren, yorulduğumda tek bakışıyla içimi huzurla dolduran canım annem...  
Sen sadece bir anne değil, aynı zamanda benim ilk öğretmenim, en yakın arkadaşım ve en güvenli limanımsın.  
Bana sevgiyi, sabrı ve güçlü olmayı öğrettiğin için sana ne kadar teşekkür etsem az kalır.  
İyi ki varsın. İyi ki benim annemsin. 💖

</div>

<h2 class="section-title">
Anne Karnesi
</h2>

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
<span>Dünyanın En Güzel Annesi</span>
<span class="grade">Sonsuz ⭐</span>
</div>

</div>

<h2 class="section-title">
Sana Özel Kuponlar
</h2>

<p class="coupon-info">
İstediğin kupona dokunman yeterli ✨
</p>

<div class="coupon-grid">

<div class="coupon glass" onclick="claim(this)">
<div class="coupon-icon">☕</div>
<h3>Kahve & Sohbet Günü</h3>
<p>
Birlikte uzun uzun kahve içip sohbet edeceğimiz özel bir gün.
</p>
</div>

<div class="coupon glass" onclick="claim(this)">
<div class="coupon-icon">💆🏻‍♀️</div>
<h3>Yorgunluk Silme Paketi</h3>
<p>
Masaj, çay servisi ve tam destek hakkı 😌
</p>
</div>

<div class="coupon glass" onclick="claim(this)">
<div class="coupon-icon">🍰</div>
<h3>Tatlı Kaçamağı</h3>
<p>
Birlikte tatlı yiyip güzel anılar biriktirme günü.
</p>
</div>

<div class="coupon glass" onclick="claim(this)">
<div class="coupon-icon">💻</div>
<h3>Teknik Destek Premium</h3>
<p>
O gün tüm teknik işler tamamen bende 😎
</p>
</div>

</div>

<div class="love-notes glass">

<h2 class="section-title">
Senin İçin Küçük Notlar 💌
</h2>

<div class="notes-grid">

<div class="note-card">
<div class="note-emoji">🌸</div>
<h3>İyi ki Varsın</h3>
<p>
Yanında olmak bile bazen tüm stresimi unutturuyor.
</p>
</div>

<div class="note-card">
<div class="note-emoji">🤍</div>
<h3>En Güvenli Yerim</h3>
<p>
Dünyada ne olursa olsun yanında huzur buluyorum.
</p>
</div>

<div class="note-card">
<div class="note-emoji">✨</div>
<h3>En Güçlü Kadın</h3>
<p>
Hayatıma güçlü olmayı öğreten ilk insan sensin.
</p>
</div>

<div class="note-card">
<div class="note-emoji">💗</div>
<h3>Benim Kahramanım</h3>
<p>
Hayatımdaki en büyük kahramansın.
</p>
</div>

</div>

</div>

<div class="memory-section glass">

<h2 class="section-title">
Bir Şey Daha...
</h2>

<p>

Belki bazen yeterince söylemiyorum ama senin emeğinin, sevgisinin ve fedakarlığının değerini biliyorum.  
Bugün olduğum her şeyde senin payın var.  
Beni her koşulda sevdiğin için teşekkür ederim.  
Umarım bu küçük sürpriz yüzünde güzel bir gülümseme bırakır. 🤍

</p>

</div>

<button class="big-button" onclick="celebrate()">
Seni Çok Seviyorum 💖
</button>

<footer>
Anneler Günün Kutlu Olsun 🌸
</footer>

</div>

<script>

function createHeart(){

    const heart=document.createElement('div');

    heart.classList.add('heart');

    const hearts=['💖','💗','💕','🌸','🤍'];

    heart.innerHTML=hearts[Math.floor(Math.random()*hearts.length)];

    heart.style.left=Math.random()*100+'vw';

    heart.style.bottom='-30px';

    heart.style.fontSize=(Math.random()*30+20)+'px';

    heart.style.animationDuration=(Math.random()*3+4)+'s';

    document.body.appendChild(heart);

    setTimeout(()=>{

        heart.remove();

    },7000);

}

setInterval(createHeart,500);

function createSparkle(){

    const sparkle=document.createElement('div');

    sparkle.classList.add('sparkle');

    const items=['✨','💖','🌸'];

    sparkle.innerHTML=items[Math.floor(Math.random()*items.length)];

    sparkle.style.left=Math.random()*100+'vw';

    sparkle.style.top='-20px';

    sparkle.style.fontSize=(Math.random()*18+14)+'px';

    sparkle.style.animationDuration=(Math.random()*5+6)+'s';

    document.body.appendChild(sparkle);

    setTimeout(()=>{

        sparkle.remove();

    },12000);

}

setInterval(createSparkle,900);

function celebrate(){

    let duration=5000;

    let end=Date.now()+duration;

    const colors=['#ff4d88','#ff99bb','#ffd6e7','#ffffff'];

    (function frame(){

        confetti({

            particleCount:4,

            angle:60,

            spread:70,

            origin:{x:0},

            colors:colors

        });

        confetti({

            particleCount:4,

            angle:120,

            spread:70,

            origin:{x:1},

            colors:colors

        });

        for(let i=0;i<3;i++){

            createHeart();

        }

        if(Date.now()<end){

            requestAnimationFrame(frame);

        }

    })();

}

function claim(el){

    if(!el.classList.contains('used')){

        el.classList.add('used');

        el.innerHTML=`

        <div class="coupon-icon">💖</div>

        <h3>Kupon Kullanıldı!</h3>

        <p>
        Asistan hemen göreve başladı 😌
        </p>

        `;

        for(let i=0;i<12;i++){

            setTimeout(()=>{

                createHeart();

            },i*100);

        }

    }

}

</script>

</body>

</html>
