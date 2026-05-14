<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <title>SAQIBFITNESS | Elite Training Center</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700;900&family=Inter:wght@300;400;600;800&display=swap');
        
        body { font-family: 'Inter', sans-serif; background: #050505; color: #fff; overflow-x: hidden; }
        .font-hero { font-family: 'Orbitron', sans-serif; }
        
        .hero-gradient {
            background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), url('https://images.unsplash.com/photo-1534438327276-14e5300c3a48?q=80&w=1470&auto=format&fit=crop');
            background-size: cover; background-position: center;
        }
        
        .accent-border { border-left: 4px solid #facc15; }
        .glass { background: rgba(255, 255, 255, 0.03); backdrop-filter: blur(10px); border: 1px solid rgba(255,255,255,0.05); }
        .btn-yellow { background: #facc15; color: #000; transition: all 0.3s ease; }
        .btn-yellow:hover { background: #eab308; transform: translateY(-3px); box-shadow: 0 10px 20px rgba(250, 204, 21, 0.3); }
    </style>
</head>
<body>

    <nav class="fixed w-full z-50 p-6 flex justify-between items-center glass">
        <h1 class="font-hero text-xl font-black tracking-tighter text-yellow-400">SAQIB<span class="text-white">FITNESS</span></h1>
        <div class="hidden md:flex gap-8 text-[10px] font-bold uppercase tracking-widest">
            <a href="#" class="hover:text-yellow-400">Home</a>
            <a href="#plans" class="hover:text-yellow-400">Memberships</a>
            <a href="#contact" class="hover:text-yellow-400">Contact</a>
        </div>
        <button class="btn-yellow px-6 py-2 rounded-full text-[10px] font-black uppercase">Join Now</button>
    </nav>

    <section class="h-screen hero-gradient flex flex-col justify-center px-10">
        <p class="text-yellow-400 font-bold uppercase tracking-[0.5em] mb-4 text-xs">Transform Your Body</p>
        <h2 class="font-hero text-6xl md:text-8xl font-black uppercase leading-none mb-6">Unleash <br> <span class="text-yellow-400">The Beast</span></h2>
        <p class="max-w-md text-slate-400 text-sm mb-10 leading-relaxed">Ladies & Gents Gym with state-of-the-art equipment and professional trainers. Your fitness journey starts here.</p>
        <div class="flex gap-4">
            <button class="btn-yellow px-10 py-4 rounded-xl font-black uppercase text-xs">Start Free Trial</button>
            <button class="border border-white/20 px-10 py-4 rounded-xl font-black uppercase text-xs hover:bg-white/10">View Tour</button>
        </div>
    </section>

    <section class="py-24 px-10 grid md:grid-cols-3 gap-10">
        <div class="glass p-10 rounded-3xl">
            <i class="fa-solid fa-dumbbell text-4xl text-yellow-400 mb-6"></i>
            <h4 class="font-hero text-lg mb-4 uppercase">Modern Gear</h4>
            <p class="text-slate-500 text-sm">Top-notch machines imported for maximum muscle engagement and safety.</p>
        </div>
        <div class="glass p-10 rounded-3xl border-yellow-400/30">
            <i class="fa-solid fa-venus-mars text-4xl text-yellow-400 mb-6"></i>
            <h4 class="font-hero text-lg mb-4 uppercase">Ladies & Gents</h4>
            <p class="text-slate-500 text-sm">Separate timings and dedicated sections for a comfortable environment.</p>
        </div>
        <div class="glass p-10 rounded-3xl">
            <i class="fa-solid fa-person-running text-4xl text-yellow-400 mb-6"></i>
            <h4 class="font-hero text-lg mb-4 uppercase">Expert Coaches</h4>
            <p class="text-slate-500 text-sm">Certified trainers to guide you with diet plans and workout routines.</p>
        </div>
    </section>

    <section id="plans" class="py-24 px-10 bg-[#0a0a0a]">
        <div class="text-center mb-16">
            <h2 class="font-hero text-4xl font-black uppercase">Choose Your <span class="text-yellow-400">Plan</span></h2>
            <div class="h-1 w-20 bg-yellow-400 mx-auto mt-4"></div>
        </div>
        
        <div class="grid md:grid-cols-2 gap-8 max-w-4xl mx-auto">
            <div class="glass p-10 rounded-[2.5rem] relative overflow-hidden">
                <p class="text-[10px] font-black uppercase text-slate-500 mb-2">Monthly</p>
                <h3 class="text-4xl font-black mb-6">₨ 2,500 <span class="text-sm font-normal opacity-50">/mo</span></h3>
                <ul class="space-y-4 text-sm mb-10">
                    <li class="flex items-center gap-3"><i class="fa-solid fa-check text-yellow-400"></i> Full Gym Access</li>
                    <li class="flex items-center gap-3"><i class="fa-solid fa-check text-yellow-400"></i> Locker Room</li>
                    <li class="flex items-center gap-3 opacity-30"><i class="fa-solid fa-xmark"></i> Personal Trainer</li>
                </ul>
                <button class="w-full py-4 border border-white/10 rounded-2xl font-black uppercase text-[10px] hover:bg-white hover:text-black transition-all">Select Plan</button>
            </div>

            <div class="glass p-10 rounded-[2.5rem] border-yellow-400/50 relative overflow-hidden">
                <div class="absolute top-0 right-0 bg-yellow-400 text-black px-6 py-2 text-[10px] font-black uppercase">Best Value</div>
                <p class="text-[10px] font-black uppercase text-yellow-400 mb-2">Quarterly (3 Months)</p>
                <h3 class="text-4xl font-black mb-6">₨ 6,000 <span class="text-sm font-normal opacity-50">/term</span></h3>
                <ul class="space-y-4 text-sm mb-10">
                    <li class="flex items-center gap-3"><i class="fa-solid fa-check text-yellow-400"></i> Full Gym Access</li>
                    <li class="flex items-center gap-3"><i class="fa-solid fa-check text-yellow-400"></i> Diet Consultation</li>
                    <li class="flex items-center gap-3"><i class="fa-solid fa-check text-yellow-400"></i> Free WiFi</li>
                </ul>
                <button class="w-full btn-yellow py-4 rounded-2xl font-black uppercase text-[10px]">Select Plan</button>
            </div>
        </div>
    </section>

    <section class="py-24 px-10 text-center">
        <div class="glass max-w-xl mx-auto p-10 rounded-[3rem]">
            <h3 class="font-hero text-xl mb-6 uppercase">Body Mass Index <span class="text-yellow-400">Calculator</span></h3>
            <div class="flex gap-4 mb-6">
                <input id="weight" type="number" placeholder="Weight (kg)" class="w-1/2 bg-black/40 border border-white/10 p-4 rounded-2xl outline-none">
                <input id="height" type="number" placeholder="Height (cm)" class="w-1/2 bg-black/40 border border-white/10 p-4 rounded-2xl outline-none">
            </div>
            <button onclick="calculateBMI()" class="btn-yellow w-full py-4 rounded-2xl font-black uppercase text-xs mb-4">Calculate My BMI</button>
            <p id="bmi-result" class="text-sm font-bold text-yellow-400 uppercase tracking-widest"></p>
        </div>
    </section>

    <footer id="contact" class="py-10 text-center border-t border-white/5 opacity-50 text-[10px] font-bold uppercase tracking-widest">
        <p>&copy; 2026 SAQIBFITNESS. Developed by High-End Solutions.</p>
    </footer>

    <script>
        function calculateBMI() {
            const w = document.getElementById('weight').value;
            const h = document.getElementById('height').value / 100;
            if(w > 0 && h > 0) {
                const bmi = (w / (h * h)).toFixed(1);
                let msg = "";
                if(bmi < 18.5) msg = "Underweight";
                else if(bmi < 25) msg = "Normal Weight";
                else if(bmi < 30) msg = "Overweight";
                else msg = "Obese";
                document.getElementById('bmi-result').innerText = `Your BMI: ${bmi} (${msg})`;
            }
        }
    </script>
</body>
</html>
