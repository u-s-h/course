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
            <button id="logoTrigger" class="text-2xl font-black text-emerald-700 tracking-wider flex items-center gap-2 cursor-pointer focus:outline-none select-none">
                <i class="fas fa-mountain"></i> DISCOVER <span class="text-slate-900 font-light">GB</span>
            </button>
            <div class="hidden md:flex space-x-8 font-semibold text-sm uppercase tracking-wider text-slate-600">
                <a href="#home" class="hover:text-emerald-600 transition">Home</a>
                <a href="#destinations" class="hover:text-emerald-600 transition">Destinations</a>
                <a href="#quote-system" class="hover:text-emerald-600 transition">Get a Quote</a>
                <a href="#testimonials" class="hover:text-emerald-600 transition">Reviews</a>
                <a href="#contact-form-section" class="hover:text-emerald-600 transition">Inquiry</a>
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

    <section id="destinations" class="py-24 px-6 max-w-7xl mx-auto">
        <div class="text-center max-w-3xl mx-auto mb-16">
            <h2 class="text-3xl md:text-5xl font-black text-slate-900 tracking-tight mb-4">Iconic Landscapes to Explore</h2>
            <div class="w-20 h-1 bg-emerald-600 mx-auto mb-6 rounded-full"></div>
        </div>
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
            <div class="bg-white rounded-2xl shadow-sm hover:shadow-xl transition border border-slate-100 overflow-hidden group">
                <img src="https://images.unsplash.com/photo-1605649487212-47bdab064df7?auto=format&fit=crop&w=600&q=80" alt="Hunza" class="w-full h-48 object-cover group-hover:scale-105 transition duration-300">
                <div class="p-6">
                    <h3 class="text-2xl font-bold text-slate-900 mb-2">Hunza & Nagar</h3>
                    <p class="text-slate-600 font-light text-sm">Famous for its majestic forts (Altit & Baltit), crystal clear Attabad Lake, pristine culture, and breathtaking views of Rakaposhi.</p>
                </div>
            </div>
            <div class="bg-white rounded-2xl shadow-sm hover:shadow-xl transition border border-slate-100 overflow-hidden group">
                <img src="https://images.unsplash.com/photo-1589308078059-be1415eab4c3?auto=format&fit=crop&w=600&q=80" alt="Skardu" class="w-full h-48 object-cover group-hover:scale-105 transition duration-300">
                <div class="p-6">
                    <h3 class="text-2xl font-bold text-slate-900 mb-2">Skardu & Deosai</h3>
                    <p class="text-slate-600 font-light text-sm">Home to Shangrila Resort, Cold Desert, and the world's second-highest plateau, Deosai National Park, filled with vibrant flora.</p>
                </div>
            </div>
            <div class="bg-white rounded-2xl shadow-sm hover:shadow-xl transition border border-slate-100 overflow-hidden group">
                <img src="https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?auto=format&fit=crop&w=600&q=80" alt="Ghizer" class="w-full h-48 object-cover group-hover:scale-105 transition duration-300">
                <div class="p-6">
                    <h3 class="text-2xl font-bold text-slate-900 mb-2">Ghizer & Meadows</h3>
                    <p class="text-slate-600 font-light text-sm">Immerse yourself in the turquoise waters of Phander Lake or trek to the legendary lush pastures at the base of Nanga Parbat.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="quote-system" class="py-20 px-6 bg-slate-900 text-white">
        <div class="max-w-3xl mx-auto bg-slate-800 p-8 rounded-3xl border border-slate-700 shadow-2xl">
            <div class="text-center mb-8">
                <h2 class="text-3xl font-black">Instant Tour Planner</h2>
                <p class="text-slate-400 text-sm mt-2">Select from 20+ majestic destinations across Gilgit-Baltistan.</p>
            </div>
            <form id="quoteForm" class="space-y-6 text-slate-900" onsubmit="return false;">
                <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                    <div>
                        <label class="block text-slate-300 text-sm font-semibold mb-2">Your Name</label>
                        <input type="text" id="userName" required placeholder="Enter full name" class="w-full bg-white px-4 py-3 rounded-xl border-none outline-none">
                    </div>
                    <div>
                        <label class="block text-slate-300 text-sm font-semibold mb-2">Contact Number</label>
                        <input type="tel" id="userPhone" required placeholder="0333XXXXXXX" class="w-full bg-white px-4 py-3 rounded-xl border-none outline-none">
                    </div>
                    <div class="md:col-span-2">
                        <label class="block text-slate-300 text-sm font-semibold mb-2">Select Location</label>
                        <select id="destination" class="w-full bg-white px-4 py-3 rounded-xl outline-none border-none">
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
                        </select>
                    </div>
                    <div>
                        <label class="block text-slate-300 text-sm font-semibold mb-2">Number of Days</label>
                        <select id="days" class="w-full bg-white px-4 py-3 rounded-xl outline-none border-none">
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
                <button type="button" id="submitBtn" class="w-full bg-emerald-500 text-slate-950 py-4 rounded-xl font-black hover:bg-emerald-400 transition cursor-pointer">
                    Submit & Book via WhatsApp
                </button>
            </form>
        </div>
    </section>

    <section id="testimonials" class="py-24 px-6 max-w-7xl mx-auto">
        <div class="text-center max-w-3xl mx-auto mb-16">
            <h2 class="text-3xl md:text-5xl font-black text-slate-900 tracking-tight mb-4">What Travelers Say</h2>
            <div class="w-20 h-1 bg-emerald-600 mx-auto mb-6 rounded-full"></div>
            <p class="text-slate-600 font-light">Feedback from adventurers who explored GB through our community guidelines.</p>
        </div>
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
            <div class="bg-white p-8 rounded-2xl shadow-sm border border-slate-100 flex flex-col justify-between">
                <p class="text-slate-600 font-light italic">"Attabad Lake aur Khunjerab Pass ka tour behtreen raha. Road conditions aur stay guidance bilkul accurate thi."</p>
                <div class="mt-6 flex items-center gap-3 border-t border-slate-100 pt-4">
                    <div class="w-10 h-10 rounded-full bg-emerald-100 text-emerald-700 flex items-center justify-center font-bold">AA</div>
                    <div>
                        <h4 class="font-bold text-slate-900 text-sm">Ali Ahmed</h4>
                        <span class="text-xs text-slate-400">Karachi</span>
                    </div>
                </div>
            </div>
            <div class="bg-white p-8 rounded-2xl shadow-sm border border-slate-100 flex flex-col justify-between">
                <p class="text-slate-600 font-light italic">"Skardu aur Deosai ke liye inhone jo itinerary suggest ki thi us se hamara kafi time aur budget save hua. Highly recommended!"</p>
                <div class="mt-6 flex items-center gap-3 border-t border-slate-100 pt-4">
                    <div class="w-10 h-10 rounded-full bg-emerald-100 text-emerald-700 flex items-center justify-center font-bold">ZK</div>
                    <div>
                        <h4 class="font-bold text-slate-900 text-sm">Zainab Khan</h4>
                        <span class="text-xs text-slate-400">Lahore</span>
                    </div>
                </div>
            </div>
            <div class="bg-white p-8 rounded-2xl shadow-sm border border-slate-100 flex flex-col justify-between">
                <p class="text-slate-600 font-light italic">"Fairy Meadows ki trekking thodi mushkil thi par Discover GB team ki local guidelines ne har step par help ki."</p>
                <div class="mt-6 flex items-center gap-3 border-t border-slate-100 pt-4">
                    <div class="w-10 h-10 rounded-full bg-emerald-100 text-emerald-700 flex items-center justify-center font-bold">UM</div>
                    <div>
                        <h4 class="font-bold text-slate-900 text-sm">Usama Malik</h4>
                        <span class="text-xs text-slate-400">Islamabad</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="contact-form-section" class="py-20 px-6 bg-slate-100 border-t border-b border-slate-200">
        <div class="max-w-xl mx-auto bg-white p-8 rounded-3xl shadow-md border border-slate-200/60">
            <div class="text-center mb-6">
                <h3 class="text-2xl font-bold text-slate-900">Have Any Questions?</h3>
                <p class="text-slate-500 text-sm mt-1">Drop your message below, and our admin team will review it.</p>
            </div>
            <form id="inquiryForm" class="space-y-4">
                <div>
                    <label class="block text-slate-700 text-xs font-bold uppercase mb-1">Your Email</label>
                    <input type="email" id="inqEmail" required placeholder="name@example.com" class="w-full bg-slate-50 border border-slate-300 px-4 py-2.5 rounded-xl text-sm focus:outline-none focus:ring-2 focus:ring-emerald-500 outline-none">
                </div>
                <div>
                    <label class="block text-slate-700 text-xs font-bold uppercase mb-1">Message Topic</label>
                    <input type="text" id="inqSubject" required placeholder="e.g., Hotel Booking, Transport Rates" class="w-full bg-slate-50 border border-slate-300 px-4 py-2.5 rounded-xl text-sm focus:outline-none focus:ring-2 focus:ring-emerald-500 outline-none">
                </div>
                <div>
                    <label class="block text-slate-700 text-xs font-bold uppercase mb-1">Detailed Message</label>
                    <textarea id="inqMessage" rows="4" required placeholder="Write your details here..." class="w-full bg-slate-50 border border-slate-300 px-4 py-2.5 rounded-xl text-sm focus:outline-none focus:ring-2 focus:ring-emerald-500 outline-none"></textarea>
                </div>
                <button type="submit" class="w-full bg-slate-900 text-white py-3 rounded-xl font-bold text-sm hover:bg-slate-800 transition cursor-pointer">
                    Send Secure Message
                </button>
            </form>
        </div>
    </section>

    <div id="adminModal" class="fixed inset-0 bg-slate-950/95 hidden items-center justify-center p-4 z-50 overflow-y-auto">
        <div class="bg-slate-900 border border-slate-800 p-8 rounded-3xl max-w-5xl w-full relative">
            <button id="closeAdminBtn" class="absolute top-4 right-4 text-slate-400 hover:text-white text-xl cursor-pointer"><i class="fas fa-times"></i></button>
            
            <div id="pinGateway" class="text-center space-y-4 py-8">
                <i class="fas fa-user-shield text-5xl text-emerald-500"></i>
                <h3 class="text-2xl font-black text-white">Admin Authentication</h3>
                <input type="password" id="secretKeyField" placeholder="Enter Secret Passcode" class="bg-slate-800 text-white text-center px-4 py-3 rounded-xl border border-slate-700 text-lg w-64 block mx-auto tracking-widest outline-none">
                <button id="verifyPinBtn" class="bg-emerald-500 text-slate-950 px-6 py-2.5 rounded-xl font-bold hover:bg-emerald-400 transition cursor-pointer">Verify Code</button>
            </div>

            <div id="googleGateway" class="text-center space-y-4 hidden py-8">
                <i class="fab fa-google text-5xl text-blue-500"></i>
                <h3 class="text-2xl font-black text-white">Google Identity Verification</h3>
                <p class="text-slate-400 text-xs max-w-sm mx-auto">Accessing live lead streaming pipelines requires an active authentication session.</p>
                <button id="googleSignInBtn" class="bg-white text-slate-900 px-6 py-3 rounded-xl font-bold hover:bg-slate-100 transition inline-flex items-center gap-2 cursor-pointer">
                    <i class="fab fa-google text-red-500"></i> Authenticate with Google
                </button>
            </div>

            <div id="adminDashboard" class="hidden space-y-6">
                <div class="flex justify-between items-center border-b border-slate-800 pb-4">
                    <h3 class="text-2xl font-black text-white"><i class="fas fa-database text-emerald-500"></i> Lead & Message Panel</h3>
                    <button id="logoutBtn" class="bg-rose-600/20 text-rose-400 border border-rose-500/30 px-4 py-2 rounded-lg text-xs font-bold hover:bg-rose-600 hover:text-white transition cursor-pointer">Sign Out</button>
                </div>
                
                <div class="flex gap-4 mb-4">
                    <button id="tabLeads" class="px-4 py-2 rounded-lg text-sm font-bold bg-emerald-600 text-slate-950 cursor-pointer">Tour Quotes</button>
                    <button id="tabMessages" class="px-4 py-2 rounded-lg text-sm font-bold bg-slate-800 text-slate-400 cursor-pointer">General Messages</button>
                </div>

                <div class="overflow-x-auto">
                    <table id="tableLeads" class="w-full text-left border-collapse">
                        <thead>
                            <tr class="text-slate-400 border-b border-slate-800 text-xs uppercase bg-slate-950/40">
                                <th class="p-4">Customer</th>
                                <th class="p-4">Destination</th>
                                <th class="p-4">Duration</th>
                                <th class="p-4">Price</th>
                                <th class="p-4 text-center">Action</th>
                            </tr>
                        </thead>
                        <tbody id="leadsTableBody" class="text-sm divide-y divide-slate-800 text-slate-300"></tbody>
                    </table>

                    <table id="tableMessages" class="w-full text-left border-collapse hidden">
                        <thead>
                            <tr class="text-slate-400 border-b border-slate-800 text-xs uppercase bg-slate-950/40">
                                <th class="p-4">Sender Email</th>
                                <th class="p-4">Topic / Subject</th>
                                <th class="p-4">Detailed Message</th>
                                <th class="p-4">Received Time</th>
                            </tr>
                        </thead>
                        <tbody id="messagesTableBody" class="text-sm divide-y divide-slate-800 text-slate-300"></tbody>
                    </table>
                </div>
            </div>
        </div>
    </div>

    <footer class="bg-slate-950 text-slate-600 py-8 px-6 text-center text-xs border-t border-slate-900">
        <p>&copy; 2026 Discover Gilgit-Baltistan. All rights reserved.</p>
    </footer>

    <script type="module">
        import { initializeApp } from "https://www.gstatic.com/firebasejs/10.8.0/firebase-app.js";
        import { getDatabase, ref, set, push, onValue } from "https://www.gstatic.com/firebasejs/10.8.0/firebase-database.js";
        import { getAuth, signInWithPopup, GoogleAuthProvider, signOut } from "https://www.gstatic.com/firebasejs/10.8.0/firebase-auth.js";

        // Firebase Client Configuration Node
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

        // Target Global Handlers
        const destinationSelect = document.getElementById('destination');
        const daysSelect = document.getElementById('days');
        const totalEstimateDisplay = document.getElementById('totalEstimate');
        const submitBtn = document.getElementById('submitBtn');
        const logoTrigger = document.getElementById('logoTrigger');
        const adminModal = document.getElementById('adminModal');

        // Instant Pricing Realtime Multiplier
        function calculateQuote() {
            const selectedOption = destinationSelect.options[destinationSelect.selectedIndex];
            const basePrice = parseInt(selectedOption.getAttribute('data-price'));
            const daysMultiplier = parseInt(daysSelect.value) / 5;
            const total = Math.round(basePrice * daysMultiplier);
            totalEstimateDisplay.innerText = `PKR ${total.toLocaleString()}`;
        }
        destinationSelect.addEventListener('change', calculateQuote);
        daysSelect.addEventListener('change', calculateQuote);

        // Submit Tour Lead Handler
        submitBtn.addEventListener('click', () => {
            const name = document.getElementById('userName').value.trim();
            const phone = document.getElementById('userPhone').value.trim();
            const dest = destinationSelect.value;
            const duration = daysSelect.value;
            const cost = totalEstimateDisplay.innerText;

            if(!name || !phone) { alert("Please complete name and contact phone fields."); return; }

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
                const text = encodeURIComponent(`Hi Discover GB!\nI generated a custom tour plan query:\n\n👤 Name: ${name}\n📞 Phone: ${phone}\n📍 Destination: ${dest}\n⏱️ Duration: ${duration} Days\n💰 Estimated Price: ${cost}`);
                window.open(`https://wa.me/923332637235?text=${text}`, '_blank');
            }).catch(err => alert("Database Error: " + err.message));
        });

        // Submit General Inquiry Handler
        document.getElementById('inquiryForm').addEventListener('submit', (e) => {
            e.preventDefault();
            const email = document.getElementById('inqEmail').value.trim();
            const subject = document.getElementById('inqSubject').value.trim();
            const msg = document.getElementById('inqMessage').value.trim();

            const msgRef = ref(database, 'messages');
            const newMsgRef = push(msgRef);

            set(newMsgRef, {
                senderEmail: email,
                messageSubject: subject,
                detailedText: msg,
                timestamp: new Date().toLocaleString()
            }).then(() => {
                alert("Your offline message has been dispatched to the admin stream successfully!");
                document.getElementById('inquiryForm').reset();
            }).catch(err => alert("Transmission failure: " + err.message));
        });

        // Easter Egg Detection Matrix (5 Fast Taps)
        let logoTaps = 0;
        let tapTimeout;
        logoTrigger.addEventListener('click', () => {
            logoTaps++;
            clearTimeout(tapTimeout);
            if(logoTaps === 5) {
                logoTaps = 0;
                adminModal.classList.remove('hidden');
                adminModal.classList.add('flex');
            }
            tapTimeout = setTimeout(() => { logoTaps = 0; }, 3000);
        });

        document.getElementById('closeAdminBtn').addEventListener('click', () => {
            adminModal.classList.add('hidden');
            adminModal.classList.remove('flex');
        });

        // Key Validation Layer
        document.getElementById('verifyPinBtn').addEventListener('click', () => {
            if(document.getElementById('secretKeyField').value === "5426") {
                document.getElementById('pinGateway').classList.add('hidden');
                document.getElementById('googleGateway').classList.remove('hidden');
            } else { 
                alert("Access Denied: Invalid Passcode."); 
            }
        });

        // OAuth Sign-In Context Engine
        document.getElementById('googleSignInBtn').addEventListener('click', () => {
            signInWithPopup(auth, provider).then(() => {
                document.getElementById('googleGateway').classList.add('hidden');
                document.getElementById('adminDashboard').classList.remove('hidden');
                loadLiveLeads();
                loadLiveMessages();
            }).catch(err => alert("Security Identity Handshake Failed: " + err.message));
        });

        // Tab Navigation Toggle Matrix
        const tabLeads = document.getElementById('tabLeads');
        const tabMessages = document.getElementById('tabMessages');
        const tableLeads = document.getElementById('tableLeads');
        const tableMessages = document.getElementById('tableMessages');

        tabLeads.addEventListener('click', () => {
            tableLeads.classList.remove('hidden');
            tableMessages.classList.add('hidden');
            tabLeads.className = "px-4 py-2 rounded-lg text-sm font-bold bg-emerald-600 text-slate-950 cursor-pointer";
            tabMessages.className = "px-4 py-2 rounded-lg text-sm font-bold bg-slate-800 text-slate-400 cursor-pointer";
        });

        tabMessages.addEventListener('click', () => {
            tableLeads.classList.add('hidden');
            tableMessages.classList.remove('hidden');
            tabLeads.className = "px-4 py-2 rounded-lg text-sm font-bold bg-slate-800 text-slate-400 cursor-pointer";
            tabMessages.className = "px-4 py-2 rounded-lg text-sm font-bold bg-emerald-600 text-slate-950 cursor-pointer";
        });

        // Live Node Read Sync Functions
        function loadLiveLeads() {
            onValue(ref(database, 'leads'), (snapshot) => {
                const tbody = document.getElementById('leadsTableBody');
                tbody.innerHTML = "";
                const data = snapshot.val();
                if(!data) { tbody.innerHTML = `<tr><td colspan="5" class="p-8 text-center text-slate-500">No quotes requests found.</td></tr>`; return; }
                
                Object.keys(data).reverse().forEach(key => {
                    const rec = data[key];
                    tbody.innerHTML += `<tr class="hover:bg-slate-950/20 border-b border-slate-800/50">
                        <td class="p-4 font-bold text-white">${rec.customerName || 'N/A'}<br><span class="text-xs text-slate-500 font-normal">${rec.customerPhone || 'N/A'}</span></td>
                        <td class="p-4">${rec.selectedDestination || 'N/A'}</td>
                        <td class="p-4 text-slate-400">${rec.tripDurationDays || '5'} Days</td>
                        <td class="p-4 text-emerald-400 font-bold">${rec.calculatedQuotePrice || '0'}</td>
                        <td class="p-4 text-center">
                            <a href="https://wa.me/${(rec.customerPhone || '').replace(/[^0-9]/g, '')}" target="_blank" class="bg-emerald-600/20 text-emerald-400 border border-emerald-500/30 px-3 py-1 rounded text-xs font-bold hover:bg-emerald-600 hover:text-slate-950 transition">Chat</a>
                        </td>
                    </tr>`;
                });
            });
        }

        function loadLiveMessages() {
            onValue(ref(database, 'messages'), (snapshot) => {
                const tbody = document.getElementById('messagesTableBody');
                tbody.innerHTML = "";
                const data = snapshot.val();
                if(!data) { tbody.innerHTML = `<tr><td colspan="4" class="p-8 text-center text-slate-500">No dynamic inquiries found.</td></tr>`; return; }
                
                Object.keys(data).reverse().forEach(key => {
                    const rec = data[key];
                    tbody.innerHTML += `<tr class="hover:bg-slate-950/20 border-b border-slate-800/50">
                        <td class="p-4 text-emerald-400 font-semibold">${rec.senderEmail || 'N/A'}</td>
                        <td class="p-4 font-bold text-white">${rec.messageSubject || 'N/A'}</td>
                        <td class="p-4 text-slate-400 max-w-xs break-words">${rec.detailedText || 'N/A'}</td>
                        <td class="p-4 text-xs text-slate-500">${rec.timestamp || 'Just Now'}</td>
                    </tr>`;
                });
            });
        }

        // Global Session Revocation
        document.getElementById('logoutBtn').addEventListener('click', () => {
            signOut(auth).then(() => {
                document.getElementById('adminDashboard').classList.add('hidden');
                document.getElementById('pinGateway').classList.remove('hidden');
                document.getElementById('secretKeyField').value = "";
                adminModal.classList.add('hidden');
                adminModal.classList.remove('flex');
            });
        });
    </script>
</body>
</html>
