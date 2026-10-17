🛍️ DRAGUN R
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
                    <input type="text" placeholder="Search for Products, Brands and More" class="w-full py-1.5 px-4 rounded text-black text-sm focus:outline-none">
                    <i class="fa-solid fa-magnifying-glass absolute right-3 top-2.5 text-gray-500"></i>
                </div>
            </div>

            <!-- Right Icons -->
            <div class="flex items-center space-x-5 text-sm font-medium">
                <button class="bg-white text-blue-600 px-4 py-1 rounded font-bold">Login</button>
                <div class="hidden md:block">More</div>
                <div class="flex items-center space-x-1 cursor-pointer">
                    <i class="fa-solid fa-cart-shopping"></i>
                    <span>Cart</span>
                </div>
            </div>
        </div>
    </header>

    <!-- Categories Section -->
    <nav class="bg-white shadow-sm py-3 px-4 overflow-x-auto whitespace-nowrap">
        <div class="container mx-auto flex justify-between space-x-8 text-center text-sm font-semibold text-gray-700">
            <div class="cursor-pointer hover:text-blue-600"><i class="fa-solid fa-bolt block text-lg text-blue-600 mb-1"></i>Top Offers</div>
            <div class="cursor-pointer hover:text-blue-600"><i class="fa-solid fa-mobile-screen block text-lg text-blue-600 mb-1"></i>Mobiles</div>
            <div class="cursor-pointer hover:text-blue-600"><i class="fa-solid fa-shirt block text-lg text-blue-600 mb-1"></i>Fashion</div>
            <div class="cursor-pointer hover:text-blue-600"><i class="fa-solid fa-laptop block text-lg text-blue-600 mb-1"></i>Electronics</div>
            <div class="cursor-pointer hover:text-blue-600"><i class="fa-solid fa-couch block text-lg text-blue-600 mb-1"></i>Home</div>
            <div class="cursor-pointer hover:text-blue-600"><i class="fa-solid fa-plane block text-lg text-blue-600 mb-1"></i>Flights</div>
        </div>
    </nav>

    <!-- Banner Section -->
    <section class="container mx-auto p-3">
        <div class="bg-blue-500 rounded-lg text-white p-6 text-center shadow-md">
            <h2 class="text-2xl font-bold mb-2">Welcome to DRAGUN R Big Billion Days!</h2>
            <p class="text-sm mb-4">Grab the best deals on electronics, fashion, and more.</p>
            <button class="bg-yellow-400 text-black font-bold px-6 py-2 rounded shadow hover:bg-yellow-500">Shop Now</button>
        </div>
    </section>

    <!-- Products Grid -->
    <main class="container mx-auto p-3">
        <h3 class="text-lg font-bold mb-3 text-gray-800">Suggested for You</h3>
        <div class="grid grid-cols-2 md:grid-cols-4 gap-4">
            <!-- Product Card 1 -->
            <div class="bg-white p-3 rounded shadow hover:shadow-lg transition">
                <div class="bg-gray-200 h-40 rounded flex items-center justify-center text-gray-500 mb-2">Product Image</div>
                <h4 class="font-semibold text-sm truncate">Smart Watch Pro</h4>
                <p class="text-green-600 font-bold text-sm">₹1,999 <span class="line-through text-gray-400 text-xs">₹4,999</span></p>
                <span class="text-xs bg-green-100 text-green-700 px-1 rounded">60% off</span>
            </div>
            <!-- Product Card 2 -->
            <div class="bg-white p-3 rounded shadow hover:shadow-lg transition">
                <div class="bg-gray-200 h-40 rounded flex items-center justify-center text-gray-500 mb-2">Product Image</div>
                <h4 class="font-semibold text-sm truncate">Wireless Earbuds</h4>
                <p class="text-green-600 font-bold text-sm">₹999 <span class="line-through text-gray-400 text-xs">₹2,999</span></p>
                <span class="text-xs bg-green-100 text-green-700 px-1 rounded">66% off</span>
            </div>
            <!-- Product Card 3 -->
            <div class="bg-white p-3 rounded shadow hover:shadow-lg transition">
                <div class="bg-gray-200 h-40 rounded flex items-center justify-center text-gray-500 mb-2">Product Image</div>
                <h4 class="font-semibold text-sm truncate">Running Shoes</h4>
                <p class="text-green-600 font-bold text-sm">₹1,299 <span class="line-through text-gray-400 text-xs">₹2,500</span></p>
                <span class="text-xs bg-green-100 text-green-700 px-1 rounded">48% off</span>
            </div>
            <!-- Product Card 4 -->
            <div class="bg-white p-3 rounded shadow hover:shadow-lg transition">
                <div class="bg-gray-200 h-40 rounded flex items-center justify-center text-gray-500 mb-2">Product Image</div>
                <h4 class="font-semibold text-sm truncate">DSQL Camera</h4>
                <p class="text-green-600 font-bold text-sm">₹35,999 <span class="line-through text-gray-400 text-xs">₹45,000</span></p>
                <span class="text-xs bg-green-100 text-green-700 px-1 rounded">20% off</span>
            </div>
        </div>
    </main>

</body>
</html>
