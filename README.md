<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>G.M. & SONS - Luxury Stolls</title>
    
    <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@700&family=Playfair+Display:wght@400;700&display=swap" rel="stylesheet">
    
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; scroll-behavior: smooth; }
        
        body { 
            font-family: 'Playfair Display', serif; 
            background-color: #FFF5F7; 
            color: #1B4332; 
        }

        /* --- STICKY NAVIGATION --- */
        header {
            padding: 2rem 5%;
            border-bottom: 3px solid #D4AF37; 
            background: #F4C2C2; 
            text-align: center;
            box-shadow: 0 4px 20px rgba(0,0,0,0.08);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .brand-name { 
            font-size: clamp(2rem, 8vw, 4.5rem); 
            font-family: 'Cormorant Garamond', serif; 
            font-weight: 700; 
            letter-spacing: 8px; 
            color: #1B4332; 
            text-transform: uppercase;
            margin-bottom: 10px;
            transition: 0.4s;
        }

        .header-info {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            max-width: 1200px;
            margin: 0 auto;
            border-top: 1px solid rgba(27, 67, 50, 0.1);
            padding-top: 15px;
        }

        .tagline { font-size: 0.85rem; color: #5E503F; flex: 1; text-align: left; font-style: italic; }
        .contact-top { font-size: 0.9rem; color: #1B4332; flex: 1; text-align: right; font-weight: bold; }

        /* --- GRID OPTIMIZATION --- */
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 25px;
            padding: 30px 5%;
            max-width: 1400px;
            margin: 0 auto;
        }
        
        .card {
            background: white;
            border: 1px solid #F0EAD6;
            padding: 12px;
            text-align: center;
            transition: transform 0.4s cubic-bezier(0.165, 0.84, 0.44, 1), box-shadow 0.4s;
            cursor: pointer;
            position: relative;
        }

        .card:hover {
            box-shadow: 0 15px 35px rgba(0,0,0,0.1);
            transform: translateY(-8px);
        }

        .watermark {
            position: absolute;
            top: 50%; left: 50%;
            transform: translate(-50%, -50%) rotate(-45deg);
            font-size: 1.2rem;
            color: rgba(255, 255, 255, 0.3);
            font-weight: bold;
            text-transform: uppercase;
            pointer-events: none;
            z-index: 5;
            letter-spacing: 2px;
        }

        .img-wrapper { position: relative; overflow: hidden; background: #f9f9f9; }

        .skeleton {
            background: linear-gradient(110deg, #ececec 8%, #f5f5f5 18%, #ececec 33%);
            background-size: 200% 100%;
            animation: shimmer 1.5s linear infinite;
        }
        @keyframes shimmer { to { background-position-x: -200%; } }

        .card img {
            width: 100%;
            aspect-ratio: 3/4;
            object-fit: cover;
            border: 1px solid #EAE0D5;
            transition: transform 0.6s ease;
            display: block;
        }
        .card:hover img { transform: scale(1.05); }

        /* --- ENHANCED LIGHTBOX --- */
        #lightbox {
            display: none;
            position: fixed;
            z-index: 3000;
            top: 0; left: 0;
            width: 100%; height: 100%;
            background: rgba(0, 0, 0, 0.95);
            justify-content: center;
            align-items: center;
            user-select: none;
        }
        #lightbox.active { display: flex; }
        #lightbox img { max-width: 90%; max-height: 80vh; border: 3px solid #D4AF37; }

        .nav-btn {
            position: absolute;
            top: 50%;
            transform: translateY(-50%);
            background: rgba(255,255,255,0.1);
            color: white;
            border: none;
            font-size: 2rem;
            padding: 20px;
            cursor: pointer;
            transition: 0.3s;
        }
        .nav-btn:hover { background: #D4AF37; }
        #prevBtn { left: 10px; }
        #nextBtn { right: 10px; }
        #closeBtn { position: absolute; top: 20px; right: 20px; color: white; font-size: 3rem; cursor: pointer; }

        /* --- WHATSAPP & TOP BUTTON --- */
        .whatsapp-float {
            position: fixed;
            bottom: 30px;
            left: 30px;
            background: #25D366;
            color: white;
            padding: 12px 20px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: bold;
            display: flex;
            align-items: center;
            gap: 10px;
            z-index: 2000;
            box-shadow: 0 4px 15px rgba(0,0,0,0.2);
            transition: 0.3s;
        }
        .whatsapp-float:hover { transform: scale(1.05); background: #128C7E; }

        #backToTop {
            position: fixed;
            bottom: 30px;
            right: 30px;
            width: 50px; height: 50px;
            background: #1B4332;
            color: white;
            border: 2px solid #D4AF37;
            border-radius: 50%;
            cursor: pointer;
            display: none;
            z-index: 2000;
        }

        footer {
            background: #1B1B1B;
            color: #FDFCFB;
            padding: 4rem 2rem;
            text-align: center;
            border-top: 4px solid #D4AF37;
        }

        @media (max-width: 600px) {
            .header-info { flex-direction: column; gap: 10px; text-align: center; }
            .tagline, .contact-top { text-align: center; }
            .whatsapp-float span { display: none; }
            .whatsapp-float { padding: 15px; border-radius: 50%; }
        }
    </style>
</head>
<body>

    <a href="https://wa.me/918887792884" class="whatsapp-float" target="_blank">
        <img src="https://upload.wikimedia.org/wikipedia/commons/6/6b/WhatsApp.svg" width="25" alt="WA">
        <span>Order on WhatsApp</span>
    </a>

    <button id="backToTop" title="Back to Top">↑</button>

    <header>
        <div class="brand-name">G.M. & SONS</div>
        <div class="header-info">
            <div class="tagline">Handloom & Powerloom Commission Agent Since 1976</div>
            <div class="contact-top">Affan: +91 8887792884</div>
        </div>
    </header>

    <main>
        <div class="grid" id="image-grid"></div>
    </main>

    <div id="lightbox">
        <span id="closeBtn">&times;</span>
        <button class="nav-btn" id="prevBtn">&#10094;</button>
        <img src="" alt="Enlarged View">
        <button class="nav-btn" id="nextBtn">&#10095;</button>
    </div>

    <footer>
        <p>&copy; G.M. & SONS. All Rights Reserved.</p>
        <p style="margin-top: 20px; color: #D4AF37; letter-spacing: 3px; font-family: 'Cormorant Garamond', serif; font-size: 1.2rem;">-- PLEASE VISIT AGAIN --</p>
    </footer>

    <script>
        const rawImageList = ["1000295702.jpg", "1000295705.jpg", "1000295711.jpg", "1000295720.jpg", "1000295723.jpg", "1000295726.jpg", "1000295729.jpg", "1000295732.jpg", "1000295735.jpg", "1000295728.jpg", "1000296053.jpg", "1000296057.jpg", "1000296061.jpg", "1000214010.jpg", "1000214016.jpg", "1000270449.jpg", "1000270450.jpg", "1000270452.jpg", "1000270453.jpg", "1000270458.jpg", "1000270459.jpg", "1000271402.jpg", "1000271619.jpg", "1000271621.jpg", "1000271627.jpg", "1000271633.jpg", "1000271974.jpg", "1000271976.jpg", "1000271977.jpg", "1000271984.jpg", "1000271985.jpg", "1000271986.jpg", "1000271990.jpg", "1000273068.jpg", "1000273377.jpg", "1000273588.jpg", "1000273589.jpg", "1000273592.jpg", "1000273594.jpg", "1000273595.jpg", "1000273229.jpg", "1000293229.jpg", "1000293232.jpg", "1000293241.jpg", "1000293244.jpg", "1000293247.jpg", "1000293253.jpg", "1000293256.jpg", "1000293259.jpg", "1000293271.jpg", "1000293274.jpg", "1000295696.jpg", "1000271377.jpg", "1000271379.jpg", "1000271381.jpg", "1000271383.jpg", "1000271385.jpg", "1000271392.jpg", "1000271399.jpg", "1000271409.jpg", "1000271412.jpg", "1000271417.jpg", "1000271596.jpg", "1000271599.jpg", "1000271603.jpg", "1000270397.jpg", "1000270449.jpg", "1000270450.jpg", "1000270453.jpg", "1000270458.jpg", "1000271367.jpg", "1000271369.jpg", "1000271371.jpg", "1000271373.jpg", "1000271375.jpg", "1000271377.jpg", "1000271379.jpg", "1000271381.jpg", "1000218263.jpg", "1000218264.jpg", "1000218265.jpg", "1000218270.jpg", "1000218271.jpg", "1000270359.jpg", "1000270365.jpg", "1000270368.jpg", "1000270370.jpg", "1000270371.jpg", "1000270372.jpg", "1000270394.jpg", "1000270397.jpg", "1000218171.jpg", "1000218172.jpg", "1000218175.jpg", "1000218184.jpg", "1000218222.jpg", "1000218248.jpg", "1000218249.jpg", "1000218250.jpg", "1000218251.jpg", "1000218254.jpg", "1000208256.jpg", "1000218259.jpg", "1000218260.jpg", "1000218261.jpg", "1000218262.jpg", "1000218127.jpg", "1000218128.jpg", "1000218129.jpg", "1000218132.jpg", "1000218139.jpg", "1000218155.jpg", "1000218165.jpg", "1000218169.jpg"];

        // UNIQUE IMAGES CLEANUP
        const imageList = [...new Set(rawImageList)]; 
        
        const grid = document.getElementById('image-grid');
        const lightbox = document.getElementById('lightbox');
        const lightboxImg = lightbox.querySelector('img');
        const bttButton = document.getElementById('backToTop');
        let currentIndex = 0;

        // AUTO-FIX: Function to remove the card if image fails to load
        function removeBrokenImage(img) {
            console.warn("Hidden missing image:", img.src);
            img.closest('.card').style.display = 'none';
        }

        // GRID GENERATION
        imageList.forEach((imgName, index) => {
            const card = document.createElement('article');
            card.className = 'card';
            card.innerHTML = `
                <div class="img-wrapper skeleton">
                    <div class="watermark">G.M. & SONS</div>
                    <img src="${imgName}" 
                         alt="G.M. & SONS Stoll" 
                         loading="lazy" 
                         onerror="removeBrokenImage(this)" 
                         onload="this.parentElement.classList.remove('skeleton')">
                </div>
                <h3 style="font-family: 'Cormorant Garamond', serif; font-size: 1.1rem; margin-top: 12px; color: #1B4332; letter-spacing:1px;">LUXURY COLLECTION</h3>
            `;
            card.onclick = () => openLightbox(index);
            grid.appendChild(card);
        });

        // LIGHTBOX LOGIC
        function openLightbox(index) {
            currentIndex = index;
            updateLightboxImage();
            lightbox.classList.add('active');
            document.body.style.overflow = 'hidden';
        }

        function updateLightboxImage() {
            lightboxImg.src = imageList[currentIndex];
            // If the lightbox image itself is broken, we don't want a black screen
            lightboxImg.onerror = () => { lightboxImg.src = 'https://via.placeholder.com/600x800?text=Image+Not+Available'; };
        }

        document.getElementById('nextBtn').onclick = (e) => {
            e.stopPropagation();
            currentIndex = (currentIndex + 1) % imageList.length;
            updateLightboxImage();
        };

        document.getElementById('prevBtn').onclick = (e) => {
            e.stopPropagation();
            currentIndex = (currentIndex - 1 + imageList.length) % imageList.length;
            updateLightboxImage();
        };

        document.getElementById('closeBtn').onclick = () => {
            lightbox.classList.remove('active');
            document.body.style.overflow = 'auto';
        };

        lightbox.onclick = () => {
            lightbox.classList.remove('active');
            document.body.style.overflow = 'auto';
        };

        // NAV & UX
        window.onscroll = () => {
            bttButton.style.display = (window.scrollY > 400) ? "block" : "none";
        };
        bttButton.onclick = () => window.scrollTo({top: 0, behavior: 'smooth'});

        document.addEventListener('keydown', (e) => {
            if (!lightbox.classList.contains('active')) return;
            if (e.key === "ArrowRight") document.getElementById('nextBtn').click();
            if (e.key === "ArrowLeft") document.getElementById('prevBtn').click();
            if (e.key === "Escape") document.getElementById('closeBtn').click();
        });
    </script>
</body>
</html>
