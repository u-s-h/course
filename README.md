<html lang="ur" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Prime Solutions | GB Tourism Hub</title>
    <script type="module">
        import { initializeApp } from "https://www.gstatic.com/firebasejs/10.8.0/firebase-app.js";
        import { getAuth, GoogleAuthProvider, signInWithPopup, signOut } from "https://www.gstatic.com/firebasejs/10.8.0/firebase-auth.js";
        import { getDatabase, ref, push, onValue, remove } from "https://www.gstatic.com/firebasejs/10.8.0/firebase-database.js";

        const firebaseConfig = {
            apiKey: "AIzaSyBiti-Ih5nxvRQ8Xt9YImiN1X3RnPoXoTI",
            authDomain: "gilgit-79048.firebaseapp.com",
            databaseURL: "https://gilgit-79048-default-rtdb.firebaseio.com",
            projectId: "gilgit-79048",
            storageBucket: "gilgit-79048.firebasestorage.app",
            messagingSenderId: "784852692962",
            appId: "1:784852692962:web:eab87b313e024ebf7953bb"
        };
        const app = initializeApp(firebaseConfig);
        const auth = getAuth(app);
        const db = getDatabase(app);
        const provider = new GoogleAuthProvider();

        window.login = () => signInWithPopup(auth, provider);
        window.saveBooking = () => {
            const city = document.getElementById('city').value;
            const phone = document.getElementById('phone').value;
            push(ref(db, 'bookings/' + auth.currentUser.uid), { city, phone, date: new Date().toLocaleDateString(), status: "✅ تصدیق شدہ" });
            alert("بکنگ موصول ہوئی!");
        };
        
        // Admin Trigger
        let taps = 0;
        window.checkAdmin = () => { if(++taps === 5 && prompt("Key:") === "5426") document.getElementById('adminPanel').style.display='block'; };
    </script>
    <style>
        :root { --main: #00d4ff; --bg: #0f172a; }
        body { background: var(--bg); color: white; font-family: sans-serif; padding: 20px; }
        .glass { background: rgba(255,255,255,0.05); padding: 20px; border-radius: 20px; margin: 10px auto; max-width: 500px; border: 1px solid rgba(255,255,255,0.1); }
        button { background: var(--main); border: none; padding: 10px; width: 100%; border-radius: 10px; font-weight: bold; cursor: pointer; margin-top: 10px; }
        .card { background: #1e293b; padding: 15px; border-radius: 10px; margin-top: 10px; }
    </style>
</head>
<body>

<div class="glass" style="text-align:center;">
    <h1 onclick="checkAdmin()">🏔️ Prime Solutions GB</h1>
    <p>آپ کا بہترین سفری ساتھی (استور، گلگت بلتستان)</p>
</div>

<!-- Services & Gallery -->
<div class="glass">
    <h3>خدمات (Services)</h3>
    <p>• فری کوٹیشن • مقامی گائیڈز • ہوٹل بکنگ • 24/7 سپورٹ</p>
    <img src="https://via.placeholder.com/500x200" style="width:100%; border-radius:15px;" alt="GB Gallery">
</div>

<!-- Booking & History -->
<div class="glass">
    <h3>بکنگ اور رسید</h3>
    <input type="text" id="phone" placeholder="واٹس ایپ نمبر" style="width:100%; padding:10px; border-radius:10px; border:none;">
    <select id="city" style="width:100%; padding:10px; margin-top:10px; border-radius:10px;">
        <option>استور</option><option>ہنزہ</option><option>سکردو</option>
    </select>
    <button onclick="login()">لاگ ان کریں</button>
    <button onclick="saveBooking()">بکنگ کنفرم کریں</button>
    <button onclick="alert('رسید: ID-9982 - Prime Solutions GB')">رسید (Receipt) دیکھیں</button>
</div>

<!-- FAQ & Privacy -->
<div class="glass">
    <h3>FAQ & Privacy</h3>
    <p><b>سوال:</b> کیا ڈیٹا محفوظ ہے؟ <br><b>جواب:</b> جی ہاں، پرائیویسی ہماری اولین ترجیح ہے۔</p>
</div>

<!-- Admin Panel -->
<div id="adminPanel" class="glass" style="display:none; position:fixed; top:0; z-index:99;">
    <h2>Admin Dashboard</h2>
    <div id="adminData"></div>
    <button onclick="document.getElementById('adminPanel').style.display='none'" style="background:red;">بند کریں</button>
</div>

<a href="https://wa.me/923332637235" style="position:fixed; bottom:20px; right:20px; background:#25D366; padding:15px; border-radius:50px; text-decoration:none; color:white;">💬 رابطہ کریں</a>

</body>
</html>
