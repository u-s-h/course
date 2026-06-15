<html lang="ur">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Discover GB - Tourist App Hub</title>
    <style>
        /* Base & Reset Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
            -webkit-tap-highlight-color: transparent;
        }

        body {
            background-color: #f1f5f9;
            color: #1e293b;
            padding-bottom: 70px; 
            direction: rtl; 
        }

        /* App Top Header */
        .app-header {
            background-color: #1e3a8a;
            color: white;
            padding: 15px;
            text-align: center;
            font-size: 1.2rem;
            font-weight: bold;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 8px rgba(0,0,0,0.1);
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 10px;
        }

        /* Hero App Banner */
        .app-banner {
            background: linear-gradient(rgba(30, 58, 138, 0.6), rgba(30, 58, 138, 0.8)), url('https://images.unsplash.com/photo-1548013146-72479768bada?q=80&w=600') no-repeat center center/cover;
            height: 200px;
            color: white;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 20px;
            margin-bottom: 15px;
        }

        .app-banner h2 {
            font-size: 1.8rem;
            margin-bottom: 5px;
        }

        .app-banner p {
            font-size: 0.9rem;
            opacity: 0.9;
        }

        .app-container {
            padding: 0 15px;
        }

        /* App Search Bar */
        .search-box {
            background: white;
            display: flex;
            align-items: center;
            padding: 10px 15px;
            border-radius: 12px;
            box-shadow: 0 2px 6px rgba(0,0,0,0.05);
            margin-bottom: 20px;
        }

        .search-box input {
            width: 100%;
            border: none;
            outline: none;
            font-size: 1rem;
            background: transparent;
        }

        /* Quick Actions Grid */
        .action-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 12px;
            margin-bottom: 25px;
        }

        .action-item {
            background: white;
            padding: 15px 10px;
            border-radius: 12px;
            text-align: center;
            box-shadow: 0 2px 6px rgba(0,0,0,0.04);
            font-size: 0.85rem;
            font-weight: bold;
            color: #1e3a8a;
            text-decoration: none;
        }

        .action-item .icon {
            font-size: 1.6rem;
            margin-bottom: 5px;
            display: block;
        }

        /* Section Title */
        .section-title {
            font-size: 1.2rem;
            color: #0f172a;
            margin-bottom: 12px;
            padding-right: 5px;
            border-right: 4px solid #2563eb;
        }

        /* Cards Layout */
        .card-stack {
            display: flex;
            flex-direction: column;
            gap: 15px;
            margin-bottom: 25px;
        }

        .app-card {
            background: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 2px 8px rgba(0,0,0,0.04);
        }

        .app-card img {
            width: 100%;
            height: 160px;
            object-fit: cover;
        }

        .app-card-content {
            padding: 15px;
        }

        .app-card-content h4 {
            font-size: 1.1rem;
            color: #1e3a8a;
            margin-bottom: 5px;
        }

        .app-card-content p {
            font-size: 0.9rem;
            color: #64748b;
        }

        /* Services Directory */
        .service-list {
            background: white;
            border-radius: 12px;
            padding: 10px;
            margin-bottom: 25px;
            box-shadow: 0 2px 8px rgba(0,0,0,0.04);
        }

        .service-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 12px 8px;
            border-bottom: 1px solid #f1f5f9;
        }

        .service-name {
            font-weight: bold;
            font-size: 0.95rem;
        }

        .service-price {
            background: #dcfce7;
            color: #166534;
            padding: 4px 10px;
            border-radius: 20px;
            font-size: 0.85rem;
            font-weight: bold;
        }

        /* Review Section */
        .app-feedback {
            background: white;
            border-radius: 12px;
            padding: 15px;
            box-shadow: 0 2px 8px rgba(0,0,0,0.04);
            margin-bottom: 20px;
        }

        .app-feedback input, .app-feedback textarea {
            width: 100%;
            padding: 10px;
            margin-bottom: 10px;
            border: 1px solid #cbd5e1;
            border-radius: 8px;
            outline: none;
            font-size: 0.9rem;
        }

        .app-feedback button {
            width: 100%;
            background-color: #1e3a8a;
            color: white;
            border: none;
            padding: 12px;
            border-radius: 8px;
            font-weight: bold;
            font-size: 1rem;
            cursor: pointer;
        }

        /* Bottom Navigation Dock */
        .bottom-nav {
            position: fixed;
            bottom: 0;
            left: 0;
            right: 0;
            height: 65px;
            background: white;
            display: flex;
            justify-content: space-around;
            align-items: center;
            box-shadow: 0 -2px 10px rgba(0,0,0,0.08);
            z-index: 2000;
        }

        .nav-tab {
            display: flex;
            flex-direction: column;
            align-items: center;
            color: #64748b;
            text-decoration: none;
            font-size: 0.75rem;
            font-weight: bold;
            width: 25%;
        }

        .nav-tab.active {
            color: #2563eb;
        }

        .nav-tab .tab-icon {
            font-size: 1.4rem;
            margin-bottom: 2px;
        }

        .whatsapp-float-btn {
            background-color: #25D366;
            color: white;
            width: 50px;
            height: 50px;
            border-radius: 50px;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 1.5rem;
            box-shadow: 0 4px 10px rgba(0,0,0,0.15);
            text-decoration: none;
        }
    </style>

    <!-- Firebase Compatibility SDKs (GitHub Pages کے لیے سب سے بیسٹ اور آسان طریقہ) -->
    <script src="https://www.gstatic.com/firebasejs/10.8.0/firebase-app-compat.js"></script>
    <script src="https://www.gstatic.com/firebasejs/10.8.0/firebase-database-compat.js"></script>
