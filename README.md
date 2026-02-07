<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>G.M. & SONS - Luxury Stolls</title>
    
    <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@700&family=Playfair+Display:wght@700&display=swap" rel="stylesheet">
    
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; scroll-behavior: smooth; }
        
        body { 
            font-family: 'Playfair Display', serif; 
            background-color: #FFF5F7; 
            color: #1B4332; 
        }

        header {
            padding: 3rem 5%;
            border-bottom: 3px solid #D4AF37; 
            background: #F4C2C2; 
            text-align: center;
            box-shadow: 0 4px 20px rgba(0,0,0,0.08);
        }

        .brand-name { 
            font-size: 4.5rem; 
            font-family: 'Cormorant Garamond', serif; 
            font-weight: 700; 
            letter-spacing: 8px; 
            color: #1B4332; 
            text-transform: uppercase;
            margin-bottom: 15px;
            text-shadow: 1px 1px 2px rgba(255,255,255,0.6);
            transition: color 0.4s ease, transform 0.4s ease;
            cursor: default;
            display: inline-block;
        }

        /* HOVER EFFECT ADDED HERE */
        .brand-name:hover {
            color: #D4AF37;
            transform: scale(1.02);
        }

        .header-info {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            max-width: 1200px;
            margin: 0 auto;
            border-top: 1px solid rgba(27, 67, 50, 0.2);
            padding-top: 20px;
        }

        .tagline { font-size: 0.9rem; color: #5E503F; flex: 1; text-align: left; font-style: italic; letter-spacing: 1px; }
        .contact-top { font-size: 0.9rem; color: #1B4332; flex: 1; text-align: right; font-weight: bold; }

        .grid {
            display: flex;
            flex-wrap: wrap;
            padding: 20px;
            gap: 20px;
            justify-content: center;
        }
        
        .card {
            width: calc(50% - 20px); 
            background: white;
            border: 1px solid #F0EAD6;
            padding: 10px;
            text-align: center;
            overflow: hidden;
            transition: all 0.4s cubic-bezier(0.165, 0.84, 0.44, 1);
            cursor: pointer;
            position: relative;
            box-shadow: 0 2px 5px rgba(0,0,0,0.05);
        }

        .card:hover {
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
            transform: translateY(-5px);
        }

        .watermark {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%) rotate(-45deg);
            font-size: 1.2rem;
            color: rgba(255, 255, 255, 0.4);
            font-weight: bold;
            text-transform: uppercase;
            white-space: nowrap;
            pointer-events: none;
            z-index: 5;
            letter-spacing: 2px;
        }

        .img-wrapper {
            position: relative;
            overflow: hidden;
        }

        .skeleton {
            background: #ececec;
            background: linear-gradient(110deg, #ececec 8%, #f5f5f5 18%, #ececec 33%);
            background-size: 200% 100%;
            animation: shimmer 1.5s linear infinite;
        }

        @keyframes shimmer { to { background-position-x: -200%; } }

        .card img {
            width: 100%;
            height: auto;
            min-height: 200px;
            border: 1px solid #EAE0D5;
            margin-bottom: 10px;
            transition: transform 0.6s ease;
            display: block;
        }

        .card:hover img { transform: scale(1.08); }

        #backToTop {
            position: fixed;
            bottom: 30px;
            right: 30px;
            width: 50px;
            height: 50px;
            background-color: #1B4332;
            color: white;
            border: 2px solid #D4AF37; 
            border-radius: 50%;
            cursor: pointer;
            display: none;
            z-index: 2000;
        }

        #lightbox {
            display: none;
            position: fixed;
            z-index: 3000;
            top: 0; left: 0;
            width: 100%; height: 100%;
            background: rgba(0, 0, 0, 0.95);
            justify-content: center;
            align-items: center;
        }

        #lightbox img { max-width: 90%; max-height: 85%; border: 4px solid #D4AF37; }
        #lightbox.active { display: flex; }

        footer {
            background: #1B1B1B;
            color: #FDFCFB;
            padding: 4rem 2rem;
            text-align: center;
            margin-top: 5rem;
            border-top: 4px solid #D4AF37;
        }

        @media (max-width: 600px) {
            .brand-name { font-size: 2.2rem; letter-spacing: 4px; }
            .header-info { flex-direction: column; gap: 15px; }
            .tagline, .contact-top { text-align: center; }
        }
    </style>
