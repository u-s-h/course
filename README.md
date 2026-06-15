<html lang="ur" dir="rtl" id="appTheme">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GB Tourist Information Hub | Prime Solutions</title>
    <script src="https://www.gstatic.com/firebasejs/10.8.0/firebase-app-compat.js"></script>
    <script src="https://www.gstatic.com/firebasejs/10.8.0/firebase-database-compat.js"></script>
    <style>
        :root { --main: #00d4ff; --bg: #0f172a; --card: rgba(255,255,255,0.05); }
        .light { --bg: #f8fafc; --card: rgba(0,0,0,0.05); --text: #1e293b; }
        body { background: var(--bg); color: var(--text, #fff); font-family: 'Segoe UI', sans-serif; margin: 0; padding: 20px; transition: 0.5s; }
        .container { max-width: 600px; margin: auto; }
        .box { background: var(--card); padding: 20px; border-radius: 25px; margin-bottom: 20px; backdrop-filter: blur(15px); border: 1px solid rgba(255,255,255,0.1); }
        .data-card { background: #1e293b; padding: 15px; border-radius: 15px; margin-bottom: 10px; border-right: 5px solid var(--main); display: flex; justify-content: space-between; align-items: center; }
        input, select { width: 100%; padding: 15px; margin: 10px 0; border-radius: 15px; border: none; background: rgba(0,0,0,0.1); color: var(--text, #fff); outline: none; }
        button { width: 100%; padding: 15px; background: linear-gradient(90deg, #00d4ff, #0055ff); border: none; border-radius: 15px; font-weight: bold; cursor: pointer; color: white; font-size: 1.1rem; }
        .modal { display: none; position: fixed; top:0; left:0; width: 100%; height: 100%; background: #000; padding: 20px; overflow-y: auto; z-index: 9999; }
    </style>
</head>
<body>

<div class="container">
    <header style="text-align: center;">
        <h1 onclick="taps++" style="cursor:pointer; color: var(--main);">🏔️ GB Tourist Information Hub</h1>
        <p>Managed by Prime Solutions</p>
        <button style="width: auto; padding: 5px 20px;" onclick="toggleTheme()">تھیم موڈ 🌓</button>
    </header>

    <div class="box">
        <h3 style="text-align:center;">اسپیشل ڈیل ختم ہونے میں: <span id="timer" style="color:#ef4444;">24:00:00</span></h3>
    </div>

    <div class="box">
        <h3>ٹور معلومات حاصل کریں</h3>
        <input type="text" id="name" placeholder="آپ کا نام">
        <select id="city">
            <option value="استور">استور</option><option value="ہنزہ">ہنزہ</option><option value="سکردو">سکردو</option>
            <option value="گلگت">گلگت</option><option value="فیری میڈوز">فیری میڈوز</option><option value="دیوسائی">دیوسائی</option>
            <option value="شگر">شگر</option><option value="خپلو">خپلو</option><option value="غذر">غذر</option>
        </select>
        <button onclick="bookNow()">واٹس ایپ پر رابطہ کریں 💬</button>
    </div>
</div>

<!-- Admin Panel -->
<div id="adminPanel" class="modal">
    <div class="container">
        <h2 style="color:var(--main);">🔐 ایڈمن پینل</h2>
        <button onclick="clearAllData()" style="background:red; margin-bottom:10px;">تمام ڈیٹا صاف کریں (Clear All)</button>
        <div id="adminData"></div>
        <button onclick="document.getElementById('adminPanel').style.display='none'" style="margin-top:20px;">بند کریں</button>
    </div>
</div>

<script>
    firebase.initializeApp({databaseURL: "https://gilgit-79048-default-rtdb.firebaseio.com"});
    const db = firebase.database();

    function toggleTheme() { document.getElementById('appTheme').classList.toggle('light'); }

    // Countdown
    let time = 86400;
    setInterval(() => {
        time--; let h = Math.floor(time/3600), m = Math.floor((time%3600)/60), s = time%60;
        document.getElementById('timer').innerText = `${h}:${m}:${s}`;
    }, 1000);

    function bookNow() {
        let n = document.getElementById('name').value;
        let c = document.getElementById('city').value;
        db.ref('quotes').push({ name: n, city: c });
        window.open(`https://wa.me/923332637235?text=ہیلو، میرا نام ${n} ہے اور میں ${c} کے بارے میں معلومات چاہتا ہوں۔`, '_blank');
    }

    let taps = 0;
    document.querySelector('h1').onclick = () => {
        if(++taps === 4) {
            if(prompt("Admin Key:") === "5426") {
                document.getElementById('adminPanel').style.display = 'block';
                db.ref('quotes').on('value', snap => {
                    let html = "";
                    snap.forEach(s => { html += `<div class="data-card">👤 ${s.val().name} | 🗺️ ${s.val().city} <button onclick="db.ref('quotes/${s.key}').remove()" style="background:red; padding:5px 10px;">❌</button></div>`; });
                    document.getElementById('adminData').innerHTML = html;
                });
            }
            taps = 0;
        }
    }

    function clearAllData() { if(confirm("ڈیٹا ڈیلیٹ کریں؟")) db.ref('quotes').remove(); }
</script>
</body>
</html>
