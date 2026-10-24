

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
