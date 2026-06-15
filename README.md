<html lang="ur" dir="rtl" id="appHtml">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Discover GB - Professional Portal</title>
    
    <script src="https://www.gstatic.com/firebasejs/10.8.0/firebase-app-compat.js"></script>
    <script src="https://www.gstatic.com/firebasejs/10.8.0/firebase-auth-compat.js"></script>
    <script src="https://www.gstatic.com/firebasejs/10.8.0/firebase-database-compat.js"></script>
    
    <style>
        :root {
            --bg-gradient: linear-gradient(135deg, #0f172a 0%, #1e1b4b 100%);
            --glass-bg: rgba(255, 255, 255, 0.08);
            --glass-border: rgba(255, 255, 255, 0.15);
            --accent-color: #38bdf8;
            --text-main: #f8fafc;
        }
        body { background: var(--bg-gradient); color: var(--text-main); font-family: sans-serif; min-height: 100vh; padding-bottom: 80px; }
        .glass-card { background: var(--glass-bg); backdrop-filter: blur(10px); border: 1px solid var(--glass-border); border-radius: 20px; padding: 20px; margin: 15px; }
        .action-btn { background: var(--accent-color); color: #000; border: none; padding: 12px; width: 100%; border-radius: 12px; font-weight: bold; cursor: pointer; margin-top: 10px; }
        .admin-modal, .receipt-modal { display: none; position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: rgba(0,0,0,0.9); z-index: 9999; padding: 20px; overflow-y: auto; }
        .data-row { background: rgba(255,255,255,0.1); padding: 10px; margin-bottom: 10px; border-radius: 10px; }
    </style>
</head>
<body>

    <div style="padding: 20px; display: flex; justify-content: space-between; align-items: center;">
        <h2 onclick="triggerSecretAdmin()" style="cursor: pointer;">🏔️ Discover GB</h2>
        <button onclick="toggleLanguage()" id="langBtn" style="padding: 5px 15px; border-radius: 20px;">English</button>
    </div>

    <div class="glass-card">
        <h3 id="formTitle">مفت ٹور پلان حاصل کریں</h3>
        <input type="text" id="custName" placeholder="آپ کا نام" style="width:100%; padding:10px; margin-bottom:10px; border-radius:10px;">
        <input type="text" id="custContact" placeholder="واٹس ایپ نمبر یا ای میل" style="width:100%; padding:10px; margin-bottom:10px; border-radius:10px;">
        <select id="destCity" style="width:100%; padding:10px; margin-bottom:10px; border-radius:10px;">
            <option value="استور">استور</option>
            <option value="گلگت">گلگت</option>
            <option value="سکردو">سکردو</option>
        </select>
        <input type="date" id="tourDate" style="width:100%; padding:10px; margin-bottom:10px; border-radius:10px;">
        <button class="action-btn" onclick="sendQuoteRequest()">درخواست جمع کریں</button>
    </div>

    <!-- Receipt Modal -->
    <div class="receipt-modal" id="receiptModal">
        <div class="glass-card" style="text-align:center;">
            <h2>✅ درخواست موصول ہوئی</h2>
            <div id="receiptContent" style="text-align:right; border:1px dashed #fff; padding:10px;"></div>
            <button class="action-btn" onclick="closeReceipt()">اوکے (Save Screenshot)</button>
        </div>
    </div>

    <!-- Admin Modal -->
    <div class="admin-modal" id="adminPanel">
        <h2 style="color:var(--accent-color);">🔐 سیکیور ایڈمن پینل</h2>
        <div id="adminDataContainer"></div>
        <button class="action-btn" onclick="closeAdmin()">بند کریں</button>
    </div>

    <script>
        const firebaseConfig = { apiKey: "AIzaSyBiti-Ih5nxvRQ8Xt9YImiN1X3RnPoXoTI", authDomain: "gilgit-79048.firebaseapp.com", databaseURL: "https://gilgit-79048-default-rtdb.firebaseio.com", projectId: "gilgit-79048" };
        firebase.initializeApp(firebaseConfig);
        const db = firebase.database();

        let tapCount = 0;
        function triggerSecretAdmin() {
            tapCount++;
            if(tapCount === 4) {
                let key = prompt("خفیہ کوڈ درج کریں:");
                if(key === "5426") {
                    document.getElementById("adminPanel").style.display = "block";
                    loadAdminData();
                }
                tapCount = 0;
            }
        }

        function sendQuoteRequest() {
            let name = document.getElementById("custName").value;
            let contact = document.getElementById("custContact").value;
            let city = document.getElementById("destCity").value;
            let date = document.getElementById("tourDate").value;

            db.ref('quotes').push({ name, contact, city, date, time: Date.now() });
            
            document.getElementById("receiptContent").innerHTML = `<p>نام: ${name}</p><p>رابطہ: ${contact}</p><p>شہر: ${city}</p><p>تاریخ: ${date}</p>`;
            document.getElementById("receiptModal").style.display = "block";
        }

        function loadAdminData() {
            db.ref('quotes').on('value', (snap) => {
                let data = snap.val();
                let html = "";
                for(let key in data) {
                    html += `<div class="data-row">👤 ${data[key].name}<br>📞 ${data[key].contact}<br>🗺️ ${data[key].city}<br>📅 ${data[key].date}</div>`;
                }
                document.getElementById("adminDataContainer").innerHTML = html;
            });
        }

        function closeReceipt() { document.getElementById("receiptModal").style.display = "none"; }
        function closeAdmin() { document.getElementById("adminPanel").style.display = "none"; }
        
        function toggleLanguage() {
            let btn = document.getElementById("langBtn");
            let title = document.getElementById("formTitle");
            if(btn.innerText === "English") {
                btn.innerText = "اردو";
                title.innerText = "Get Free Tour Plan";
            } else {
                btn.innerText = "English";
                title.innerText = "مفت ٹور پلان حاصل کریں";
            }
        }
    </script>
</body>
</html>
