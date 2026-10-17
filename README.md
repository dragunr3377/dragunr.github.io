🛍️ DRAGUN R
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Burj Khalifa Live Flag Animation - Dragun</title>
    <style>
        body, html {
            margin: 0;
            padding: 0;
            width: 100%;
            height: 100%;
            overflow: hidden;
            background-color: #050b14;
            font-family: Arial, sans-serif;
        }

        .scene {
            position: relative;
            width: 100vw;
            height: 100vh;
            background: linear-gradient(to bottom, #020408, #0c1b33, #1e3a60);
        }

        /* Burj Khalifa Building Structure */
        .burj-khalifa {
            position: absolute;
            bottom: 0;
            left: 30%;
            width: 250px;
            height: 90vh;
            background: linear-gradient(90deg, #111d2d, #1f334d, #0d1622);
            border-top-left-radius: 20px;
            border-top-right-radius: 20px;
            box-shadow: inset 0 0 20px rgba(255, 255, 255, 0.1);
        }

        /* Building Lights / Facade Text Effect */
        .building-text {
            position: absolute;
            top: 40%;
            left: 50%;
            transform: translate(-50%, -50%) rotate(-90deg);
            color: #ff9900;
            font-size: 36px;
            font-weight: bold;
            letter-spacing: 5px;
            text-shadow: 0 0 15px #ff7700, 0 0 30px #ff5500;
        }

        /* Spire / Top of Burj Khalifa */
        .spire {
            position: absolute;
            bottom: 90vh;
            left: calc(30% + 115px);
            width: 20px;
            height: 100px;
            background: #silver;
            background: linear-gradient(to top, #333, #fff);
        }

        /* Boy standing at the top */
        .boy {
            position: absolute;
            bottom: calc(90vh + 40px);
            left: calc(30% + 118px);
            width: 15px;
            height: 40px;
            background: #000;
            border-radius: 5px;
        }

        /* Flag Pole */
        .flag-pole {
            position: absolute;
            bottom: calc(90vh + 40px);
            left: calc(30% + 128px);
            width: 4px;
            height: 120px;
            background: #ddd;
        }

        /* Live Waving Flag */
        .flag {
            position: absolute;
            bottom: calc(90vh + 110px);
            left: calc(30% + 132px);
            width: 140px;
            height: 90px;
            background: #0b131f;
            border: 2px solid #ff7700;
            border-radius: 4px;
            transform-origin: left center;
            animation: wave 1.5s ease-in-out infinite alternate;
            display: flex;
            align-items: center;
            justify-content: center;
            flex-direction: column;
            box-shadow: 0 0 10px rgba(255, 119, 0, 0.5);
        }

        .flag-content {
            color: #fff;
            text-align: center;
            font-size: 14px;
            font-weight: bold;
        }

        .flag-content span {
            color: #ff7700;
            display: block;
            font-size: 10px;
        }

        @keyframes wave {
            0% {
                transform: rotateX(0deg) rotateY(0deg) skewY(0deg);
            }
            100% {
                transform: rotateX(15deg) rotateY(-25deg) skewY(-5deg);
            }
        }
    </style>
</head>
<body>

    <div class="scene">
        <!-- Burj Khalifa Building -->
        <div class="burj-khalifa">
            <div class="building-text">DRAGUN</div>
        </div>
        
        <!-- Spire -->
        <div class="spire"></div>

        <!-- Boy -->
        <div class="boy"></div>

        <!-- Flag Pole -->
        <div class="flag-pole"></div>

        <!-- Live Waving Flag with Dragun Branding -->
        <div class="flag">
            <div class="flag-content">
                🐉 DRAGUN
                <span>COMPANY</span>
            </div>
        </div>
    </div>

</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dragun Luxury Watch - Exclusive Offer</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: #0f172a;
            color: #f8fafc;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            padding: 20px;
        }

        .product-container {
            display: flex;
            flex-wrap: wrap;
            background: #1e293b;
            border-radius: 16px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
            max-width: 900px;
            width: 100%;
            overflow: hidden;
            border: 1px solid #334155;
        }

        .product-image {
            flex: 1;
            min-width: 300px;
            background: #0f172a;
            display: flex;
            justify-content: center;
            align-items: center;
            position: relative;
            padding: 40px;
        }

        /* Live Watch Graphic / Animation */
        .watch-mockup {
            width: 220px;
            height: 220px;
            border: 8px solid #cbd5e1;
            border-radius: 50%;
            position: relative;
            background: #000;
            box-shadow: inset 0 0 15px rgba(255,255,255,0.2), 0 5px 15px rgba(0,0,0,0.5);
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .watch-center {
            width: 12px;
            height: 12px;
            background: #e2e8f0;
            border-radius: 50%;
            position: absolute;
            z-index: 10;
        }

        .hand {
            position: absolute;
            bottom: 50%;
            left: 50%;
            transform-origin: bottom;
            border-radius: 4px;
        }

        .hour-hand {
            width: 4px;
            height: 55px;
            background: #e2e8f0;
            transform: translateX(-50%) rotate(0deg);
        }

        .minute-hand {
            width: 3px;
            height: 75px;
            background: #94a3b8;
            transform: translateX(-50%) rotate(0deg);
        }

        .second-hand {
            width: 2px;
            height: 85px;
            background: #ef4444;
            transform: translateX(-50%) rotate(0deg);
        }

        .product-details {
            flex: 1;
            min-width: 300px;
            padding: 40px;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }

        .brand-title {
            font-size: 14px;
            letter-spacing: 2px;
            color: #38bdf8;
            font-weight: 600;
            text-transform: uppercase;
            margin-bottom: 8px;
        }

        .product-title {
            font-size: 28px;
            font-weight: 700;
            margin-bottom: 15px;
        }

        .price-tag {
            font-size: 32px;
            font-weight: 700;
            color: #22c55e;
            margin-bottom: 20px;
        }

        .price-tag span {
            font-size: 16px;
            color: #94a3b8;
            text-decoration: line-through;
            margin-left: 10px;
        }

        .description {
            font-size: 14px;
            color: #94a3b8;
            line-height: 1.6;
            margin-bottom: 20px;
        }

        .timer-box {
            background: #0f172a;
            padding: 12px;
            border-radius: 8px;
            text-align: center;
            margin-bottom: 25px;
            border: 1px solid #334155;
        }

        .timer-box p {
            font-size: 12px;
            color: #cbd5e1;
            margin-bottom: 4px;
        }

        #countdown {
            font-size: 18px;
            font-weight: 700;
            color: #f59e0b;
        }

        .buy-btn {
            background: #2563eb;
            color: white;
            border: none;
            padding: 15px;
            font-size: 16px;
            font-weight: 600;
            border-radius: 8px;
            cursor: pointer;
            transition: background 0.3s ease;
            width: 100%;
            text-align: center;
            text-decoration: none;
            display: inline-block;
        }

        .buy-btn:hover {
            background: #1d4ed8;
        }
    </style>
</head>
<body>

    <div class="product-container">
        <!-- Live Animated Watch Section -->
        <div class="product-image">
            <div class="watch-mockup">
                <div class="watch-center"></div>
                <div class="hand hour-hand" id="hourHand"></div>
                <div class="hand minute-hand" id="minuteHand"></div>
                <div class="hand second-hand" id="secondHand"></div>
            </div>
        </div>

        <!-- Product Details Section -->
        <div class="product-details">
            <div>
                <div class="brand-title">Dragun Official</div>
                <h1 class="product-title">Dragun Chrono Master</h1>
                <div class="price-tag">$199 USD <span>$350 USD</span></div>
                <p class="description">
                    Experience precision timekeeping with the Dragun Chrono Master. Built with aerospace-grade steel, scratch-resistant sapphire glass, and a live smooth-sweep movement mechanism.
                </p>

                <!-- Timer -->
                <div class="timer-box">
                    <p>Limited Time Offer Ends In:</p>
                    <div id="countdown">05:12:45</div>
                </div>
            </div>

            <!-- Buy Button -->
            <a href="#" class="buy-btn" onclick="alert('Redirecting to checkout for $199 USD...')">Buy Now - $199</a>
        </div>
    </div>

    <script>
        // Live Watch Hands Movement Script
        function updateClock() {
            const now = new Date();
            const seconds = now.getSeconds();
            const minutes = now.getMinutes();
            const hours = now.getHours();

            const secondDegrees = (seconds / 60) * 360;
            const minuteDegrees = ((minutes + seconds / 60) / 60) * 360;
            const hourDegrees = ((hours % 12 + minutes / 60) / 12) * 360;

            document.getElementById('secondHand').style.transform = `translateX(-50%) rotate(${secondDegrees}deg)`;
            document.getElementById('minuteHand').style.transform = `translateX(-50%) rotate(${minuteDegrees}deg)`;
            document.getElementById('hourHand').style.transform = `translateX(-50%) rotate(${hourDegrees}deg)`;
        }

        setInterval(updateClock, 1000);
        updateClock();

        // Countdown Timer Script
        let timeRemaining = 5 * 3600 + 12 * 60 + 45; // 5 hours 12 mins 45 secs
        const countdownElement = document.getElementById('countdown');

        setInterval(() => {
            if (timeRemaining > 0) {
                timeRemaining--;
                let hrs = Math.floor(timeRemaining / 3600);
                let mins = Math.floor((timeRemaining % 3600) / 60);
                let secs = timeRemaining % 60;

                countdownElement.textContent = 
                    `${hrs.toString().padStart(2, '0')}:${mins.toString().padStart(2, '0')}:${secs.toString().padStart(2, '0')}`;
            }
        }, 1000);
    </script>

</body>
</html>



<!DOCTYPE html>
<!DOCTYPE html>
<html lang="hi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>DRAGUN Official Advertisement</title>
<style>
* { box-sizing: border-box; }
body {
  margin: 0;
  font-family: Arial, sans-serif;
  background: #101827;
  color: white;
  text-align: center;
}
.video {
  max-width: 850px;
  min-height: 570px;
  margin: 20px auto;
  padding: 25px;
  border-radius: 20px;
  background: linear-gradient(135deg,#132a45,#087e8b);
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  overflow: hidden;
}
.logo {
  color: #ffdc46;
  font-size: clamp(38px,8vw,65px);
  font-weight: 900;
  letter-spacing: 7px;
  text-shadow: 3px 3px #111;
}
.tagline { font-size: 20px; }
.scene {
  font-size: 100px;
  margin: 15px;
  animation: float 2s infinite ease-in-out;
}
@keyframes float {
  0%,100% { transform: translateY(0); }
  50% { transform: translateY(-12px); }
}
h1 { font-size: clamp(25px,5vw,40px); }
#dialogue {
  font-size: 21px;
  line-height: 1.6;
  max-width: 650px;
  min-height: 95px;
}
button {
  background: #ffdc46;
  color: #111;
  border: 0;
  padding: 13px 24px;
  margin: 7px;
  font-size: 16px;
  font-weight: bold;
  border-radius: 30px;
  cursor: pointer;
}
button:hover { background: white; }
.controls { padding-bottom: 25px; }
.small { color: #d8e5f0; font-size: 14px; }
</style>
</head>
<body>

<div class="video">
  <div class="logo">DRAGUN</div>
  <div class="tagline">STYLE • QUALITY • PROTECTION</div>

  <div class="scene" id="product">👜</div>
  <h1 id="heading">Welcome to DRAGUN!</h1>
  <p id="dialogue">
    Namaskar dosto! DRAGUN lekar aaya hai
    aapke liye style aur quality ka zabardast collection!
  </p>
  <p class="small" id="counter">Scene 1 / 4</p>
</div>

<div class="controls">
  <button onclick="previous()">⬅ Pichla Scene</button>
  <button onclick="speak()">🔊 Hindi Voice</button>
  <button onclick="next()">Agla Scene ➡</button>
  <button onclick="toggleAuto()" id="autoBtn">▶ Auto Play</button>
</div>

<script>
const scenes = [
  {
    icon: "👜",
    title: "Welcome to DRAGUN!",
    text: "Namaskar dosto! DRAGUN lekar aaya hai aapke liye style aur quality ka zabardast collection!"
  },
  {
    icon: "🎒",
    title: "DRAGUN Stylish Bags",
    text: "Chahe school ho, office ho ya travel, DRAGUN bags ke saath paaiye stylish look aur apna samaan rakhne ki suvidha!"
  },
  {
    icon: "🧢",
    title: "DRAGUN Fashion Caps",
    text: "Apne style ko banaiye aur bhi khaas! DRAGUN caps ke saath paaiye ek smart aur trendy look!"
  },
  {
    icon: "🌧️",
    title: "DRAGUN Raincoats",
    text: "Baarish ho ya kharab mausam, DRAGUN raincoat ke saath taiyar rahiye! DRAGUN — style, quality aur protection, sab ek saath!"
  }
];

let index = 0;
let timer = null;

function showScene() {
  const s = scenes[index];
  document.getElementById("product").textContent = s.icon;
  document.getElementById("heading").textContent = s.title;
  document.getElementById("dialogue").textContent = s.text;
  document.getElementById("counter").textContent =
    `Scene ${index + 1} / ${scenes.length}`;
}

function next() {
  index = (index + 1) % scenes.length;
  showScene();
}

function previous() {
  index = (index - 1 + scenes.length) % scenes.length;
  showScene();
}

function speak() {
  if (!("speechSynthesis" in window)) {
    alert("Is browser mein voice support nahi hai.");
    return;
  }
  speechSynthesis.cancel();
  const utterance = new SpeechSynthesisUtterance(
    scenes[index].text
  );
  utterance.lang = "hi-IN";
  utterance.rate = 0.9;
  utterance.pitch = 1.1;
  speechSynthesis.speak(utterance);
}

function toggleAuto() {
  if (timer) {
    clearInterval(timer);
    timer = null;
    document.getElementById("autoBtn").textContent =
      "▶ Auto Play";
  } else {
    timer = setInterval(next, 6000);
    document.getElementById("autoBtn").textContent =
      "⏸ Stop Auto Play";
  }
}

showScene();
</script>
</body>
</html>
<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dragun Company - Adventure Gear Store</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- FontAwesome for Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts Inter -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                    },
                    colors: {
                        dragun: {
                            50: '#fff7ed',
                            100: '#ffedd5',
                            500: '#f97316',
                            600: '#ea580c',
                            700: '#c2410c',
                            900: '#7c2d12',
                        }
                    }
                }
            }
        }
    </script>
