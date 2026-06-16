<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Discover Gilgit-Baltistan | Official Hub</title>
    <script src="https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
</head>
<body class="bg-slate-50 text-slate-800 font-sans tracking-wide">

    <nav class="bg-white/90 backdrop-blur-md shadow-sm sticky top-0 z-50 border-b border-emerald-100">
        <div class="max-w-7xl mx-auto px-6 py-4 flex justify-between items-center">
            <button id="logoTrigger" class="text-2xl font-black text-emerald-700 tracking-wider flex items-center gap-2 cursor-pointer focus:outline-none">
                <i class="fas fa-mountain"></i> DISCOVER <span class="text-slate-900 font-light">GB</span>
            </button>
            <div class="hidden md:flex space-x-8 font-semibold text-sm uppercase tracking-wider text-slate-600">
                <a href="#home" class="hover:text-emerald-600 transition">Home</a>
                <a href="#destinations" class="hover:text-emerald-600 transition">Destinations</a>
                <a href="#quote-system" class="hover:text-emerald-600 transition">Get a Quote</a>
            </div>
            <a href="https://wa.me/923332637235" target="_blank" class="bg-emerald-600 text-white px-5 py-2.5 rounded-full font-bold hover:bg-emerald-700 transition shadow-md flex items-center gap-2 text-sm">
                <i class="fab fa-whatsapp"></i> WHATSAPP
            </a>
        </div>
    </nav>

    <section id="home" class="relative bg-slate-950 text-white py-36 px-6 bg-cover bg-center" style="background-image: linear-gradient(to bottom, rgba(2, 6, 23, 0.85), rgba(6, 78, 59, 0.9)), url('https://images.unsplash.com/photo-1549880338-65ddcdfd017b?auto=format&fit=crop&w=1200&q=80');">
        <div class="max-w-7xl mx-auto text-center md:text-left relative z-10">
            <span class="bg-emerald-500/20 text-emerald-400 px-4 py-1.5 rounded-full text-xs font-bold uppercase tracking-widest border border-emerald-500/30">The Land of Peaks</span>
            <h1 class="text-4xl md:text-6xl font-extrabold mt-4">Explore the Majesty of <span class="text-emerald-400">Gilgit-Baltistan</span></h1>
            <p class="mt-4 text-slate-300 max-w-2xl font-light">Connect with the ultimate guide for your next northern adventure across 20+ hidden gems of GB.</p>
        </div>
    </section>

    <section id="quote-system" class="py-20 px-6 bg-slate-900 text-white">
        <div class="max-w-3xl mx-auto bg-slate-800 p-8 rounded-3xl border border-slate-700 shadow-2xl">
            <div class="text-center mb-8">
                <h2 class="text-3xl font-black">Instant Tour Planner</h2>
                <p class="text-slate-400 text-sm mt-2">Select from 20+ majestic destinations across Gilgit-Baltistan.</p>
            </div>

            <form id="quoteForm" class="space-y-6 text-slate-900">
                <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                    <div>
                        <label class="block text-slate-300 text-sm font-semibold mb-2">Your Name</label>
                        <input type="text" id="userName" required placeholder="Enter full name" class="w-full bg-white px-4 py-3 rounded-xl">
                    </div>
                    <div>
                        <label class="block text-slate-300 text-sm font-semibold mb-2">Contact Number</label>
                        <input type="tel" id="userPhone" required placeholder="0333XXXXXXX" class="w-full bg-white px-4 py-3 rounded-xl">
                    </div>
                    <div class="md:col-span-2">
                        <label class="block text-slate-300 text-sm font-semibold mb-2">Select Location</label>
                        <select id="destination" class="w-full bg-white px-4 py-3 rounded-xl">
                            <optgroup label="Gilgit & Surrounding">
                                <option value="Gilgit City" data-price="35000">Gilgit City</option>
                                <option value="Naltar Valley" data-price="45000">Naltar Valley (Lakes & Ski Resort)</option>
                                <option value="Kargah Buddha" data-price="32000">Kargah Buddha</option>
                                <option value="Bagrot Valley" data-price="38000">Bagrot Valley</option>
                            </optgroup>
                            <optgroup label="Hunza & Nagar">
                                <option value="Karimabad (Hunza)" data-price="48000">Karimabad & Forts</option>
                                <option value="Attabad Lake" data-price="50000">Attabad Lake & Passu Cones</option>
                                <option value="Khunjerab Pass" data-price="55000">Khunjerab Pass (China Border)</option>
                                <option value="Shimshal Valley" data-price="65000">Shimshal Valley (Remote GB)</option>
                                <option value="Hopper Glacier (Nagar)" data-price="46000">Hopper Glacier</option>
                                <option value="Minapin (Rakaposhi Base)" data-price="42000">Minapin Valley</option>
                            </optgroup>
                            <optgroup label="Baltistan Division">
                                <option value="Skardu Town" data-price="50000">Skardu Town & Lakes</option>
                                <option value="Deosai National Park" data-price="60000">Deosai (Land of Giants)</option>
                                <option value="Shigar Valley" data-price="52000">Shigar Valley (Cold Desert)</option>
                                <option value="Khaplu Valley" data-price="55000">Khaplu Palace & Chaqchan Mosque</option>
                                <option value="Basho Valley" data-price="58000">Basho Meadow & Meadows</option>
                                <option value="Kachura Lakes" data-price="48000">Shangrila & Upper Kachura Lake</option>
                            </optgroup>
                            <optgroup label="Diamer & Astore">
                                <option value="Fairy Meadows" data-price="55000">Fairy Meadows & Nanga Parbat Base</option>
                                <option value="Chilas" data-price="35000">Chilas Archeological Sites</option>
                                <option value="Rama Meadow (Astore)" data-price="48000">Rama Meadow & Lake</option>
                                <option value="Tarashing (Nanga Parbat)" data-price="50000">Tarashing Village</option>
                            </optgroup>
                            <optgroup label="Ghizer & Ghangche">
                                <option value="Phander Lake (Ghizer)" data-price="52000">Phander Lake (Gupis)</option>
                                <option value="Ishkoman Valley" data-price="48000">Ishkoman Valley</option>
                            </optgroup>
                        </select>
                    </div>
                    <div>
                        <label class="block text-slate-300 text-sm font-semibold mb-2">Number of Days</label>
                        <select id="days" class="w-full bg-white px-4 py-3 rounded-xl">
                            <option value="5">5 Days Trip</option>
                            <option value="7">7 Days Trip</option>
                            <option value="10">10 Days Trip</option>
                        </select>
                    </div>
                </div>

                <div class="bg-slate-950 p-6 rounded-2xl border border-slate-700 text-center">
                    <span class="text-slate-400 text-xs block">Estimated Price</span>
                    <span id="totalEstimate" class="text-3xl font-black text-emerald-400 mt-1 block">PKR 35,000</span>
                </div>

                <button type="button" id="submitBtn" class="w-full bg-emerald-500 text-slate-950 py-4 rounded-xl font-black hover:bg-emerald-400 transition">
                    Submit & Book via WhatsApp
                </button>
            </form>
        </div>
    </section>

    <div id="adminModal" class="fixed inset-0 bg-slate-950/95 hidden items-center justify-center p-4 z-50 overflow-y-auto">
        <div class="bg-slate-900 border border-slate-800 p-8 rounded-3xl max-w-4xl w-full relative">
            <button onclick="closeAdminPanel()" class="absolute top-4 right-4 text-slate-400 hover:text-white text-xl"><i class="fas fa-times"></i></button>
            
            <div id="pinGateway" class="text-center space-y-4">
                <i class="fas fa-user-shield text-5xl text-emerald-500"></i>
                <h3 class="text-2xl font-black text-white">Admin Authentication</h3>
                <input type="password" id="secretKeyField" placeholder="Enter Secret Passcode" class="bg-slate-800 text-white text-center px-4 py-3 rounded-xl border border-slate-700 text-lg w-64 block mx-auto tracking-widest">
                <button onclick="verifySecretKey()" class="bg-emerald-500 text-slate-950 px-6 py-2.5 rounded-xl font-bold hover:bg-emerald-400 transition">Verify Code</button>
            </div>

            <div id="googleGateway" class="text-center space-y-4 hidden">
                <i class="fab fa-google text-5xl text-blue-500"></i>
                <h3 class="text-2xl font-black text-white">Google Identity Verification</h3>
                <p class="text-slate-400 text-sm">Security layer require Google account verification to stream live database nodes.</p>
                <button id="googleSignInBtn" class="bg-white text-slate-900 px-6 py-3 rounded-xl font-bold hover:bg-slate-100 transition inline-flex items-center gap-2 shadow-lg">
                    <i class="fab fa-google text-red-500"></i> Authenticate with Google
                </button>
            </div>

            <div id="adminDashboard" class="hidden space-y-6">
                <div class="flex justify-between items-center border-b border-slate-800 pb-4">
                    <h3 class="text-2xl font-black text-white flex items-center gap-2"><i class="fas fa-database text-emerald-500"></i> Active Lead Inquiries</h3>
                    <button id="logoutBtn" class="bg-rose-600/20 text-rose-400 border border-rose-500/30 px-4 py-2 rounded-lg text-xs font-bold hover:bg-rose-600 hover:text-white transition">Sign Out</button>
                </div>
                <div class="overflow-x-auto">
                    <table class="w-full text-left border-collapse">
                        <thead>
                            <tr class="text-slate-400 border-b border-slate-800 text-xs uppercase bg-slate-950/40">
                                <th class="p-4">Customer Details</th>
                                <th class="p-4">Target Destination</th>
                                <th class="p-4">Duration</th>
                                <th class="p-4">Price Quoted</th>
                                <th class="p-4 text-center">Action</th>
                            </tr>
                        </thead>
                        <tbody id="leadsTableBody" class="text-sm divide-y divide-slate-800 text-slate-300">
                            </tbody>
                    </table>
                </div>
            </div>
        </div>
    </div>

    <script type="module">
        import { initializeApp } from "https://www.gstatic.com/firebasejs/10.8.0/firebase-app.js";
        import { getDatabase, ref, set, push, onValue } from "https://www.gstatic.com/firebasejs/10.8.0/firebase-database.js";
        import { getAuth, signInWithPopup, GoogleAuthProvider, signOut } from "https://www.gstatic.com/firebasejs/10.8.0/firebase-auth.js";

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
        const database = getDatabase(app);
        const auth = getAuth(app);
        const provider = new GoogleAuthProvider();

        // UI Target Hooks
        const destinationSelect = document.getElementById('destination');
        const daysSelect = document.getElementById('days');
        const totalEstimateDisplay = document.getElementById('totalEstimate');
        const submitBtn = document.getElementById('submitBtn');
        const logoTrigger = document.getElementById('logoTrigger');

        // Calculator Pricing Engine
        function calculateQuote() {
            const selectedOption = destinationSelect.options[destinationSelect.selectedIndex];
            const basePrice = parseInt(selectedOption.getAttribute('data-price'));
            const daysMultiplier = parseInt(daysSelect.value) / 5;
            const total = Math.round(basePrice * daysMultiplier);
            totalEstimateDisplay.innerText = `PKR ${total.toLocaleString()}`;
        }
        destinationSelect.addEventListener('change', calculateQuote);
        daysSelect.addEventListener('change', calculateQuote);

        // Submit Data to RTDB
        submitBtn.addEventListener('click', () => {
            const name = document.getElementById('userName').value.trim();
            const phone = document.getElementById('userPhone').value.trim();
            const dest = destinationSelect.value;
            const duration = daysSelect.value;
            const cost = totalEstimateDisplay.innerText;

            if(!name || !phone) { alert("Fields Required!"); return; }

            const quotesRef = ref(database, 'leads');
            const newQuoteRef = push(quotesRef);

            set(newQuoteRef, {
                customerName: name,
                customerPhone: phone,
                selectedDestination: dest,
                tripDurationDays: duration,
                calculatedQuotePrice: cost,
                timestamp: new Date().toLocaleString()
            }).then(() => {
                const text = encodeURIComponent(`Hi Discover GB!\nI generated a package quote:\nName: ${name}\nPhone: ${phone}\nDestination: ${dest}\nDays: ${duration}\nPrice: ${cost}`);
                window.open(`https://wa.me/923332637235?text=${text}`, '_blank');
            });
        });

        // Secret Easter Egg Trigger Setup (5 Taps)
        let logoTaps = 0;
        logoTrigger.addEventListener('click', () => {
            logoTaps++;
            if(logoTaps === 5) {
                logoTaps = 0;
                document.getElementById('adminModal').classList.remove('hidden');
                document.getElementById('adminModal').classList.add('flex');
            }
            setTimeout(() => { if(logoTaps > 0) logoTaps = 0; }, 3000); // reset if slow
        });

        window.closeAdminPanel = function() {
            document.getElementById('adminModal').classList.add('hidden');
            document.getElementById('adminModal').classList.remove('flex');
        };

        // Pin Key Validation
        window.verifySecretKey = function() {
            const pinInput = document.getElementById('secretKeyField').value;
            if(pinInput === "5426") {
                document.getElementById('pinGateway').classList.add('hidden');
                document.getElementById('googleGateway').classList.remove('hidden');
            } else {
                alert("Incorrect Pin Key!");
            }
        };

        // Google Authentication Logic
        document.getElementById('googleSignInBtn').addEventListener('click', () => {
            signInWithPopup(auth, provider).then((result) => {
                document.getElementById('googleGateway').classList.add('hidden');
                document.getElementById('adminDashboard').classList.remove('hidden');
                loadLiveLeads();
            }).catch((err) => alert("Auth Failed: " + err.message));
        });

        // Stream Records from DB to Table UI
        function loadLiveLeads() {
            const leadsRef = ref(database, 'leads');
            onValue(leadsRef, (snapshot) => {
                const tableBody = document.getElementById('leadsTableBody');
                tableBody.innerHTML = "";
                const data = snapshot.val();
                
                if(!data) {
                    tableBody.innerHTML = `<tr><td colspan="5" class="p-8 text-center text-slate-500">No active leads in database node.</td></tr>`;
                    return;
                }

                Object.keys(data).reverse().forEach(key => {
                    const record = data[key];
                    const row = `
                        <tr class="hover:bg-slate-950/20">
                            <td class="p-4 font-bold text-white">${record.customerName}<br><span class="text-xs text-slate-500">${record.customerPhone}</span></td>
                            <td class="p-4">${record.selectedDestination}</td>
                            <td class="p-4 text-slate-400">${record.tripDurationDays} Days</td>
                            <td class="p-4 text-emerald-400 font-bold">${record.calculatedQuotePrice}</td>
                            <td class="p-4 text-center">
                                <a href="https://wa.me/${record.customerPhone.replace(/[^0-9]/g, '')}" target="_blank" class="bg-emerald-600/20 text-emerald-400 border border-emerald-500/30 px-3 py-1.5 rounded-lg text-xs hover:bg-emerald-600 hover:text-white transition">
                                    <i class="fab fa-whatsapp"></i> Chat
                                </a>
                            </td>
                        </tr>
                    `;
                    tableBody.innerHTML += row;
                });
            });
        }

        // Logout Flow
        document.getElementById('logoutBtn').addEventListener('click', () => {
            signOut(auth).then(() => {
                document.getElementById('adminDashboard').classList.add('hidden');
                document.getElementById('pinGateway').classList.remove('hidden');
                document.getElementById('secretKeyField').value = "";
                closeAdminPanel();
            });
        });
    </script>
</body>
</html>
