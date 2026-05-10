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

        /* Kaydırmalı Albüm Alanı */
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
            object-fit: cover;
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
        <source src="
