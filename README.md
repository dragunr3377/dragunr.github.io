🛍️ DRAGUN R

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

Welcome to DRAGUN R — Your Trusted Shopping Destination

DRAGUN R में आपका स्वागत है! हमारा उद्देश्य आपको रोजमर्रा में काम आने वाले उपयोगी, स्टाइलिश और अच्छी क्वालिटी के प्रोडक्ट उपलब्ध कराना है। हम आपके लिए रेनकोट, टोपी, बैग और कई अन्य जरूरी सामान एक ही जगह लेकर आए हैं।

🛒 Our Products | हमारे प्रोडक्ट

🌧️ 1. Raincoats

बारिश में खुद को सूखा रखने के लिए हमारे रेनकोट देखें। रोजाना इस्तेमाल, यात्रा और काम के लिए अपनी पसंद का रेनकोट चुनें।

🧢 2. Caps & Hats

अपने स्टाइल को बेहतर बनाने और धूप से बचाव के लिए अलग-अलग डिजाइन की टोपी चुनें।

🎒 3. Bags

स्कूल, ऑफिस, यात्रा और रोजमर्रा के इस्तेमाल के लिए अपनी जरूरत के अनुसार बैग खरीदें।

⭐ 4. Other Useful Products

DRAGUN R पर आपको अन्य उपयोगी सामान भी मिलेंगे, जो आपकी रोजमर्रा की जरूरतों को पूरा करने में मदद करेंगे।

💎 Why Choose DRAGUN R?

- ✅ उपयोगी प्रोडक्ट की शानदार रेंज
- ✅ अलग-अलग डिजाइन और विकल्प
- ✅ आपकी जरूरत के अनुसार खरीदारी
- ✅ आसान ऑनलाइन शॉपिंग
- ✅ ग्राहकों की सहायता के लिए संपर्क सुविधा

प्रोडक्ट की क्वालिटी, कीमत, डिलीवरी और रिटर्न की शर्तें संबंधित प्रोडक्ट की जानकारी में दी जाएंगी।

🛍️ Shop With Us

आपकी जरूरत, आपकी पसंद और आपकी खरीदारी — सब कुछ एक ही जगह!

आज ही DRAGUN R के प्रोडक्ट देखें और अपनी पसंद का सामान चुनें।

Explore Products | Shop Now

📞 Contact Us

क्या आपको किसी प्रोडक्ट के बारे में जानकारी चाहिए? ऑर्डर करना चाहते हैं या कोई सवाल पूछना चाहते हैं? हमारी टीम से संपर्क करें।

Company Name: DRAGUN R
Customer Support: WhatsApp / Contact Us
Email: [अपना ईमेल यहाँ जोड़ें]
Address: [अपना व्यावसायिक पता यहाँ जोड़ें]

❤️ DRAGUN R — Shopping Made Simple!

आपकी जरूरतों के लिए उपयोगी सामान, आपकी पसंद के साथ।git remote add origin https://github.com/dragunr3377/dragun.github.io.git
git branch -M main
git push -u origin maingit remote add origin https://github.com/dragunr3377/dragun.github.io.git
git branch -M main
git push -u origin main# dragunr.github.io