</head>
<body class="bg-slate-950 text-slate-100 font-sans antialiased selection:bg-dragun-500 selection:text-white">

    <!-- Navigation Header -->
    <header class="sticky top-0 z-50 backdrop-blur-md bg-slate-950/80 border-b border-slate-800 transition-all duration-300">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-20 flex items-center justify-between">
            <div class="flex items-center gap-3">
                <div class="w-10 h-10 rounded-xl bg-gradient-to-tr from-dragun-600 to-amber-500 flex items-center justify-center shadow-lg shadow-dragun-600/30">
                    <i class="fa-solid fa-dragon text-white text-xl"></i>
                </div>
                <span class="text-2xl font-extrabold tracking-wider bg-gradient-to-r from-white via-slate-200 to-dragun-500 bg-clip-text text-transparent">
                    DRAGUN <span class="text-dragun-500 text-sm font-semibold uppercase tracking-widest block -mt-1">Company</span>
                </span>
            </div>

            <!-- Desktop Nav Links -->
            <nav class="hidden md:flex items-center gap-8 font-medium text-sm text-slate-300">
                <a href="#home" class="hover:text-dragun-500 transition-colors">Home</a>
                <a href="#products" class="hover:text-dragun-500 transition-colors">Products</a>
                <a href="#about" class="hover:text-dragun-500 transition-colors">About Us</a>
                <a href="#contact" class="hover:text-dragun-500 transition-colors">Contact</a>
            </nav>

            <!-- Actions -->
            <div class="flex items-center gap-4">
                <button id="cart-btn" class="relative p-2.5 rounded-xl bg-slate-900 border border-slate-800 hover:border-dragun-500/50 hover:bg-slate-800 transition-all text-slate-200" aria-label="Shopping Cart">
                    <i class="fa-solid fa-bag-shopping text-lg"></i>
                    <span id="cart-counter" class="absolute -top-1.5 -right-1.5 bg-dragun-600 text-white text-xs font-bold w-5 h-5 rounded-full flex items-center justify-center shadow-md scale-100 transition-transform">0</span>
                </button>
                <button id="mobile-menu-btn" class="md:hidden p-2.5 rounded-xl bg-slate-900 border border-slate-800 text-slate-300 hover:text-white">
                    <i class="fa-solid fa-bars text-lg"></i>
                </button>
            </div>
        </div>

        <!-- Mobile Menu -->
        <div id="mobile-menu" class="hidden md:hidden border-t border-slate-800 bg-slate-900/95 backdrop-blur-lg px-4 pt-4 pb-6 space-y-3">
            <a href="#home" class="block py-2 text-slate-300 hover:text-dragun-500 font-medium">Home</a>
            <a href="#products" class="block py-2 text-slate-300 hover:text-dragun-500 font-medium">Products</a>
            <a href="#about" class="block py-2 text-slate-300 hover:text-dragun-500 font-medium">About Us</a>
            <a href="#contact" class="block py-2 text-slate-300 hover:text-dragun-500 font-medium">Contact</a>
        </div>
    </header>

    <!-- Hero Section -->
    <section id="home" class="relative overflow-hidden pt-12 pb-24 lg:pt-20 lg:pb-32 border-b border-slate-900">
        <div class="absolute inset-0 bg-[radial-gradient(ellipse_80%_80%_at_50%_-20%,rgba(249,115,22,0.15),rgba(255,255,255,0))]"></div>
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
            <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 items-center">
                <div class="lg:col-span-7 space-y-6 text-center lg:text-left">
                    <div class="inline-flex items-center gap-2 px-3.5 py-1.5 rounded-full bg-dragun-500/10 border border-dragun-500/20 text-dragun-400 text-xs font-semibold tracking-wider uppercase">
                        <i class="fa-solid fa-fire text-amber-500"></i> Engineered For Extreme Adventure
                    </div>
                    <h1 class="text-4xl sm:text-6xl lg:text-7xl font-extrabold tracking-tight leading-none text-white">
                        Conquer Every <span class="bg-gradient-to-r from-dragun-500 to-amber-400 bg-clip-text text-transparent">Element</span>
                    </h1>
                    <p class="text-slate-400 text-lg sm:text-xl max-w-2xl mx-auto lg:mx-0 font-normal leading-relaxed">
                        Discover ultra-durable backpacks, waterproof tactical caps, and all-weather raincoats designed for the modern explorer. Built tough, styled sharp.
                    </p>
                    <div class="flex flex-col sm:flex-row items-center justify-center lg:justify-start gap-4 pt-4">
                        <a href="#products" class="w-full sm:w-auto px-8 py-4 rounded-xl bg-gradient-to-r from-dragun-600 to-amber-600 hover:from-dragun-500 hover:to-amber-500 text-white font-semibold text-base shadow-lg shadow-dragun-600/30 transition-all flex items-center justify-center gap-2 group">
                            Shop Now <i class="fa-solid fa-arrow-right group-hover:translate-x-1 transition-transform"></i>
                        </a>
                        <a href="#about" class="w-full sm:w-auto px-8 py-4 rounded-xl bg-slate-900 border border-slate-800 hover:border-slate-700 text-slate-300 hover:text-white font-semibold text-base transition-all text-center">
                            Learn Our Story
                        </a>
                    </div>
                    <!-- Stats -->
                    <div class="grid grid-cols-3 gap-6 pt-8 border-t border-slate-900 max-w-lg mx-auto lg:mx-0">
                        <div>
                            <div class="text-2xl sm:text-3xl font-extrabold text-white">100%</div>
                            <div class="text-xs text-slate-400 mt-1">Waterproof Gear</div>
                        </div>
                        <div>
                            <div class="text-2xl sm:text-3xl font-extrabold text-white">50k+</div>
                            <div class="text-xs text-slate-400 mt-1">Explorers Equipped</div>
                        </div>
                        <div>
                            <div class="text-2xl sm:text-3xl font-extrabold text-white">5-Yr</div>
                            <div class="text-xs text-slate-400 mt-1">Warranty</div>
                        </div>
                    </div>
                </div>
                <div class="lg:col-span-5 relative">
                    <div class="relative mx-auto max-w-md lg:max-w-none">
                        <div class="absolute -inset-1 rounded-3xl bg-gradient-to-r from-dragun-600 to-amber-500 opacity-30 blur-xl"></div>
                        <div class="relative rounded-2xl overflow-hidden border border-slate-800 bg-slate-900 shadow-2xl">
                            <img src="https://images.unsplash.com/photo-1546938576-6e6a64f317cc?q=80&w=800&auto=format&fit=crop" onerror="this.src='https://placehold.co/600x700/0f172a/f97316?text=Dragun+Gear'" alt="Hero Gear" class="w-full h-[450px] object-cover hover:scale-105 transition-transform duration-700">
                            <div class="absolute inset-0 bg-gradient-to-t from-slate-950 via-slate-950/20 to-transparent"></div>
                            <div class="absolute bottom-6 left-6 right-6 p-4 rounded-xl bg-slate-900/90 backdrop-blur-md border border-slate-800 flex items-center justify-between">
                                <div>
                                    <span class="text-xs font-semibold text-dragun-400 uppercase tracking-wider">Featured Release</span>
                                    <h4 class="text-lg font-bold text-white">Apex Storm Backpack</h4>
                                </div>
                                <span class="px-3 py-1.5 rounded-lg bg-dragun-600 text-white text-sm font-bold">$129.99</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Products Section -->
    <section id="products" class="py-20 bg-slate-900/50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex flex-col md:flex-row md:items-end justify-between mb-12">
                <div>
                    <span class="text-dragun-500 text-sm font-bold uppercase tracking-wider">Our Collection</span>
                    <h2 class="text-3xl sm:text-4xl font-extrabold text-white mt-2">Engineered For The Wild</h2>
                </div>
                <!-- Category Tabs -->
                <div class="flex flex-wrap gap-2 mt-6 md:mt-0 bg-slate-900 p-1.5 rounded-xl border border-slate-800">
                    <button class="category-btn px-5 py-2 rounded-lg text-sm font-semibold transition-all bg-dragun-600 text-white shadow-md" data-category="all">All Items</button>
                    <button class="category-btn px-5 py-2 rounded-lg text-sm font-semibold transition-all text-slate-400 hover:text-white hover:bg-slate-800" data-category="bags">Bags</button>
                    <button class="category-btn px-5 py-2 rounded-lg text-sm font-semibold transition-all text-slate-400 hover:text-white hover:bg-slate-800" data-category="caps">Caps</button>
                    <button class="category-btn px-5 py-2 rounded-lg text-sm font-semibold transition-all text-slate-400 hover:text-white hover:bg-slate-800" data-category="raincoats">Raincoats</button>
                </div>
            </div>

            <!-- Product Grid -->
            <div id="product-grid" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-8">
                <!-- Product items injected dynamically via JS -->
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="py-24 border-t border-slate-900 relative overflow-hidden">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
                <div class="space-y-6">
                    <div class="inline-flex items-center gap-2 px-3.5 py-1.5 rounded-full bg-dragun-500/10 border border-dragun-500/20 text-dragun-400 text-xs font-semibold tracking-wider uppercase">
                        The Dragun Philosophy
                    </div>
                    <h2 class="text-3xl sm:text-5xl font-extrabold text-white leading-tight">
                        Built For Those Who Never Stop Exploring.
                    </h2>
                    <p class="text-slate-400 text-base sm:text-lg leading-relaxed">
                        At Dragun Company, we believe that weather should never dictate your limits. Founded by mountaineers and urban explorers, we craft gear that withstands torrential downpours, rugged mountain trails, and the daily grind with uncompromising style.
                    </p>
                    <div class="grid grid-cols-2 gap-6 pt-4">
                        <div class="p-5 rounded-2xl bg-slate-900 border border-slate-800">
                            <div class="w-10 h-10 rounded-xl bg-dragun-500/10 text-dragun-500 flex items-center justify-center text-lg mb-3">
                                <i class="fa-solid fa-shield-halved"></i>
                            </div>
                            <h4 class="text-white font-bold text-lg">Armor Grade</h4>
                            <p class="text-slate-400 text-sm mt-1">Military-spec fabrics resistant to tearing and extreme water pressure.</p>
                        </div>
                        <div class="p-5 rounded-2xl bg-slate-900 border border-slate-800">
                            <div class="w-10 h-10 rounded-xl bg-amber-500/10 text-amber-500 flex items-center justify-center text-lg mb-3">
                                <i class="fa-solid fa-feather"></i>
                            </div>
                            <h4 class="text-white font-bold text-lg">Ultralight Fit</h4>
                            <p class="text-slate-400 text-sm mt-1">Maximum protection without the bulk. Lightweight ergonomic designs.</p>
                        </div>
                    </div>
                </div>
                <div class="relative">
                    <div class="absolute -inset-1 rounded-3xl bg-gradient-to-r from-amber-500 to-dragun-600 opacity-20 blur-xl"></div>
                    <div class="grid grid-cols-2 gap-4 relative">
                        <img src="https://images.unsplash.com/photo-1516738901171-8eb4fc13bd20?q=80&w=600&auto=format&fit=crop" onerror="this.src='https://placehold.co/400x500/0f172a/f97316?text=Adventure'" alt="Adventure 1" class="rounded-2xl object-cover h-72 w-full border border-slate-800">
                        <img src="https://images.unsplash.com/photo-1509316975850-ff9c5deb0cd9?q=80&w=600&auto=format&fit=crop" onerror="this.src='https://placehold.co/400x500/0f172a/f97316?text=Wilderness'" alt="Adventure 2" class="rounded-2xl object-cover h-72 w-full border border-slate-800 mt-8">
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="py-20 bg-slate-900/50 border-t border-slate-900">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="max-w-3xl mx-auto text-center space-y-4 mb-16">
                <span class="text-dragun-500 text-sm font-bold uppercase tracking-wider">Get In Touch</span>
                <h2 class="text-3xl sm:text-4xl font-extrabold text-white">Have Questions About Our Gear?</h2>
                <p class="text-slate-400">Our expedition support team is available 24/7 to help you choose the right equipment.</p>
            </div>
            <div class="max-w-xl mx-auto bg-slate-900 p-8 rounded-3xl border border-slate-800 shadow-xl">
                <form id="contact-form" class="space-y-6" onsubmit="handleContact(event)">
                    <div>
                        <label class="block text-sm font-medium text-slate-300 mb-2">Your Name</label>
                        <input type="text" required placeholder="Alex Mercer" class="w-full bg-slate-950 border border-slate-800 rounded-xl px-4 py-3 text-white placeholder-slate-600 focus:outline-none focus:border-dragun-500 transition-colors">
                    </div>
                    <div>
                        <label class="block text-sm font-medium text-slate-300 mb-2">Email Address</label>
                        <input type="email" required placeholder="alex@example.com" class="w-full bg-slate-950 border border-slate-800 rounded-xl px-4 py-3 text-white placeholder-slate-600 focus:outline-none focus:border-dragun-500 transition-colors">
                    </div>
                    <div>
                        <label class="block text-sm font-medium text-slate-300 mb-2">Message</label>
                        <textarea rows="4" required placeholder="Tell us what gear you are looking for..." class="w-full bg-slate-950 border border-slate-800 rounded-xl px-4 py-3 text-white placeholder-slate-600 focus:outline-none focus:border-dragun-500 transition-colors"></textarea>
                    </div>
                    <button type="submit" class="w-full py-4 rounded-xl bg-dragun-600 hover:bg-dragun-500 text-white font-bold transition-all shadow-lg shadow-dragun-600/30">
                        Send Message
                    </button>
                </form>
            </div>
        </div>
    </section>

    <!-- Shopping Cart Slide-over -->
    <div id="cart-modal" class="fixed inset-0 z-50 overflow-hidden hidden">
        <div id="cart-backdrop" class="absolute inset-0 bg-slate-950/80 backdrop-blur-sm transition-opacity opacity-0"></div>
        <div class="absolute inset-y-0 right-0 max-w-full flex pl-10">
            <div id="cart-panel" class="w-screen max-w-md bg-slate-900 border-l border-slate-800 shadow-2xl transform transition-transform translate-x-full duration-300 flex flex-col">
                <!-- Cart Header -->
                <div class="p-6 border-b border-slate-800 flex items-center justify-between">
                    <div class="flex items-center gap-3">
                        <div class="w-8 h-8 rounded-lg bg-dragun-600/20 text-dragun-500 flex items-center justify-center font-bold">
                            <i class="fa-solid fa-bag-shopping"></i>
                        </div>
                        <h3 class="text-lg font-bold text-white">Your Cart (<span id="cart-item-count">0</span>)</h3>
                    </div>
                    <button id="close-cart" class="p-2 rounded-lg text-slate-400 hover:text-white hover:bg-slate-800 transition-colors">
                        <i class="fa-solid fa-xmark text-lg"></i>
                    </button>
                </div>
                <!-- Cart Items List -->
                <div id="cart-items" class="flex-1 overflow-y-auto p-6 space-y-4 divide-y divide-slate-800/50">
                    <!-- Dynamic cart items -->
                </div>
                <!-- Cart Footer -->
                <div class="p-6 border-t border-slate-800 bg-slate-950/50 space-y-4">
                    <div class="flex justify-between text-base font-medium text-slate-300">
                        <span>Subtotal</span>
                        <span id="cart-subtotal" class="text-white font-bold">$0.00</span>
                    </div>
                    <div class="flex justify-between text-sm text-slate-400">
                        <span>Shipping</span>
                        <span class="text-emerald-400 font-semibold">FREE</span>
                    </div>
                    <div class="border-t border-slate-800 pt-3 flex justify-between text-lg font-bold text-white">
                        <span>Total</span>
                        <span id="cart-total" class="text-dragun-500">$0.00</span>
                    </div>
                    <button id="checkout-btn" onclick="handleCheckout()" class="w-full py-4 rounded-xl bg-gradient-to-r from-dragun-600 to-amber-600 hover:from-dragun-500 hover:to-amber-500 text-white font-bold text-base shadow-lg shadow-dragun-600/30 transition-all flex items-center justify-center gap-2">
                        <i class="fa-solid fa-lock text-sm"></i> Proceed to Checkout
                    </button>
                </div>
            </div>
        </div>
    </div>

    <!-- Toast Notification -->
    <div id="toast" class="fixed bottom-6 right-6 z-50 transform translate-y-24 opacity-0 transition-all duration-300 pointer-events-none">
        <div class="bg-slate-900 border border-dragun-500/50 shadow-2xl rounded-2xl p-4 flex items-center gap-3 text-white">
            <div class="w-8 h-8 rounded-xl bg-dragun-600 text-white flex items-center justify-center font-bold">
                <i class="fa-solid fa-check"></i>
            </div>
            <div>
                <h5 class="text-sm font-bold" id="toast-title">Added to cart</h5>
                <p class="text-xs text-slate-400" id="toast-desc">Item successfully added to your gear bag.</p>
            </div>
        </div>
    </div>

    <!-- Footer -->
    <footer class="bg-slate-950 border-t border-slate-900 py-12">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-8 mb-12">
                <div class="space-y-4 md:col-span-1">
                    <div class="flex items-center gap-3">
                        <div class="w-8 h-8 rounded-xl bg-dragun-600 flex items-center justify-center text-white">
                            <i class="fa-solid fa-dragon"></i>
                        </div>
                        <span class="text-xl font-extrabold text-white">DRAGUN</span>
                    </div>
                    <p class="text-slate-400 text-sm">High-performance bags, caps, and raincoats built for uncompromising explorers.</p>
                </div>
                <div>
                    <h5 class="text-white font-bold text-sm uppercase tracking-wider mb-4">Quick Links</h5>
                    <ul class="space-y-2 text-sm text-slate-400">
                        <li><a href="#home" class="hover:text-dragun-500 transition-colors">Home</a></li>
                        <li><a href="#products" class="hover:text-dragun-500 transition-colors">Products</a></li>
                        <li><a href="#about" class="hover:text-dragun-500 transition-colors">About Us</a></li>
                        <li><a href="#contact" class="hover:text-dragun-500 transition-colors">Contact</a></li>
                    </ul>
                </div>
                <div>
                    <h5 class="text-white font-bold text-sm uppercase tracking-wider mb-4">Categories</h5>
                    <ul class="space-y-2 text-sm text-slate-400">
                        <li><a href="#products" onclick="filterProducts('bags')" class="hover:text-dragun-500 transition-colors">Tactical Bags</a></li>
                        <li><a href="#products" onclick="filterProducts('caps')" class="hover:text-dragun-500 transition-colors">Waterproof Caps</a></li>
                        <li><a href="#products" onclick="filterProducts('raincoats')" class="hover:text-dragun-500 transition-colors">All-Weather Raincoats</a></li>
                    </ul>
                </div>
                <div>
                    <h5 class="text-white font-bold text-sm uppercase tracking-wider mb-4">Stay Adventurous</h5>
                    <p class="text-slate-400 text-sm mb-4">Subscribe to get gear drop notifications and special discounts.</p>
                    <form onsubmit="handleNewsletter(event)" class="flex gap-2">
                        <input type="email" required placeholder="Your email" class="bg-slate-900 border border-slate-800 rounded-xl px-4 py-2.5 text-sm text-white focus:outline-none focus:border-dragun-500 flex-1">
                        <button type="submit" class="px-4 py-2.5 rounded-xl bg-dragun-600 hover:bg-dragun-500 text-white font-semibold text-sm transition-colors">Join</button>
                    </form>
                </div>
            </div>
            <div class="border-t border-slate-900 pt-8 flex flex-col sm:flex-row items-center justify-between text-xs text-slate-500">
                <p>&copy; 2026 Dragun Company. All rights reserved.</p>
                <div class="flex gap-6 mt-4 sm:mt-0">
                    <a href="#" class="hover:text-slate-400 transition-colors">Privacy Policy</a>
                    <a href="#" class="hover:text-slate-400 transition-colors">Terms of Service</a>
                </div>
            </div>
        </div>
    </footer>

    <!-- JavaScript Application Logic -->
    <script>
        // Product Catalog Data
        const products = [
            {
                id: 1,
                name: "Apex Storm Backpack",
                category: "bags",
                price: 129.99,
                rating: 4.9,
                reviews: 128,
                image: "https://images.unsplash.com/photo-1553062407-98eeb64c6a62?q=80&w=600&auto=format&fit=crop",
                description: "35L waterproof tactical backpack with padded laptop compartment and reinforced Cordura fabric."
            },
            {
                id: 2,
                name: "Nomad Hydration Pack",
                category: "bags",
                price: 89.99,
                rating: 4.8,
                reviews: 94,
                image: "https://images.unsplash.com/photo-1622560480605-d83c853bc5c3?q=80&w=600&auto=format&fit=crop",
                description: "Lightweight streamlined hiking pack with integrated water bladder compartment."
            },
            {
                id: 3,
                name: "Vortex Waterproof Cap",
                category: "caps",
                price: 34.99,
                rating: 4.7,
                reviews: 210,
                image: "https://images.unsplash.com/photo-1588850561407-ed78c282e89b?q=80&w=600&auto=format&fit=crop",
                description: "Hydrophobic quick-dry cap featuring breathable mesh panels and reflective brim piping."
            },
            {
                id: 4,
                name: "Dragun Tactical Snapback",
                category: "caps",
                price: 29.99,
                rating: 4.6,
                reviews: 85,
                image: "https://images.unsplash.com/photo-1576871337632-b9aef4c17ab9?q=80&w=600&auto=format&fit=crop",
                description: "Rugged cotton-twill cap with custom embroidered Dragun dragon crest insignia."
            },
            {
                id: 5,
                name: "Monsoon Pro Raincoat",
                category: "raincoats",
                price: 159.99,
                rating: 5.0,
                reviews: 172,
                image: "https://images.unsplash.com/photo-1544441893-675973e31985?q=80&w=600&auto=format&fit=crop",
                description: "Triple-layer breathable waterproof shell jacket designed for extreme downpours."
            },
            {
                id: 6,
                name: "Abyss Storm Poncho",
                category: "raincoats",
                price: 79.99,
                rating: 4.7,
                reviews: 63,
                image: "https://images.unsplash.com/photo-1515886657613-9f3515b0c78f?q=80&w=600&auto=format&fit=crop",
                description: "Over-sized packable emergency rain poncho with sealed seams and storm hood."
            },
            {
                id: 7,
                name: "Explorer Duffel Bag 50L",
                category: "bags",
                price: 119.99,
                rating: 4.9,
                reviews: 112,
                image: "https://images.unsplash.com/photo-1545128485-c400e7702796?q=80&w=600&auto=format&fit=crop",
                description: "Indestructible waterproof travel duffel with backpack straps and heavy-duty zippers."
            },
            {
                id: 8,
                name: "Alpine Thermal Rain Jacket",
                category: "raincoats",
                price: 189.99,
                rating: 4.9,
                reviews: 145,
                image: "https://images.unsplash.com/photo-1495105787522-5334e3ffa0ef?q=80&w=600&auto=format&fit=crop",
                description: "Insulated waterproof winter jacket engineered for freezing mountain winds and rain."
            }
        ];

        let cart = [];

        // DOM Elements
        const productGrid = document.getElementById('product-grid');
        const cartModal = document.getElementById('cart-modal');
        const cartBackdrop = document.getElementById('cart-backdrop');
        const cartPanel = document.getElementById('cart-panel');
        const cartBtn = document.getElementById('cart-btn');
        const closeCartBtn = document.getElementById('close-cart');
        const cartCounter = document.getElementById('cart-counter');
        const cartItemCount = document.getElementById('cart-item-count');
        const cartItemsContainer = document.getElementById('cart-items');
        const cartSubtotal = document.getElementById('cart-subtotal');
        const cartTotal = document.getElementById('cart-total');
        const mobileMenuBtn = document.getElementById('mobile-menu-btn');
        const mobileMenu = document.getElementById('mobile-menu');
        const categoryBtns = document.querySelectorAll('.category-btn');
        const toast = document.getElementById('toast');
        const toastTitle = document.getElementById('toast-title');
        const toastDesc = document.getElementById('toast-desc');

        // Initialize Store
        document.addEventListener('DOMContentLoaded', () => {
            renderProducts(products);
            setupEventListeners();
        });

        function setupEventListeners() {
            // Cart Toggle
            cartBtn.addEventListener('click', openCart);
            closeCartBtn.addEventListener('click', closeCart);
            cartBackdrop.addEventListener('click', closeCart);

            // Mobile menu toggle
            mobileMenuBtn.addEventListener('click', () => {
                mobileMenu.classList.toggle('hidden');
            });

            // Category filters
            categoryBtns.forEach(btn => {
                btn.addEventListener('click', (e) => {
                    categoryBtns.forEach(b => {
                        b.classList.remove('bg-dragun-600', 'text-white', 'shadow-md');
                        b.classList.add('text-slate-400', 'hover:text-white', 'hover:bg-slate-800');
                    });
                    e.target.classList.remove('text-slate-400', 'hover:text-white', 'hover:bg-slate-800');
                    e.target.classList.add('bg-dragun-600', 'text-white', 'shadow-md');
                    
                    const category = e.target.getAttribute('data-category');
                    filterProducts(category);
                });
            });
        }

        function filterProducts(category) {
            if (category === 'all') {
                renderProducts(products);
            } else {
                const filtered = products.filter(p => p.category === category);
                renderProducts(filtered);
            }
        }

        function renderProducts(items) {
            productGrid.innerHTML = '';
            items.forEach(product => {
                const card = document.createElement('div');
                card.className = "group bg-slate-900 border border-slate-800 rounded-3xl overflow-hidden hover:border-dragun-500/50 transition-all duration-300 flex flex-col justify-between shadow-lg hover:shadow-2xl hover:shadow-dragun-600/10";
                card.innerHTML = `
                    <div>
                        <div class="relative overflow-hidden bg-slate-950 h-64">
                            <img src="${product.image}" onerror="this.src='https://placehold.co/600x600/0f172a/f97316?text=Dragun+Item'" alt="${product.name}" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500">
                            <span class="absolute top-4 left-4 uppercase tracking-wider text-[10px] font-bold px-3 py-1 rounded-full bg-slate-900/80 backdrop-blur-md text-dragun-400 border border-slate-800">
                                ${product.category}
                            </span>
                            <div class="absolute bottom-4 right-4 bg-slate-900/90 backdrop-blur-md px-2.5 py-1 rounded-lg border border-slate-800 flex items-center gap-1.5 text-xs font-bold text-amber-400">
                                <i class="fa-solid fa-star"></i> ${product.rating} <span class="text-slate-500 font-normal">(${product.reviews})</span>
                            </div>
                        </div>
                        <div class="p-6">
                            <h3 class="text-lg font-bold text-white group-hover:text-dragun-400 transition-colors">${product.name}</h3>
                            <p class="text-slate-400 text-xs mt-2 line-clamp-2 leading-relaxed">${product.description}</p>
                        </div>
                    </div>
                    <div class="p-6 pt-0 flex items-center justify-between">
                        <span class="text-xl font-extrabold text-white">$${product.price.toFixed(2)}</span>
                        <button onclick="addToCart(${product.id})" class="px-4 py-2.5 rounded-xl bg-slate-800 hover:bg-dragun-600 text-white font-semibold text-sm transition-all flex items-center gap-2 border border-slate-700 hover:border-dragun-500 shadow-sm">
                            <i class="fa-solid fa-plus text-xs"></i> Add to Cart
                        </button>
                    </div>
                `;
                productGrid.appendChild(card);
            });
        }

        function addToCart(productId) {
            const product = products.find(p => p.id === productId);
            const existingItem = cart.find(item => item.id === productId);

            if (existingItem) {
                existingItem.quantity += 1;
            } else {
                cart.push({ ...product, quantity: 1 });
            }

            updateCartUI();
            showToast("Added to Cart", `${product.name} has been added to your gear bag.`);
        }

        function removeFromCart(productId) {
            cart = cart.filter(item => item.id !== productId);
            updateCartUI();
        }

        function updateQuantity(productId, delta) {
            const item = cart.find(i => i.id === productId);
            if (item) {
                item.quantity += delta;
                if (item.quantity <= 0) {
                    removeFromCart(productId);
                } else {
                    updateCartUI();
                }
            }
        }

        function updateCartUI() {
            const totalItems = cart.reduce((sum, item) => sum + item.quantity, 0);
            cartCounter.textContent = totalItems;
            cartItemCount.textContent = totalItems;

            if (totalItems > 0) {
                cartCounter.classList.add('scale-125');
                setTimeout(() => cartCounter.classList.remove('scale-125'), 200);
            }

            cartItemsContainer.innerHTML = '';
            if (cart.length === 0) {
                cartItemsContainer.innerHTML = `
                    <div class="text-center py-16 space-y-3">
                        <div class="w-16 h-16 rounded-2xl bg-slate-800 text-slate-500 mx-auto flex items-center justify-center text-2xl">
                            <i class="fa-solid fa-bag-shopping"></i>
                        </div>
                        <p class="text-slate-400 text-sm font-medium">Your gear bag is currently empty.</p>
                    </div>
                `;
            } else {
                cart.forEach(item => {
                    const div = document.createElement('div');
                    div.className = "py-4 flex items-center gap-4";
                    div.innerHTML = `
                        <img src="${item.image}" onerror="this.src='https://placehold.co/100x100/0f172a/f97316?text=Item'" alt="${item.name}" class="w-16 h-16 object-cover rounded-xl border border-slate-800">
                        <div class="flex-1">
                            <h4 class="text-white font-bold text-sm">${item.name}</h4>
                            <div class="text-dragun-500 font-bold text-sm mt-0.5">$${item.price.toFixed(2)}</div>
                            <div class="flex items-center gap-3 mt-2">
                                <div class="flex items-center border border-slate-800 rounded-lg bg-slate-950">
                                    <button onclick="updateQuantity(${item.id}, -1)" class="px-2 py-0.5 text-slate-400 hover:text-white">-</button>
                                    <span class="px-2 text-xs font-bold text-white">${item.quantity}</span>
                                    <button onclick="updateQuantity(${item.id}, 1)" class="px-2 py-0.5 text-slate-400 hover:text-white">+</button>
                                </div>
                                <button onclick="removeFromCart(${item.id})" class="text-xs text-rose-400 hover:text-rose-300 font-medium">Remove</button>
                            </div>
                        </div>
                    `;
                    cartItemsContainer.appendChild(div);
                });
            }

            const subtotal = cart.reduce((sum, item) => sum + (item.price * item.quantity), 0);
            cartSubtotal.textContent = `$${subtotal.toFixed(2)}`;
            cartTotal.textContent = `$${subtotal.toFixed(2)}`;
        }

        function openCart() {
            cartModal.classList.remove('hidden');
            setTimeout(() => {
                cartBackdrop.classList.remove('opacity-0');
                cartPanel.classList.remove('translate-x-full');
            }, 10);
        }

        function closeCart() {
            cartBackdrop.classList.add('opacity-0');
            cartPanel.classList.add('translate-x-full');
            setTimeout(() => {
                cartModal.classList.add('hidden');
            }, 300);
        }

        function handleCheckout() {
            if (cart.length === 0) {
                showToast("Cart is Empty", "Add some gear before proceeding to checkout.");
                return;
            }
            showToast("Order Placed Successfully! 🎉", "Thank you for shopping with Dragun Company.");
            cart = [];
            updateCartUI();
            closeCart();
        }

        function handleContact(e) {
            e.preventDefault();
            showToast("Message Sent!", "We will get back to you within 24 hours.");
            e.target.reset();
        }

        function handleNewsletter(e) {
            e.preventDefault();
            showToast("Subscribed!", "You are now on the Dragun VIP explorer list.");
            e.target.reset();
        }

        function showToast(title, desc) {
            toastTitle.textContent = title;
            toastDesc.textContent = desc;
            toast.classList.remove('translate-y-24', 'opacity-0');
            setTimeout(() => {
                toast.classList.add('translate-y-24', 'opacity-0');
            }, 3500);
        }
    </script>
</body>
</html>
https://github.com/dragunr3377/dragunr.github.io/commit/eeb25d0e992f8062b51d679909c0fe772d62d5b8
Your Style, Your Choice!

