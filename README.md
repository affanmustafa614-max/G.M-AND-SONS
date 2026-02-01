<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>G.M. & SONS | Luxury Indian Textiles</title>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700&display=swap" rel="stylesheet">
    
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { font-family: 'Georgia', serif; background-color: #FDFCFB; color: #2D2D2D; }

        /* Navigation */
        nav { display: flex; justify-content: space-between; align-items: center; padding: 1.5rem 8%; border-bottom: 1px solid #EAE0D5; }
        
        .logo { 
            font-family: 'Playfair Display', serif; 
            font-size: 2.5rem; 
            font-weight: bold; 
            color: #1B4332; 
            text-transform: uppercase; 
            letter-spacing: 2px;
        }

        nav ul { display: flex; list-style: none; }
        nav ul li { margin-left: 1.5rem; }
        nav ul li a { text-decoration: none; color: #2D2D2D; font-size: 0.8rem; text-transform: uppercase; }

        /* Side-by-Side Container */
        .main-container { 
            display: flex; 
            flex-wrap: wrap; 
            gap: 20px; 
            padding: 2rem 5%; 
        }

        .collection-column { 
            flex: 1; 
            min-width: 300px; 
            border: 1px solid #EAE0D5;
            padding: 1rem;
            background: #fff;
        }

        .section-title { text-align: center; margin-bottom: 2rem; color: #1B4332; text-transform: uppercase; border-bottom: 2px solid #D4AF37; padding-bottom: 10px; }

        /* Grid for images */
        .grid { 
            display: grid; 
            grid-template-columns: repeat(auto-fill, minmax(140px, 1fr)); 
            gap: 15px; 
        }

        .card img { 
            width: 100%; 
            height: 200px; 
            object-fit: cover; 
            border: 1px solid #eee;
            transition: 0.3s;
        }
        .card img:hover { transform: scale(1.05); }

        footer { background: #1B1B1B; color: #FDFCFB; padding: 3rem; text-align: center; margin-top: 5rem; }
    </style>
</head>
<body>

    <nav>
        <div class="logo">G.M. & SONS</div>
        <ul>
            <li><a href="#">8090307576-Moin</a></li>
            <li><a href="#">8887792884-Affan</a></li>
        </ul>
    </nav>

    <main class="main-container">
        
        <section class="collection-column">
            <h2 class="section-title">Handloom</h2>
            <div class="grid">
                <div class="card"><img src="1000295702.jpg"></div>
                <div class="card"><img src="1000295705.jpg"></div>
                <div class="card"><img src="1000295711.jpg"></div>
                <div class="card"><img src="1000295720.jpg"></div>
            </div>
        </section>

        <section class="collection-column">
            <h2 class="section-title">Powerloom</h2>
            <div class="grid">
                <div class="card"><img src="1000270449.jpg"></div>
                <div class="card"><img src="1000270450.jpg"></div>
                <div class="card"><img src="1000270452.jpg"></div>
                <div class="card"><img src="1000270453.jpg"></div>
            </div>
        </section>

    </main>

    <footer>
        <p>&copy; G.M. & SONS. All Rights Reserved.</p>
        <p>SINCE 1976</p>
        <p>-- PLEASE VISIT AGAIN --</p>
    </footer>

</body>
</html>