</head>
<body>

    <!-- App Top Bar -->
    <div class="app-header">
        <span>🏔️ Discover GB Hub</span>
    </div>

    <!-- App Banner -->
    <div class="app-banner" id="home-sec">
        <h2>گلگت بلتستان پورٹل</h2>
        <p>جنت نظیر وادیوں کی مکمل سفری گائیڈ</p>
    </div>

    <!-- Main Content App Views -->
    <div class="app-container">

        <!-- Search Bar -->
        <div class="search-box">
            <input type="text" id="appSearch" onkeyup="filterAppCards()" placeholder="وادی یا مقام کا نام لکھیں...">
        </div>

        <!-- Quick Action Menu -->
        <div class="action-grid">
            <a href="#places-sec" class="action-item"><span class="icon">🗺️</span>مقامات</a>
            <a href="#services-sec" class="action-item"><span class="icon">🚗</span>ٹرانسپورٹ</a>
            <a href="tel:1122" class="action-item"><span class="icon">🚨</span>ہیلپ لائن</a>
        </div>

        <!-- Destinations Section -->
        <h3 class="section-title" id="places-sec">مشہور وادیاں</h3>
        <div class="card-stack" id="appCardStack">
            <div class="app-card">
                <img src="https://images.unsplash.com/photo-1627483262769-04d0a1401487?q=80&w=600" alt="Hunza">
                <div class="app-card-content">
                    <h4>ہنزہ وادی (Hunza Valley)</h4>
                    <p>خوبصورت پہاڑ، التت اور بلتت قلعے، اور مہمان نواز لوکل کلچر۔</p>
                </div>
            </div>

            <div class="app-card">
                <img src="https://images.unsplash.com/photo-1589308078059-be1415eab4c3?q=80&w=600" alt="Attabad">
                <div class="app-card-content">
                    <h4>عطا آباد جھیل (Attabad Lake)</h4>
                    <p>شاندار نیلے پانی کی جھیل، بوٹنگ اور جیٹ اسکیئنگ کا مرکز۔</p>
                </div>
            </div>

            <div class="app-card">
                <img src="https://images.unsplash.com/photo-1605649487212-47bdab064df7?q=80&w=600" alt="Skardu">
                <div class="app-card-content">
                    <h4>سکردو وادی (Skardu Valley)</h4>
                    <p>بلتستان کا مرکز، شنگریلا جھیل اور سرفرنگا سرد ریگستان۔</p>
                </div>
            </div>
        </div>

        <!-- Services Section -->
        <h3 class="section-title" id="services-sec">لوکل سروسز ریٹس</h3>
        <div class="service-list">
            <div class="service-item">
                <span class="service-name">Prado / Jeep (لوکل ٹور)</span>
                <span class="service-price">12,000 PKR</span>
            </div>
            <div class="service-item">
                <span class="service-name">Hiace Grand Cabin (یومیہ)</span>
                <span class="service-price">18,000 PKR</span>
            </div>
            <div class="service-item">
                <span class="service-name">لوکل ٹور گائیڈ سروس</span>
                <span class="service-price">3,500 PKR</span>
            </div>
        </div>

        <!-- Firebase Live Review Section -->
        <h3 class="section-title" id="feed-sec">سیاحوں کا فیڈ بیک (Live)</h3>
        <div class="app-feedback">
            <input type="text" id="appUser" placeholder="آپ کا نام">
            <textarea id="appMsg" rows="3" placeholder="اپنا تجربہ لکھیں..."></textarea>
            <button onclick="submitAppFeedback()">ریویو جمع کریں</button>
            
            <!-- یہ ڈو (Div) اب فائر بیس سے لائیو کمنٹس لوڈ کرے گا -->
            <div id="appCommentsBox" style="margin-top: 15px;">
                <p style="text-align: center; color: #64748b; font-size: 0.9rem;" id="loadingText">ریویوز لوڈ ہو رہے ہیں...</p>
            </div>
        </div>

    </div>

    <!-- Bottom App Navigation Dock -->
    <div class="bottom-nav">
        <a href="#home-sec" class="nav-tab active" onclick="setActiveTab(this)">
            <span class="tab-icon">🏠</span>
            <span>ہوم</span>
        </a>
        <a href="#places-sec" class="nav-tab" onclick="setActiveTab(this)">
            <span class="tab-icon">🗺️</span>
            <span>مقامات</span>
        </a>
        
        <a href="https://wa.me/923332637235" target="_blank" class="whatsapp-float-btn">
            💬
        </a>

        <a href="#services-sec" class="nav-tab" onclick="setActiveTab(this)">
            <span class="tab-icon">🚗</span>
            <span>سروسز</span>
        </a>
        <a href="#feed-sec" class="nav-tab" onclick="setActiveTab(this)">
            <span class="tab-icon">⭐</span>
            <span>رائے</span>
        </a>
    </div>

    <!-- Firebase Logic & App Scripts -->
    <script>
        // آپ کی فراہم کردہ فائر بیس کنفیگریشن
        const firebaseConfig = {
          apiKey: "AIzaSyBiti-Ih5nxvRQ8Xt9YImiN1X3RnPoXoTI",
          authDomain: "gilgit-79048.firebaseapp.com",
          databaseURL: "https://gilgit-79048-default-rtdb.firebaseio.com",
          projectId: "gilgit-79048",
          storageBucket: "gilgit-79048.firebasestorage.app",
          messagingSenderId: "784852692962",
          appId: "1:784852692962:web:eab87b313e024ebf7953bb"
        };

        // فائر بیس انیشیلائزیشن
        firebase.initializeApp(firebaseConfig);
        const database = firebase.database();

        // 1. فائر بیس سے کمنٹس لائیو سننا (Read Comments)
        database.ref('reviews').on('value', (snapshot) => {
            let box = document.getElementById('appCommentsBox');
            let loadingText = document.getElementById('loadingText');
            if(loadingText) loadingText.remove();
            
            box.innerHTML = ""; // پرانا لوکل ڈیٹا صاف کریں
            
            let data = snapshot.val();
            if(data) {
                // کمنٹس کو الٹے آرڈر (Newest First) میں دکھانے کے لیے
                Object.keys(data).reverse().forEach((key) => {
                    let item = document.createElement('div');
                    item.style.cssText = "background: #f8fafc; padding: 10px; border-radius: 6px; margin-top: 10px; font-size: 0.9rem; border-left: 3px solid #1e3a8a; text-align: right;";
                    item.innerHTML = `<strong>${data[key].username}:</strong> <p style="margin-top:3px; color:#475569;">${data[key].message}</p>`;
                    box.appendChild(item);
                });
            } else {
                box.innerHTML = `<p style="text-align: center; color: #64748b; font-size: 0.9rem;">ابھی تک کوئی فیڈ بیک نہیں ہے۔ پہلے وزٹر بنیں!</p>`;
            }
        });

        // 2. فائر بیس میں نیا کمنٹ سیو کرنا (Write Comment)
        function submitAppFeedback() {
            let user = document.getElementById('appUser').value;
            let msg = document.getElementById('appMsg').value;
            
            if(user.trim() === "" || msg.trim() === "") {
                alert("براہ کرم تمام معلومات لکھیں!");
                return;
            }
            
            // فائر بیس ریل ٹائم ڈیٹا بیس میں پش کرنا
            database.ref('reviews').push({
                username: user,
                message: msg,
                timestamp: Date.now()
            }).then(() => {
                // فارم صاف کریں
                document.getElementById('appUser').value = "";
                document.getElementById('appMsg').value = "";
            }).catch((error) => {
                alert("خرابی: ڈیٹا سیو نہیں ہو سکا۔ رولز چیک کریں!");
                console.error(error);
            });
        }

        // سرچ فلٹر
        function filterAppCards() {
            let query = document.getElementById('appSearch').value.toLowerCase();
            let cards = document.getElementsByClassName('app-card');
            for(let i=0; i<cards.length; i++) {
                let text = cards[i].innerText.toLowerCase();
                if(text.includes(query)) {
                    cards[i].style.display = "block";
                } else {
                    cards[i].style.display = "none";
                }
            }
        }

        // ایکٹیو ٹیب ہائی لائٹ
        function setActiveTab(element) {
            let tabs = document.getElementsByClassName('nav-tab');
            for(let i=0; i<tabs.length; i++) {
                tabs[i].classList.remove('active');
            }
            element.classList.add('active');
        }
    </script>

</body>
</html>
