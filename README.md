<html lang="ur">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Discover Gilgit-Baltistan</title>
    <style>
        /* Modern Dark Theme Design */
        body { margin: 0; font-family: 'Segoe UI', sans-serif; background-color: #0a0a0a; color: #fff; }
        
        .navbar { display: flex; justify-content: space-between; align-items: center; padding: 20px 8%; background: rgba(255, 255, 255, 0.03); backdrop-filter: blur(10px); }
        .logo { font-size: 1.5rem; font-weight: bold; color: #00d4ff; }
        .nav-links a { color: white; text-decoration: none; margin: 0 15px; }
        .login-btn { padding: 8px 20px; border-radius: 20px; border: none; background: #00d4ff; cursor: pointer; }

        .hero { text-align: center; padding: 100px 20px; background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), url('https://images.unsplash.com/photo-1600585154340-be6161a56a0c?q=80&w=2070&auto=format&fit=crop'); background-size: cover; height: 60vh; display: flex; flex-direction: column; justify-content: center; align-items: center; }
        
        .container { padding: 50px 8%; }
        .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 20px; }
        .card { background: #1a1a1a; padding: 20px; border-radius: 15px; transition: 0.4s; border: 1px solid #333; }
        .card:hover { transform: translateY(-10px); border-color: #00d4ff; box-shadow: 0 10px 20px rgba(0,212,255,0.2); }
    </style>
</head>
<body>

    <nav class="navbar">
        <div class="logo">Discover GB</div>
        <div class="nav-links">
            <a href="#">Home</a>
            <a href="#">Destinations</a>
            <a href="#">Culture</a>
        </div>
        <button class="login-btn">Login/Signup</button>
    </nav>

    <section class="hero">
        <h1>Khush Amdeed Gilgit-Baltistan Mein</h1>
        <p>Explore the hidden paradise and the land of giants.</p>
        <button style="padding: 10px 30px; border-radius: 25px; border: none; cursor: pointer; margin-top: 20px;">Start Your Adventure</button>
    </section>

    <div class="container">
        <h2>Top Destinations</h2>
        <div class="grid">
            <div class="card"><h3>Hunza Valley</h3><p>Explore the beauty of the Karakoram mountains.</p></div>
            <div class="card"><h3>Attabad Lake</h3><p>Witness the stunning turquoise waters.</p></div>
            <div class="card"><h3>Skardu</h3><p>The gateway to the highest peaks.</p></div>
        </div>
    </div>

</body>
</html>
