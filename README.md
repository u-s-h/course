<html lang="ur">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Discover Gilgit-Baltistan</title>
    <style>
        body { background: #050505; color: #fff; font-family: 'Poppins', sans-serif; margin: 0; padding: 0; }
        .navbar { display: flex; justify-content: space-between; padding: 20px 5%; background: rgba(255,255,255,0.05); backdrop-filter: blur(10px); position: sticky; top: 0; }
        .hero { text-align: center; padding: 100px 20px; background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), url('https://images.unsplash.com/photo-1626621341517-b830d695d73d?auto=format&fit=crop&w=1920&q=80'); background-size: cover; }
        .container { padding: 40px 5%; }
        .card { background: #1a1a1a; padding: 20px; margin: 15px 0; border-radius: 15px; border: 1px solid #333; }
        button { padding: 10px 20px; border-radius: 20px; border: none; cursor: pointer; background: #00d4ff; font-weight: bold; }
    </style>
</head>
<body>

    <nav class="navbar">
        <div class="logo" style="cursor:pointer; font-size:1.5rem; font-weight:bold; color:#00d4ff;">Discover GB</div>
        <div>
            <button onclick="loginWithGoogle()">Login</button>
            <button onclick="showHistory()">History</button>
        </div>
    </nav>

    <section class="hero">
        <h1>Khush Amdeed Gilgit-Baltistan</h1>
        <p>Explore the hidden paradise.</p>
    </section>

    <div class="container">
        <h2>Book A Trip</h2>
        <select id="destination" style="padding:10px;">
            <option value="Hunza">Hunza</option>
            <option value="Skardu">Skardu</option>
            <option value="Astore">Astore</option>
        </select>
        <button onclick="saveBooking()">Confirm Booking</button>

        <div id="history-container" style="margin-top:30px;">
            <h3>Your Bookings</h3>
            <ul id="history-list"></ul>
        </div>
    </div>

    <script type="module">
        import { initializeApp } from "https://www.gstatic.com/firebasejs/10.0.0/firebase-app.js";
        import { getAuth, GoogleAuthProvider, signInWithPopup } from "https://www.gstatic.com/firebasejs/10.0.0/firebase-auth.js";
        import { getFirestore, addDoc, collection, query, where, getDocs } from "https://www.gstatic.com/firebasejs/10.0.0/firebase-firestore.js";

        const firebaseConfig = { /* APNI FIREBASE CONFIG YAHAN PASTE KAREIN */ };
        const app = initializeApp(firebaseConfig);
        const auth = getAuth();
        const db = getFirestore();

        window.loginWithGoogle = async () => {
            try { await signInWithPopup(auth, new GoogleAuthProvider()); alert("Welcome!"); } 
            catch (e) { alert("Login failed"); }
        };

        window.saveBooking = async () => {
            if (!auth.currentUser) return alert("Pehle login karein!");
            await addDoc(collection(db, "bookings"), { destination: document.getElementById("destination").value, userEmail: auth.currentUser.email, date: new Date().toLocaleDateString() });
            alert("Booked!");
        };

        window.showHistory = async () => {
            if (!auth.currentUser) return alert("Login zaroori hai!");
            const q = query(collection(db, "bookings"), where("userEmail", "==", auth.currentUser.email));
            const list = document.getElementById("history-list");
            list.innerHTML = "";
            (await getDocs(q)).forEach(doc => {
                let li = document.createElement("li");
                li.innerText = doc.data().destination + " - " + doc.data().date;
                list.appendChild(li);
            });
        };

        let taps = 0;
        document.querySelector('.logo').addEventListener('click', () => {
            if (++taps === 5) {
                if (prompt("Enter Admin Key:") === "5426") alert("Access Granted!");
                taps = 0;
            }
        });
    </script>
</body>
</html>
