<html lang="ur">
<head>
    <meta charset="UTF-8">
    <title>Discover GB | Official Portal</title>
    <style>
        body { background: #050505; color: #fff; font-family: 'Poppins', sans-serif; margin: 0; padding: 20px; }
        .navbar { display: flex; justify-content: space-between; padding: 20px; background: rgba(255,255,255,0.05); border-radius: 15px; }
        .card { background: #1a1a1a; padding: 20px; margin: 10px 0; border-radius: 10px; }
    </style>
</head>
<body>

    <nav class="navbar">
        <div class="logo" style="cursor:pointer; color:#00d4ff; font-weight:bold;">Discover GB</div>
        <div>
            <button onclick="loginWithGoogle()">Google Login</button>
            <button onclick="showHistory()">View History</button>
        </div>
    </nav>

    <section style="margin-top:50px;">
        <h2>Book Your Trip</h2>
        <select id="destination">
            <option value="Hunza">Hunza</option>
            <option value="Skardu">Skardu</option>
            <option value="Astore">Astore</option>
        </select>
        <button onclick="saveBooking()">Confirm Booking</button>
    </section>

    <div id="history-container" style="margin-top:30px;">
        <h3>Aapki Booking History</h3>
        <ul id="history-list"></ul>
    </div>

    <script type="module">
        import { initializeApp } from "https://www.gstatic.com/firebasejs/10.0.0/firebase-app.js";
        import { getAuth, GoogleAuthProvider, signInWithPopup } from "https://www.gstatic.com/firebasejs/10.0.0/firebase-auth.js";
        import { getFirestore, addDoc, collection, query, where, getDocs } from "https://www.gstatic.com/firebasejs/10.0.0/firebase-firestore.js";

        const firebaseConfig = { /* APNI CONFIG YAHAN PASTE KARO SWEETIE */ };
        const app = initializeApp(firebaseConfig);
        const auth = getAuth();
        const db = getFirestore();

        // 1. Google Login
        window.loginWithGoogle = async () => {
            try {
                const result = await signInWithPopup(auth, new GoogleAuthProvider());
                alert("Welcome, " + result.user.displayName + "! Sweetie.");
            } catch (e) { alert("Login failed!"); }
        };

        // 2. Booking Save
        window.saveBooking = async () => {
            if (!auth.currentUser) return alert("Pehle login karo, sweetie!");
            const dest = document.getElementById("destination").value;
            await addDoc(collection(db, "bookings"), { destination: dest, userEmail: auth.currentUser.email, date: new Date().toLocaleDateString() });
            alert("Booking confirmed, sweetie!");
        };

        // 3. History Fetch
        window.showHistory = async () => {
            if (!auth.currentUser) return alert("Login karo, sweetie!");
            const q = query(collection(db, "bookings"), where("userEmail", "==", auth.currentUser.email));
            const list = document.getElementById("history-list");
            list.innerHTML = "";
            (await getDocs(q)).forEach(doc => {
                let li = document.createElement("li");
                li.innerText = doc.data().destination + " - " + doc.data().date;
                list.appendChild(li);
            });
        };

        // 4. Secret Admin (5426)
        let taps = 0;
        document.querySelector('.logo').addEventListener('click', () => {
            if (++taps === 5) {
                if (prompt("Enter Admin Key:") === "5426") alert("Welcome Admin, Sweetie!");
                taps = 0;
            }
        });
    </script>
</body>
</html>
