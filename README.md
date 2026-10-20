
<!DOCTYPE html>
<html lang="hi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dragon R - Realistic Rain Scene</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background-color: #050508;
            overflow: hidden;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }

        /* Canvas for Rain Effect */
        #rainCanvas {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 2;
            pointer-events: none;
        }

        /* Scene Container */
        .scene-container {
            position: relative;
            width: 100%;
            max-width: 800px;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            background: radial-gradient(circle at center, #1a1c29 0%, #08090f 100%);
            box-shadow: 0 0 50px rgba(0, 0, 0, 0.8);
            overflow: hidden;
        }

        /* Lighting & Flash Effect */
        .lightning {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(255, 255, 255, 0.05);
            z-index: 1;
            animation: flash 6s infinite;
        }

        @keyframes flash {
            0%, 95%, 98%, 100% { opacity: 0; }
            96%, 99% { opacity: 1; }
        }

        /* Character & Jacket Visuals */
        .character-wrapper {
            position: relative;
            z-index: 3;
            display: flex;
            flex-direction: column;
            align-items: center;
            transform: scale(0.95);
            animation: breath 4s ease-in-out infinite;
        }

        @keyframes breath {
            0%, 100% { transform: scale(0.95) translateY(0); }
            50% { transform: scale(0.96) translateY(-5px); }
        }

        /* Boy's Head */
        .head {
            width: 70px;
            height: 85px;
            background: #2b1f1d;
            border-radius: 35px 35px 25px 25px;
            position: relative;
            box-shadow: inset -5px -5px 15px rgba(0,0,0,0.6);
        }

        .hair {
            position: absolute;
            top: -10px;
            width: 100%;
            height: 45px;
            background: #0d0d0d;
            border-radius: 40px 40px 0 0;
        }

        /* Dragon R Jacket Styling */
        .jacket {
            position: relative;
            width: 220px;
            height: 260px;
            background: linear-gradient(135deg, #111 0%, #1e2638 50%, #0d131d 100%);
            border-radius: 30px 30px 10px 10px;
            margin-top: -10px;
            box-shadow: 0 15px 35px rgba(0,0,0,0.8), inset 0 2px 5px rgba(255,255,255,0.2);
            border-top: 3px solid #3a4b6e;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        /* Zipper line */
        .jacket::before {
            content: '';
            position: absolute;
            top: 0;
            width: 4px;
            height: 100%;
            background: #444;
            box-shadow: 0 0 2px rgba(255,255,255,0.5);
        }

        /* Dragon R Brand Logo */
        .brand-logo {
            position: absolute;
            top: 40px;
            left: 30px;
            display: flex;
            align-items: center;
            gap: 5px;
            background: rgba(0, 0, 0, 0.4);
            padding: 5px 10px;
            border-radius: 5px;
            border: 1px solid rgba(255, 69, 0, 0.5);
        }

        .dragon-icon {
            color: #ff4500;
            font-weight: bold;
            font-size: 18px;
            text-shadow: 0 0 8px #ff4500;
        }

        .brand-name {
            color: #ffffff;
            font-size: 12px;
            font-weight: 800;
            letter-spacing: 1px;
        }

        /* Price Tag Overlay */
        .price-badge {
            position: absolute;
            bottom: 30px;
            right: -20px;
            background: linear-gradient(45deg, #ff4500, #ff0055);
            color: #fff;
            padding: 10px 20px;
            border-radius: 25px;
            font-weight: bold;
            font-size: 20px;
            box-shadow: 0 5px 20px rgba(255, 69, 0, 0.5);
            z-index: 4;
            animation: pulse 2s infinite;
            border: 2px solid #fff;
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.08); }
        }

        /* Wet Ground Reflection */
        .ground {
            position: absolute;
            bottom: 0;
            width: 100%;
            height: 120px;
            background: linear-gradient(to top, #05070a, transparent);
            border-top: 1px solid rgba(255,255,255,0.05);
        }
    </style>
</head>
<body>

    <div class="scene-container">
        <div class="lightning"></div>
        <canvas id="rainCanvas"></canvas>

        <div class="character-wrapper">
            <!-- Head -->
            <div class="head">
                <div class="hair"></div>
            </div>

            <!-- Jacket -->
            <div class="jacket">
                <!-- Dragon R Branding -->
                <div class="brand-logo">
                    <span class="dragon-icon">🐉</span>
                    <span class="brand-name">DRAGON R</span>
                </div>
            </div>

            <!-- Price Tag -->
            <div class="price-badge">
                ₹999 ONLY
            </div>
        </div>

        <div class="ground"></div>
    </div>

    <script>
        const canvas = document.getElementById('rainCanvas');
        const ctx = canvas.getContext('2d');

        function resizeCanvas() {
            canvas.width = window.innerWidth;
            canvas.height = window.innerHeight;
        }
        resizeCanvas();
        window.addEventListener('resize', resizeCanvas);

        // Raindrops Array
        const drops = [];
        const dropCount = 300;

        for (let i = 0; i < dropCount; i++) {
            drops.push({
                x: Math.random() * canvas.width,
                y: Math.random() * canvas.height,
                length: Math.random() * 20 + 10,
                speed: Math.random() * 10 + 12,
                opacity: Math.random() * 0.5 + 0.2
            });
        }

        // Draw Rain Animation Loop
        function drawRain() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);

            ctx.lineWidth = 1.5;
            ctx.lineCap = 'round';

            drops.forEach(drop => {
                ctx.beginPath();
                ctx.strokeStyle = `rgba(174, 194, 224, ${drop.opacity})`;
                ctx.moveTo(drop.x, drop.y);
                ctx.lineTo(drop.x - 2, drop.y + drop.length);
                ctx.stroke();

                // Move drop down
                drop.y += drop.speed;
                drop.x -= 0.5; // Slight slant for wind

                // Reset drop position
                if (drop.y > canvas.height) {
                    drop.y = -20;
                    drop.x = Math.random() * canvas.width;
                }
            });

            requestAnimationFrame(drawRain);
        }

        drawRain();
    </script>
</body>
</html>


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DRAGUN R - Online Shopping App</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
</head>
<body class="bg-gray-100">

    <!-- Header / Navbar -->
    <header class="bg-blue-600 text-white p-3 sticky top-0 z-50 shadow-md">
        <div class="container mx-auto flex items-center justify-between">
            <!-- Logo -->
            <div class="flex items-center space-x-2">
                <span class="text-xl font-bold italic tracking-wider">DRAGUN R</span>
                <span class="text-xs bg-yellow-400 text-black px-1 rounded font-semibold">Explore Plus</span>
            </div>
            
            <!-- Search Bar -->
            <div class="flex-1 mx-4">
                <div class="relative">
                    <input type="text" id="searchInput" placeholder="Search for Clothes, Raincoats, Watches, Bags..." class="w-full py-1.5 px-4 rounded text-black text-sm focus:outline-none">
                    <i class="fa-solid fa-magnifying-glass absolute right-3 top-2.5 text-gray-500"></i>
                </div>
            </div>

            <!-- Right Icons -->
            <div class="flex items-center space-x-5 text-sm font-medium">
                <button onclick="openLoginModal()" class="bg-white text-blue-600 px-4 py-1 rounded font-bold hover:bg-gray-100">Login</button>
                <div class="hidden md:block cursor-pointer">More</div>
                <div onclick="openCart()" class="flex items-center space-x-1 cursor-pointer relative">
                    <i class="fa-solid fa-cart-shopping text-lg"></i>
                    <span>Cart</span>
                    <span id="cartCount" class="absolute -top-2 -right-2 bg-yellow-400 text-black text-xs font-bold rounded-full h-5 w-5 flex items-center justify-center">0</span>
                </div>
            </div>
        </div>
    </header>

    <!-- Categories Section -->
    <nav class="bg-white shadow-sm py-3 px-4 overflow-x-auto whitespace-nowrap">
        <div class="container mx-auto flex justify-between space-x-8 text-center text-sm font-semibold text-gray-700">
            <div class="cursor-pointer hover:text-blue-600"><i class="fa-solid fa-bolt block text-lg text-blue-600 mb-1"></i>Top Offers</div>
            <div class="cursor-pointer hover:text-blue-600"><i class="fa-solid fa-shirt block text-lg text-blue-600 mb-1"></i>Fashion / Clothes</div>
            <div class="cursor-pointer hover:text-blue-600"><i class="fa-solid fa-cloud-rain block text-lg text-blue-600 mb-1"></i>Raincoats</div>
            <div class="cursor-pointer hover:text-blue-600"><i class="fa-solid fa-bag-shopping block text-lg text-blue-600 mb-1"></i>Bags</div>
            <div class="cursor-pointer hover:text-blue-600"><i class="fa-solid fa-clock block text-lg text-blue-600 mb-1"></i>Watches</div>
            <div class="cursor-pointer hover:text-blue-600"><i class="fa-solid fa-mobile-screen block text-lg text-blue-600 mb-1"></i>Mobiles</div>
        </div>
    </nav>

    <!-- Banner Section -->
    <section class="container mx-auto p-3">
        <div class="bg-blue-500 rounded-lg text-white p-6 text-center shadow-md">
            <h2 class="text-2xl font-bold mb-2">Welcome to DRAGUN R Mega Sale!</h2>
            <p class="text-sm mb-4">Discover Raincoats, Trendy Clothes, Stylish Bags & Watches on huge discounts.</p>
            <button class="bg-yellow-400 text-black font-bold px-6 py-2 rounded shadow hover:bg-yellow-500">Shop Now</button>
        </div>
    </section>

    <!-- Products Grid -->
    <main class="container mx-auto p-3">
        <h3 class="text-lg font-bold mb-3 text-gray-800">Featured Products</h3>
        <div id="productGrid" class="grid grid-cols-2 md:grid-cols-4 gap-4">
            
            <!-- Product 1: Watch -->
            <div class="product-card bg-white p-3 rounded shadow hover:shadow-lg transition flex flex-col justify-between">
                <div>
                    <img src="https://images.unsplash.com/photo-1523275335684-37898b6baf30?w=300&q=80" alt="Watch" class="h-40 w-full object-cover rounded mb-2">
                    <h4 class="font-semibold text-sm truncate">Luxury Analog Watch</h4>
                    <p class="text-green-600 font-bold text-sm">₹1,499 <span class="line-through text-gray-400 text-xs">₹3,999</span></p>
                    <span class="text-xs bg-green-100 text-green-700 px-1 rounded">62% off</span>
                </div>
                <button onclick="addToCart('Luxury Analog Watch', 1499)" class="mt-3 bg-yellow-400 hover:bg-yellow-500 text-black font-semibold text-xs py-1.5 rounded w-full">Add to Cart</button>
            </div>

            <!-- Product 2: Raincoat -->
            <div class="product-card bg-white p-3 rounded shadow hover:shadow-lg transition flex flex-col justify-between">
                <div>
                    <img src="https://images.unsplash.com/photo-1515886657613-9f3515b0c78f?w=300&q=80" alt="Raincoat" class="h-40 w-full object-cover rounded mb-2">
                    <h4 class="font-semibold text-sm truncate">Waterproof Raincoat</h4>
                    <p class="text-green-600 font-bold text-sm">₹799 <span class="line-through text-gray-400 text-xs">₹1,999</span></p>
                    <span class="text-xs bg-green-100 text-green-700 px-1 rounded">60% off</span>
                </div>
                <button onclick="addToCart('Waterproof Raincoat', 799)" class="mt-3 bg-yellow-400 hover:bg-yellow-500 text-black font-semibold text-xs py-1.5 rounded w-full">Add to Cart</button>
            </div>

            <!-- Product 3: Bag -->
            <div class="product-card bg-white p-3 rounded shadow hover:shadow-lg transition flex flex-col justify-between">
                <div>
                    <img src="https://images.unsplash.com/photo-1553062407-98eeb64c6a62?w=300&q=80" alt="Bag" class="h-40 w-full object-cover rounded mb-2">
                    <h4 class="font-semibold text-sm truncate">Stylish Laptop Backpack</h4>
                    <p class="text-green-600 font-bold text-sm">₹1,199 <span class="line-through text-gray-400 text-xs">₹2,999</span></p>
                    <span class="text-xs bg-green-100 text-green-700 px-1 rounded">60% off</span>
                </div>
                <button onclick="addToCart('Stylish Laptop Backpack', 1199)" class="mt-3 bg-yellow-400 hover:bg-yellow-500 text-black font-semibold text-xs py-1.5 rounded w-full">Add to Cart</button>
            </div>

            <!-- Product 4: Clothes (Shirt) -->
            <div class="product-card bg-white p-3 rounded shadow hover:shadow-lg transition flex flex-col justify-between">
                <div>
                    <img src="https://images.unsplash.com/photo-1521572267360-ee0c2909d518?w=300&q=80" alt="Clothes" class="h-40 w-full object-cover rounded mb-2">
                    <h4 class="font-semibold text-sm truncate">Men's Casual Cotton T-Shirt</h4>
                    <p class="text-green-600 font-bold text-sm">₹499 <span class="line-through text-gray-400 text-xs">₹1,299</span></p>
                    <span class="text-xs bg-green-100 text-green-700 px-1 rounded">61% off</span>
                </div>
                <button onclick="addToCart('Mens Casual Cotton T-Shirt', 499)" class="mt-3 bg-yellow-400 hover:bg-yellow-500 text-black font-semibold text-xs py-1.5 rounded w-full">Add to Cart</button>
            </div>

            <!-- Product 5: Shoes -->
            <div class="product-card bg-white p-3 rounded shadow hover:shadow-lg transition flex flex-col justify-between">
                <div>
                    <img src="https://images.unsplash.com/photo-1542291026-7eec264c27ff?w=300&q=80" alt="Shoes" class="h-40 w-full object-cover rounded mb-2">
                    <h4 class="font-semibold text-sm truncate">Running Sports Shoes</h4>
                    <p class="text-green-600 font-bold text-sm">₹1,299 <span class="line-through text-gray-400 text-xs">₹2,500</span></p>
                    <span class="text-xs bg-green-100 text-green-700 px-1 rounded">48% off</span>
                </div>
                <button onclick="addToCart('Running Sports Shoes', 1299)" class="mt-3 bg-yellow-400 hover:bg-yellow-500 text-black font-semibold text-xs py-1.5 rounded w-full">Add to Cart</button>
            </div>

            <!-- Product 6: Smartwatch
