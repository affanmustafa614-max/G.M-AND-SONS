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

        /* --- HEADER (STICKY REMOVED) --- */
        header {
            padding: 2rem 5%;
            border-bottom: 3px solid #D4AF37; 
            background: #F4C2C2; 
            text-align: center;
            box-shadow: 0 4px 20px rgba(0,0,0,0.08);
            /* Removed position: sticky and top: 0 */
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