</head>
<body>

    <button id="backToTop">↑</button>

    <header>
        <div class="brand-name">G.M. & SONS</div>
        <div class="header-info">
            <div class="tagline">Handloom, Powerloom Cloths Commission Agent And Order Supplier</div>
            <div class="contact-top">Moin: 8090307576 | Affan: 8887792884</div>
        </div>
    </header>

    <main>
        <div class="grid" id="image-grid"></div>
    </main>

    <div id="lightbox"><img src="" alt="Enlarged View"></div>

    <footer>
        <p style="letter-spacing: 1px;">&copy; G.M. & SONS. All Rights Reserved. SINCE 1976</p>
        <p style="margin-top: 20px; color: #D4AF37; letter-spacing: 3px; font-family: 'Cormorant Garamond', serif; font-weight: bold; font-size: 1.2rem;">-- PLEASE VISIT AGAIN --</p>
    </footer>

    <script>
        const imageList = ["1000295702.jpg", "1000295705.jpg", "1000295711.jpg", "1000295720.jpg", "1000295723.jpg", "1000295726.jpg", "1000295729.jpg", "1000295732.jpg", "1000295735.jpg", "1000295728.jpg", "1000296053.jpg", "1000296057.jpg", "1000296061.jpg", "1000214010.jpg", "1000214016.jpg", "1000270449.jpg", "1000270450.jpg", "1000270452.jpg", "1000270453.jpg", "1000270458.jpg", "1000270459.jpg", "1000271402.jpg", "1000271619.jpg", "1000271621.jpg", "1000271627.jpg", "1000271633.jpg", "1000271974.jpg", "1000271976.jpg", "1000271977.jpg", "1000271984.jpg", "1000271985.jpg", "1000271986.jpg", "1000271990.jpg", "1000273068.jpg", "1000273377.jpg", "1000273588.jpg", "1000273589.jpg", "1000273592.jpg", "1000273594.jpg", "1000273595.jpg", "1000273229.jpg", "1000293229.jpg", "1000293232.jpg", "1000293241.jpg", "1000293244.jpg", "1000293247.jpg", "1000293253.jpg", "1000293256.jpg", "1000293259.jpg", "1000293271.jpg", "1000293274.jpg", "1000295696.jpg", "1000271377.jpg", "1000271379.jpg", "1000271381.jpg", "1000271383.jpg", "1000271385.jpg", "1000271392.jpg", "1000271399.jpg", "1000271409.jpg", "1000271412.jpg", "1000271417.jpg", "1000271596.jpg", "1000271599.jpg", "1000271603.jpg", "1000270397.jpg", "1000270449.jpg", "1000270450.jpg", "1000270453.jpg", "1000270458.jpg", "1000271367.jpg", "1000271369.jpg", "1000271371.jpg", "1000271373.jpg", "1000271375.jpg", "1000271377.jpg", "1000271379.jpg", "1000271381.jpg", "1000218263.jpg", "1000218264.jpg", "1000218265.jpg", "1000218270.jpg", "1000218271.jpg", "1000270359.jpg", "1000270365.jpg", "1000270368.jpg", "1000270370.jpg", "1000270371.jpg", "1000270372.jpg", "1000270394.jpg", "1000270397.jpg", "1000218171.jpg", "1000218172.jpg", "1000218175.jpg", "1000218184.jpg", "1000218222.jpg", "1000218248.jpg", "1000218249.jpg", "1000218250.jpg", "1000218251.jpg", "1000218254.jpg", "1000208256.jpg", "1000218259.jpg", "1000218260.jpg", "1000218261.jpg", "1000218262.jpg", "1000218127.jpg", "1000218128.jpg", "1000218129.jpg", "1000218132.jpg", "1000218139.jpg", "1000218155.jpg", "1000218165.jpg", "1000218169.jpg"];

        const grid = document.getElementById('image-grid');
        const lightbox = document.getElementById('lightbox');
        const lightboxImg = lightbox.querySelector('img');
        const bttButton = document.getElementById('backToTop');

        imageList.forEach(imgName => {
            const card = document.createElement('article');
            card.className = 'card';
            card.innerHTML = `
                <div class="img-wrapper skeleton">
                    <div class="watermark">G.M. & SONS</div>
                    <img src="${imgName}" alt="G.M. & SONS" loading="lazy" onload="this.parentElement.classList.remove('skeleton')">
                </div>
                <h3 style="font-family: 'Cormorant Garamond', serif; font-size: 1.2rem; margin-top: 5px; color: #1B4332;">G.M. & SONS stoll</h3>
            `;
            card.onclick = () => { lightboxImg.src = imgName; lightbox.classList.add('active'); };
            grid.appendChild(card);
        });

        window.onscroll = () => {
            bttButton.style.display = (window.scrollY > 300) ? "block" : "none";
        };
        bttButton.onclick = () => window.scrollTo({top: 0, behavior: 'smooth'});
        lightbox.onclick = () => lightbox.classList.remove('active');
    </script>
</body>
</html>
