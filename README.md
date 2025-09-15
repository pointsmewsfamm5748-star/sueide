<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sneaker Collection | Fusion of Style and Outdoor Performance</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdn.jsdelivr.net/npm/font-awesome@4.7.0/css/font-awesome.min.css" rel="stylesheet">
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        primary: '#007aff',
                        dark: '#111111',
                        light: '#f8f9fa'
                    },
                    fontFamily: {
                        sans: ['Inter', 'system-ui', 'sans-serif'],
                    },
                }
            }
        }
    </script>
    <style type="text/tailwindcss">
        @layer utilities {
            .content-auto {
                content-visibility: auto;
            }
            .text-shadow {
                text-shadow: 0 2px 4px rgba(0,0,0,0.3);
            }
            .transition-custom {
                transition: all 0.3s ease;
            }
            .hover-lift {
                transition: transform 0.3s ease, box-shadow 0.3s ease;
            }
            .hover-lift:hover {
                transform: translateY(-5px);
                box-shadow: 0 10px 25px -5px rgba(0, 122, 255, 0.2), 0 8px 10px -6px rgba(0, 122, 255, 0.1);
            }
            .scroll-indicator {
                height: 3px;
                background-color: #007aff;
                position: fixed;
                top: 0;
                left: 0;
                z-index: 60;
                width: 0%;
            }
        }
    </style>
</head>
<body class="bg-light text-dark antialiased">
    <!-- Scroll Progress Indicator -->
    <div id="scrollIndicator" class="scroll-indicator"></div>

    <!-- Navigation -->
    <header id="navbar" class="fixed w-full z-50 transition-all duration-300 bg-transparent">
        <div class="container mx-auto px-4 py-4 flex items-center justify-between">
            <a href="#" class="text-2xl font-bold text-white text-shadow">STEP</a>
            
            <!-- Desktop Navigation -->
            <nav class="hidden md:flex items-center space-x-8">
                <a href="#home" class="text-white hover:text-primary/80 transition-custom">Home</a>
                <a href="#collection" class="text-white hover:text-primary/80 transition-custom">Collection</a>
                <a href="#features" class="text-white hover:text-primary/80 transition-custom">Features</a>
                <a href="#reviews" class="text-white hover:text-primary/80 transition-custom">Reviews</a>
                <a href="#contact" class="text-white hover:text-primary/80 transition-custom">Contact</a>
            </nav>
            
            <!-- Navigation Icons -->
            <div class="hidden md:flex items-center space-x-6">
                <a href="#" class="text-white hover:text-primary/80 transition-custom">
                    <i class="fa fa-search text-xl"></i>
                </a>
                <a href="#" class="text-white hover:text-primary/80 transition-custom">
                    <i class="fa fa-user text-xl"></i>
                </a>
                <a href="#" class="text-white hover:text-primary/80 transition-custom relative">
                    <i class="fa fa-shopping-cart text-xl"></i>
                    <span class="absolute -top-2 -right-2 bg-primary text-white text-xs rounded-full w-5 h-5 flex items-center justify-center">3</span>
                </a>
            </div>
            
            <!-- Mobile Menu Button -->
            <button id="mobileMenuBtn" class="md:hidden text-white text-2xl">
                <i class="fa fa-bars"></i>
            </button>
        </div>
        
        <!-- Mobile Navigation -->
        <div id="mobileMenu" class="md:hidden bg-white shadow-lg absolute w-full left-0 top-full transform -translate-y-full opacity-0 transition-all duration-300 pointer-events-none">
            <div class="container mx-auto px-4 py-4 flex flex-col space-y-4">
                <a href="#home" class="text-dark hover:text-primary transition-custom py-2 border-b border-gray-100">Home</a>
                <a href="#collection" class="text-dark hover:text-primary transition-custom py-2 border-b border-gray-100">Collection</a>
                <a href="#features" class="text-dark hover:text-primary transition-custom py-2 border-b border-gray-100">Features</a>
                <a href="#reviews" class="text-dark hover:text-primary transition-custom py-2 border-b border-gray-100">Reviews</a>
                <a href="#contact" class="text-dark hover:text-primary transition-custom py-2">Contact</a>
                
                <div class="flex justify-between pt-4">
                    <a href="#" class="text-dark hover:text-primary transition-custom">
                        <i class="fa fa-search text-xl"></i>
                    </a>
                    <a href="#" class="text-dark hover:text-primary transition-custom">
                        <i class="fa fa-user text-xl"></i>
                    </a>
                    <a href="#" class="text-dark hover:text-primary transition-custom relative">
                        <i class="fa fa-shopping-cart text-xl"></i>
                        <span class="absolute -top-2 -right-2 bg-primary text-white text-xs rounded-full w-5 h-5 flex items-center justify-center">3</span>
                    </a>
                </div>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section id="home" class="relative h-screen bg-dark overflow-hidden">
        <div class="absolute inset-0 z-0">
            <img src="https://picsum.photos/id/1059/1920/1080" alt="Stylish sneakers on urban background" class="w-full h-full object-cover opacity-60">
            <div class="absolute inset-0 bg-gradient-to-r from-dark/80 to-dark/40"></div>
        </div>
        
        <div class="container mx-auto px-4 h-full flex items-center relative z-10">
            <div class="max-w-2xl" data-aos="fade-right">
                <h1 class="text-[clamp(2.5rem,6vw,4.5rem)] font-bold text-white leading-tight text-shadow mb-6">
                    Elevate Your <span class="text-primary">Step</span> With Style
                </h1>
                <p class="text-[clamp(1rem,2vw,1.25rem)] text-gray-200 mb-8 max-w-xl">
                    Discover our premium collection of mesh sneakers and outdoor footwear designed for both style and performance.
                </p>
                <div class="flex flex-wrap gap-4">
                    <a href="#collection" class="bg-primary hover:bg-primary/90 text-white font-medium px-8 py-3 rounded-full transition-custom hover-lift">
                        Explore Collection
                    </a>
                    <a href="#features" class="bg-transparent border-2 border-white hover:border-primary hover:text-primary text-white font-medium px-8 py-3 rounded-full transition-custom hover-lift">
                        Learn More
                    </a>
                </div>
            </div>
        </div>
        
        <div class="absolute bottom-10 left-1/2 transform -translate-x-1/2 text-white animate-bounce">
            <a href="#collection" class="flex flex-col items-center">
                <span class="mb-2 text-sm font-medium">Scroll Down</span>
                <i class="fa fa-chevron-down"></i>
            </a>
        </div>
    </section>

    <!-- Collection Section -->
    <section id="collection" class="py-20 bg-light">
        <div class="container mx-auto px-4">
            <div class="text-center mb-16">
                <h2 class="text-[clamp(1.5rem,3vw,2.5rem)] font-bold mb-4">Our Collection</h2>
                <p class="text-gray-600 max-w-2xl mx-auto">Discover our carefully curated selection of premium sneakers, designed for both urban style and outdoor adventures.</p>
                
                <div class="flex justify-center mt-8 space-x-4 flex-wrap">
                    <button class="collection-filter active px-6 py-2 rounded-full bg-primary text-white font-medium transition-custom">All</button>
                    <button class="collection-filter px-6 py-2 rounded-full bg-gray-200 hover:bg-gray-300 transition-custom">Mesh Sneakers</button>
                    <button class="collection-filter px-6 py-2 rounded-full bg-gray-200 hover:bg-gray-300 transition-custom">Outdoor</button>
                    <button class="collection-filter px-6 py-2 rounded-full bg-gray-200 hover:bg-gray-300 transition-custom">Casual</button>
                </div>
            </div>
            
            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-8">
                <!-- Product 1 -->
                <div class="product-card hover-lift bg-white rounded-xl overflow-hidden shadow-md">
                    <div class="relative group">
                        <img src="https://picsum.photos/id/96/800/800" alt="Lightweight mesh running sneakers" class="w-full h-64 object-cover">
                        <div class="absolute inset-0 bg-primary/20 opacity-0 group-hover:opacity-100 transition-custom flex items-center justify-center gap-3">
                            <button class="bg-white text-dark w-10 h-10 rounded-full flex items-center justify-center hover:bg-primary hover:text-white transition-custom">
                                <i class="fa fa-eye"></i>
                            </button>
                            <button class="bg-white text-dark w-10 h-10 rounded-full flex items-center justify-center hover:bg-primary hover:text-white transition-custom">
                                <i class="fa fa-heart"></i>
                            </button>
                            <button class="bg-white text-dark w-10 h-10 rounded-full flex items-center justify-center hover:bg-primary hover:text-white transition-custom">
                                <i class="fa fa-shopping-cart"></i>
                            </button>
                        </div>
                        <span class="absolute top-4 left-4 bg-primary text-white text-sm font-medium px-3 py-1 rounded-full">New</span>
                    </div>
                    <div class="p-4">
                        <h3 class="font-semibold text-lg mb-1">Urban Mesh Runner</h3>
                        <div class="flex items-center mb-2">
                            <div class="flex text-yellow-400">
                                <i class="fa fa-star"></i>
                                <i class="fa fa-star"></i>
                                <i class="fa fa-star"></i>
                                <i class="fa fa-star"></i>
                                <i class="fa fa-star-half-o"></i>
                            </div>
                            <span class="text-gray-500 text-sm ml-2">(42)</span>
                        </div>
                        <p class="text-gray-600 text-sm mb-3">Lightweight breathable mesh design</p>
                        <div class="flex justify-between items-center">
                            <span class="font-bold text-lg">$89.99</span>
                            <div class="flex space-x-1">
                                <span class="w-4 h-4 rounded-full bg-primary border border-gray-300 cursor-pointer hover:scale-110 transition-custom"></span>
                                <span class="w-4 h-4 rounded-full bg-dark border border-gray-300 cursor-pointer hover:scale-110 transition-custom"></span>
                                <span class="w-4 h-4 rounded-full bg-white border border-gray-300 cursor-pointer hover:scale-110 transition-custom"></span>
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- Product 2 -->
                <div class="product-card hover-lift bg-white rounded-xl overflow-hidden shadow-md">
                    <div class="relative group">
                        <img src="https://picsum.photos/id/21/800/800" alt="Outdoor hiking sneakers" class="w-full h-64 object-cover">
                        <div class="absolute inset-0 bg-primary/20 opacity-0 group-hover:opacity-100 transition-custom flex items-center justify-center gap-3">
                            <button class="bg-white text-dark w-10 h-10 rounded-full flex items-center justify-center hover:bg-primary hover:text-white transition-custom">
                                <i class="fa fa-eye"></i>
                            </button>
                            <button class="bg-white text-dark w-10 h-10 rounded-full flex items-center justify-center hover:bg-primary hover:text-white transition-custom">
                                <i class="fa fa-heart"></i>
                            </button>
                            <button class="bg-white text-dark w-10 h-10 rounded-full flex items-center justify-center hover:bg-primary hover:text-white transition-custom">
                                <i class="fa fa-shopping-cart"></i>
                            </button>
                        </div>
                    </div>
                    <div class="p-4">
                        <h3 class="font-semibold text-lg mb-1">Trail Explorer</h3>
                        <div class="flex items-center mb-2">
                            <div class="flex text-yellow-400">
                                <i class="fa fa-star"></i>
                                <i class="fa fa-star"></i>
                                <i class="fa fa-star"></i>
                                <i class="fa fa-star"></i>
                                <i class="fa fa-star-o"></i>
                            </div>
                            <span class="text-gray-500 text-sm ml-2">(28)</span>
                        </div>
                        <p class="text-gray-600 text-sm mb-3">Durable outdoor performance design</p>
                        <div class="flex justify-between items-center">
                            <span class="font-bold text-lg">$109.99</span>
                            <div class="flex space-x-1">
                                <span class="w-4 h-4 rounded-full bg-dark border border-gray-300 cursor-pointer hover:scale-110 transition-custom"></span>
                                <span class="w-4 h-4 rounded-full bg-gray-400 border border-gray-300 cursor-pointer hover:scale-110 transition-custom"></span>
                                <span class="w-4 h-4 rounded-full bg-green-700 border border-gray-300 cursor-pointer hover:scale-110 transition-custom"></span>
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- Product 3 -->
                <div class="product-card hover-lift bg-white rounded-xl overflow-hidden shadow-md">
                    <div class="relative group">
                        <img src="https://picsum.photos/id/1059/800/800" alt="Stylish casual mesh sneakers" class="w-full h-64 object-cover">
                        <div class="absolute inset-0 bg-primary/20 opacity-0 group-hover:opacity-100 transition-custom flex items-center justify-center gap-3">
                            <button class="bg-white text-dark w-10 h-10 rounded-full flex items-center justify-center hover:bg-primary hover:text-white transition-custom">
                                <i class="fa fa-eye"></i>
                            </button>
                            <button class="bg-white text-dark w-10 h-10 rounded-full flex items-center justify-center hover:bg-primary hover:text-white transition-custom">
                                <i class="fa fa-heart"></i>
                            </button>
                            <button class="bg-white text-dark w-10 h-10 rounded-full flex items-center justify-center hover:bg-primary hover:text-white transition-custom">
                                <i class="fa fa-shopping-cart"></i>
                            </button>
                        </div>
                        <span class="absolute top-4 left-4 bg-red-500 text-white text-sm font-medium px-3 py-1 rounded-full">-15%</span>
                    </div>
                    <div class="p-4">
                        <h3 class="font-semibold text-lg mb-1">Metro Casual</h3>
                        <div class="flex items-center mb-2">
                            <div class="flex text-yellow-400">
                                <i class="fa fa-star"></i>
                                <i class="fa fa-star"></i>
                                <i class="fa fa-star"></i>
                                <i class="fa fa-star"></i>
                                <i class="fa fa-star"></i>
                            </div>
                            <span class="text-gray-500 text-sm ml-2">(56)</span>
                        </div>
                        <p class="text-gray-600 text-sm mb-3">Sleek design with breathable mesh</p>
                        <div class="flex justify-between items-center">
                            <div>
                                <span class="font-bold text-lg">$74.99</span>
                                <span class="text-gray-500 text-sm line-through ml-2">$89.99</span>
                            </div>
                            <div class="flex space-x-1">
                                <span class="w-4 h-4 rounded-full bg-white border border-gray-300 cursor-pointer hover:scale-110 transition-custom"></span>
                                <span class="w-4 h-4 rounded-full bg-primary border border-gray-300 cursor-pointer hover:scale-110 transition-custom"></span>
                                <span class="w-4 h-4 rounded-full bg-gray-200 border border-gray-300 cursor-pointer hover:scale-110 transition-custom"></span>
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- Product 4 -->
                <div class="product-card hover-lift bg-white rounded-xl overflow-hidden shadow-md">
                    <div class="relative group">
                        <img src="https://picsum.photos/id/1058/800/800" alt="Waterproof outdoor sneakers" class="w-full h-64 object-cover">
                        <div class="absolute inset-0 bg-primary/20 opacity-0 group-hover:opacity-100 transition-custom flex items-center justify-center gap-3">
                            <button class="bg-white text-dark w-10 h-10 rounded-full flex items-center justify-center hover:bg-primary hover:text-white transition-custom">
                                <i class="fa fa-eye"></i>
                            </button>
                            <button class="bg-white text-dark w-10 h-10 rounded-full flex items-center justify-center hover:bg-primary hover:text-white transition-custom">
                                <i class="fa fa-heart"></i>
                            </button>
                            <button class="bg-white text-dark w-10 h-10 rounded-full flex items-center justify-center hover:bg-primary hover:text-white transition-custom">
                                <i class="fa fa-shopping-cart"></i>
                            </button>
                        </div>
                    </div>
                    <div class="p-4">
                        <h3 class="font-semibold text-lg mb-1">Terrain Master</h3>
                        <div class="flex items-center mb-2">
                            <div class="flex text-yellow-400">
                                <i class="fa fa-star"></i>
                                <i class="fa fa-star"></i>
                                <i class="fa fa-star"></i>
                                <i class="fa fa-star-half-o"></i>
                                <i class="fa fa-star-o"></i>
                            </div>
                            <span class="text-gray-500 text-sm ml-2">(34)</span>
                        </div>
                        <p class="text-gray-600 text-sm mb-3">Waterproof outdoor performance</p>
                        <div class="flex justify-between items-center">
                            <span class="font-bold text-lg">$129.99</span>
                            <div class="flex space-x-1">
                                <span class="w-4 h-4 rounded-full bg-gray-800 border border-gray-300 cursor-pointer hover:scale-110 transition-custom"></span>
                                <span class="w-4 h-4 rounded-full bg-brown-600 border border-gray-300 cursor-pointer hover:scale-110 transition-custom"></span>
                                <span class="w-4 h-4 rounded-full bg-blue-900 border border-gray-300 cursor-pointer hover:scale-110 transition-custom"></span>
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- Product 5 -->
                <div class="product-card hover-lift bg-white rounded-xl overflow-hidden shadow-md">
                    <div class="relative group">
                        <img src="https://picsum.photos/id/1060/800/800" alt="Light blue mesh sneakers" class="w-full h-64 object-cover">
                        <div class="absolute inset-0 bg-primary/20 opacity-0 group-hover:opacity-100 transition-custom flex items-center justify-center gap-3">
                            <button class="bg-white text-dark w-10 h-10 rounded-full flex items-center justify-center hover:bg-primary hover:text-white transition-custom">
                                <i class="fa fa-eye"></i>
                            </button>
                            <button class="bg-white text-dark w-10 h-10 rounded-full flex items-center justify-center hover:bg-primary hover:text-white transition-custom">
                                <i class="fa fa-heart"></i>
                            </button>
                            <button class="bg-white text-dark w-10 h-10 rounded-full flex items-center justify-center hover:bg-primary hover:text-white transition-custom">
                                <i class="fa fa-shopping-cart"></i>
                            </button>
                        </div>
                    </div>
                    <div class="p-4">
                        <h3 class="font-semibold text-lg mb-1">Aero Mesh</h3>
                        <div class="flex items-center mb-2">
                            <div class="flex text-yellow-400">
                                <i class="fa fa-star"></i>
                                <i class="fa fa-star"></i>
                                <i class="fa fa-star"></i>
                                <i class="fa fa-star"></i>
                                <i class="fa fa-star-o"></i>
                            </div>
                            <span class="text-gray-500 text-sm ml-2">(29)</span>
                        </div>
                        <p class="text-gray-600 text-sm mb-3">Ultra-light breathable construction</p>
                        <div class="flex justify-between items-center">
                            <span class="font-bold text-lg">$84.99</span>
                            <div class="flex space-x-1">
                                <span class="w-4 h-4 rounded-full bg-primary border border-gray-300 cursor-pointer hover:scale-110 transition-custom"></span>
                                <span class="w-4 h-4 rounded-full bg-white border border-gray-300 cursor-pointer hover:scale-110 transition-custom"></span>
                                <span class="w-4 h-4 rounded-full bg-dark border border-gray-300 cursor-pointer hover:scale-110 transition-custom"></span>
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- Product 6 -->
                <div class="product-card hover-lift bg-white rounded-xl overflow-hidden shadow-md">
                    <div class="relative group">
                        <img src="https://picsum.photos/id/1062/800/800" alt="Black and white casual sneakers" class="w-full h-64 object-cover">
                        <div class="absolute inset-0 bg-primary/20 opacity-0 group-hover:opacity-100 transition-custom flex items-center justify-center gap-3">
                            <button class="bg-white text-dark w-10 h-10 rounded-full flex items-center justify-center hover:bg-primary hover:text-white transition-custom">
                                <i class="fa fa-eye"></i>
                            </button>
                            <button class="bg-white text-dark w-10 h-10 rounded-full flex items-center justify-center hover:bg-primary hover:text-white transition-custom">
                                <i class="fa fa-heart"></i>
                            </button>
                            <button class="bg-white text-dark w-10 h-10 rounded-full flex items-center justify-center hover:bg-primary hover:text-white transition-custom">
                                <i class="fa fa-shopping-cart"></i>
                            </button>
                        </div>
                        <span class="absolute top-4 left-4 bg-red-500 text-white text-sm font-medium px-3 py-1 rounded-full">-20%</span>
                    </div>
                    <div class="p-4">
                        <h3 class="font-semibold text-lg mb-1">Urban Edge</h3>
                        <div class="flex items-center mb-2">
                            <div class="flex text-yellow-400">
                                <i class="fa fa-star"></i>
                                <i class="fa fa-star"></i>
                                <i class="fa fa-star"></i>
                                <i class="fa fa-star"></i>
                                <i class="fa fa-star-half-o"></i>
                            </div>
                            <span class="text-gray-500 text-sm ml-2">(63)</span>
                        </div>
                        <p class="text-gray-600 text-sm mb-3">Stylish monochrome urban design</p>
                        <div class="flex justify-between items-center">
                            <div>
                                <span class="font-bold text-lg">$71.99</span>
                                <span class="text-gray-500 text-sm line-through ml-2">$89.99</span>
                            </div>
                            <div class="flex space-x-1">
                                <span class="w-4 h-4 rounded-full bg-white border border-gray-300 cursor-pointer hover:scale-110 transition-custom"></span>
                                <span class="w-4 h-4 rounded-full bg-dark border border-gray-300 cursor-pointer hover:scale-110 transition-custom"></span>
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- Product 7 -->
                <div class="product-card hover-lift bg-white rounded-xl overflow-hidden shadow-md">
                    <div class="relative group">
                        <img src="https://picsum.photos/id/1071/800/800" alt="Hiking boots for outdoor activities" class="w-full h-64 object-cover">
                        <div class="absolute inset-0 bg-primary/20 opacity-0 group-hover:opacity-100 transition-custom flex items-center justify-center gap-3">
                            <button class="bg-white text-dark w-10 h-10 rounded-full flex items-center justify-center hover:bg-primary hover:text-white transition-custom">
                                <i class="fa fa-eye"></i>
                            </button>
                            <button class="bg-white text-dark w-10 h-10 rounded-full flex items-center justify-center hover:bg-primary hover:text-white transition-custom">
                                <i class="fa fa-heart"></i>
                            </button>
                            <button class="bg-white text-dark w-10 h-10 rounded-full flex items-center justify-center hover:bg-primary hover:text-white transition-custom">
                                <i class="fa fa-shopping-cart"></i>
                            </button>
                        </div>
                    </div>
                    <div class="p-4">
                        <h3 class="font-semibold text-lg mb-1">Alpine Trekker</h3>
                        <div class="flex items-center mb-2">
                            <div class="flex text-yellow-400">
                                <i class="fa fa-star"></i>
                                <i class="fa fa-star"></i>
                                <i class="fa fa-star"></i>
                                <i class="fa fa-star"></i>
                                <i class="fa fa-star-o"></i>
                            </div>
                            <span class="text-gray-500 text-sm ml-2">(18)</span>
                        </div>
                        <p class="text-gray-600 text-sm mb-3">Rugged outdoor trekking design</p>
                        <div class="flex justify-between items-center">
                            <span class="font-bold text-lg">$139.99</span>
                            <div class="flex space-x-1">
                                <span class="w-4 h-4 rounded-full bg-brown-700 border border-gray-300 cursor-pointer hover:scale-110 transition-custom"></span>
                                <span class="w-4 h-4 rounded-full bg-gray-600 border border-gray-300 cursor-pointer hover:scale-110 transition-custom"></span>
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- Product 8 -->
                <div class="product-card hover-lift bg-white rounded-xl overflow-hidden shadow-md">
                    <div class="relative group">
                        <img src="https://picsum.photos/id/1072/800/800" alt="Lightweight running sneakers" class="w-full h-64 object-cover">
                        <div class="absolute inset-0 bg-primary/20 opacity-0 group-hover:opacity-100 transition-custom flex items-center justify-center gap-3">
                            <button class="bg-white text-dark w-10 h-10 rounded-full flex items-center justify-center hover:bg-primary hover:text-white transition-custom">
                                <i class="fa fa-eye"></i>
                            </button>
                            <button class="bg-white text-dark w-10 h-10 rounded-full flex items-center justify-center hover:bg-primary hover:text-white transition-custom">
                                <i class="fa fa-heart"></i>
                            </button>
                            <button class="bg-white text-dark w-10 h-10 rounded-full flex items-center justify-center hover:bg-primary hover:text-white transition-custom">
                                <i class="fa fa-shopping-cart"></i>
                            </button>
                        </div>
                        <span class="absolute top-4 left-4 bg-primary text-white text-sm font-medium px-3 py-1 rounded-full">Trending</span>
                    </div>
                    <div class="p-4">
                        <h3 class="font-semibold text-lg mb-1">Velocity Sprint</h3>
                        <div class="flex items-center mb-2">
                            <div class="flex text-yellow-400">
                                <i class="fa fa-star"></i>
                                <i class="fa fa-star"></i>
                                <i class="fa fa-star"></i>
                                <i class="fa fa-star"></i>
                                <i class="fa fa-star"></i>
                            </div>
                            <span class="text-gray-500 text-sm ml-2">(78)</span>
                        </div>
                        <p class="text-gray-600 text-sm mb-3">High-performance running technology</p>
                        <div class="flex justify-between items-center">
                            <span class="font-bold text-lg">$99.99</span>
                            <div class="flex space-x-1">
                                <span class="w-4 h-4 rounded-full bg-primary border border-gray-300 cursor-pointer hover:scale-110 transition-custom"></span>
                                <span class="w-4 h-4 rounded-full bg-red-500 border border-gray-300 cursor-pointer hover:scale-110 transition-custom"></span>
                                <span class="w-4 h-4 rounded-full bg-dark border border-gray-300 cursor-pointer hover:scale-110 transition-custom"></span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="text-center mt-12">
                <a href="#" class="inline-block bg-dark hover:bg-primary text-white font-medium px-8 py-3 rounded-full transition-custom hover-lift">
                    View All Products
                </a>
            </div>
        </div>
    </section>

    <!-- Features Section -->
    <section id="features" class="py-20 bg-white">
        <div class="container mx-auto px-4">
            <div class="text-center mb-16">
                <h2 class="text-[clamp(1.5rem,3vw,2.5rem)] font-bold mb-4">Why Choose Our Sneakers</h2>
                <p class="text-gray-600 max-w-2xl mx-auto">Designed with premium materials and advanced technology for ultimate comfort and performance.</p>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
                <!-- Feature 1 -->
                <div class="hover-lift bg-light p-6 rounded-xl text-center">
                    <div class="w-16 h-16 bg-primary/10 rounded-full flex items-center justify-center mx-auto mb-6">
                        <i class="fa fa-bolt text-primary text-2xl"></i>
                    </div>
                    <h3 class="font-semibold text-xl mb-3">Lightweight Design</h3>
                    <p class="text-gray-600">Our mesh technology creates ultra-lightweight sneakers that feel like you're walking on air.</p>
                </div>
                
                <!-- Feature 2 -->
                <div class="hover-lift bg-light p-6 rounded-xl text-center">
                    <div class="w-16 h-16 bg-primary/10 rounded-full flex items-center justify-center mx-auto mb-6">
                        <i class="fa fa-tint text-primary text-2xl"></i>
                    </div>
                    <h3 class="font-semibold text-xl mb-3">Water Resistance</h3>
                    <p class="text-gray-600">Advanced materials protect against water while maintaining breathability for outdoor adventures.</p>
                </div>
                
                <!-- Feature 3 -->
                <div class="hover-lift bg-light p-6 rounded-xl text-center">
                    <div class="w-16 h-16 bg-primary/10 rounded-full flex items-center justify-center mx-auto mb-6">
                        <i class="fa fa-shield text-primary text-2xl"></i>
                    </div>
                    <h3 class="font-semibold text-xl mb-3">Durable Construction</h3>
                    <p class="text-gray-600">Reinforced soles and premium materials ensure long-lasting performance in any environment.</p>
                </div>
                
                <!-- Feature 4 -->
                <div class="hover-lift bg-light p-6 rounded-xl text-center">
                    <div class="w-16 h-16 bg-primary/10 rounded-full flex items-center justify-center mx-auto mb-6">
                        <i class="fa fa-leaf text-primary text-2xl"></i>
                    </div>
                    <h3 class="font-semibold text-xl mb-3">Eco-Friendly</h3>
                    <p class="text-gray-600">Sustainably sourced materials and responsible manufacturing processes reduce environmental impact.</p>
                </div>
            </div>
            
            <div class="mt-20 grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
                <div class="order-2 lg:order-1">
                    <h3 class="text-[clamp(1.25rem,2.5vw,2rem)] font-bold mb-6">Engineered for Maximum Comfort</h3>
                    <p class="text-gray-600 mb-6">Our sneakers combine ergonomic design with advanced cushioning technology to provide all-day comfort, whether you're navigating city streets or exploring mountain trails.</p>
                    
                    <div class="space-y-4 mb-8">
                        <div class="flex items-start">
                            <div class="mt-1 mr-4 text-primary">
                                <i class="fa fa-check-circle"></i>
                            </div>
                            <div>
                                <h4 class="font-medium text-lg">Adaptive Fit Technology</h4>
                                <p class="text-gray-600">Customizable fit that adapts to your foot shape over time.</p>
                            </div>
                        </div>
                        <div class="flex items-start">
                            <div class="mt-1 mr-4 text-primary">
                                <i class="fa fa-check-circle"></i>
                            </div>
                            <div>
                                <h4 class="font-medium text-lg">Shock Absorption</h4>
                                <p class="text-gray-600">Advanced midsole technology reduces impact on joints.</p>
                            </div>
                        </div>
                        <div class="flex items-start">
                            <div class="mt-1 mr-4 text-primary">
                                <i class="fa fa-check-circle"></i>
                            </div>
                            <div>
                                <h4 class="font-medium text-lg">Breathable Mesh</h4>
                                <p class="text-gray-600">Maximum airflow to keep feet cool and dry in any conditions.</p>
                            </div>
                        </div>
                    </div>
                    
                    <a href="#collection" class="inline-block bg-primary hover:bg-primary/90 text-white font-medium px-8 py-3 rounded-full transition-custom hover-lift">
                        Shop Now
                    </a>
                </div>
                
                <div class="order-1 lg:order-2 relative">
                    <img src="https://picsum.photos/id/1069/800/1000" alt="Sneaker comfort technology demonstration" class="w-full h-auto rounded-xl shadow-xl">
                    <div class="absolute -bottom-6 -left-6 bg-white p-4 rounded-xl shadow-lg max-w-xs">
                        <div class="flex items-center mb-2">
                            <div class="flex text-yellow-400">
                                <i class="fa fa-star"></i>
                                <i class="fa fa-star"></i>
                                <i class="fa fa-star"></i>
                                <i class="fa fa-star"></i>
                                <i class="fa fa-star"></i>
                            </div>
                            <span class="text-gray-500 text-sm ml-2">5.0 Rating</span>
                        </div>
                        <p class="text-gray-700 italic">"The most comfortable sneakers I've ever owned. I can wear them all day without any discomfort."</p>
                        <p class="font-medium mt-2">— Sarah J.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Reviews Section -->
    <section id="reviews" class="py-20 bg-light">
        <div class="container mx-auto px-4">
            <div class="text-center mb-16">
                <h2 class="text-[clamp(1.5rem,3vw,2.5rem)] font-bold mb-4">What Our Customers Say</h2>
                <p class="text-gray-600 max-w-2xl mx-auto">Read genuine reviews from people who have experienced our sneakers in their daily lives.</p>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Review 1 -->
                <div class="hover-lift bg-white p-6 rounded-xl shadow-md">
                    <div class="flex text-yellow-400 mb-4">
                        <i class="fa fa-star"></i>
                        <i class="fa fa-star"></i>
                        <i class="fa fa-star"></i>
                        <i class="fa fa-star"></i>
                        <i class="fa fa-star"></i>
                    </div>
                    <p class="text-gray-600 mb-6">"I've been using the Urban Mesh Runners for my daily commute and they're perfect. Lightweight, stylish, and incredibly comfortable even after 12 hours of wear."</p>
                    <div class="flex items-center">
                        <img src="https://picsum.photos/id/1012/100/100" alt="Customer profile" class="w-12 h-12 rounded-full object-cover mr-4">
                        <div>
                            <h4 class="font-medium">Michael T.</h4>
                            <p class="text-gray-500 text-sm">New York, USA</p>
                        </div>
                    </div>
                </div>
                
                <!-- Review 2 -->
                <div class="hover-lift bg-white p-6 rounded-xl shadow-md">
                    <div class="flex text-yellow-400 mb-4">
                        <i class="fa fa-star"></i>
                        <i class="fa fa-star"></i>
                        <i class="fa fa-star"></i>
                        <i class="fa fa-star"></i>
                        <i class="fa fa-star-half-o"></i>
                    </div>
                    <p class="text-gray-600 mb-6">"The Trail Explorer sneakers exceeded my expectations on a recent hiking trip. They provided excellent grip on wet surfaces and kept my feet dry throughout the adventure."</p>
                    <div class="flex items-center">
                        <img src="https://picsum.photos/id/1027/100/100" alt="Customer profile" class="w-12 h-12 rounded-full object-cover mr-4">
                        <div>
                            <h4 class="font-medium">Emma L.</h4>
                            <p class="text-gray-500 text-sm">Colorado, USA</p>
                        </div>
                    </div>
                </div>
                
                <!-- Review 3 -->
                <div class="hover-lift bg-white p-6 rounded-xl shadow-md">
                    <div class="flex text-yellow-400 mb-4">
                        <i class="fa fa-star"></i>
                        <i class="fa fa-star"></i>
                        <i class="fa fa-star"></i>
                        <i class="fa fa-star"></i>
                        <i class="fa fa-star"></i>
                    </div>
                    <p class="text-gray-600 mb-6">"I love my Metro Casual sneakers! They're versatile enough to wear with jeans or shorts, and the breathable mesh keeps my feet cool even in hot weather. Worth every penny!"</p>
                    <div class="flex items-center">
                        <img src="https://picsum.photos/id/1025/100/100" alt="Customer profile" class="w-12 h-12 rounded-full object-cover mr-4">
                        <div>
                            <h4 class="font-medium">David K.</h4>
                            <p class="text-gray-500 text-sm">California, USA</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Newsletter Section -->
    <section class="py-16 bg-primary relative overflow-hidden">
        <div class="absolute inset-0 opacity-10">
            <img src="https://picsum.photos/id/1048/1920/600" alt="Background pattern" class="w-full h-full object-cover">
        </div>
        
        <div class="container mx-auto px-4 relative z-10">
            <div class="max-w-3xl mx-auto text-center">
                <h2 class="text-[clamp(1.5rem,3vw,2.25rem)] font-bold text-white mb-4">Join Our Newsletter</h2>
                <p class="text-white/80 mb-8">Subscribe to receive updates on new arrivals, exclusive offers, and sneaker care tips.</p>
                
                <form class="flex flex-col sm:flex-row gap-4 max-w-xl mx-auto">
                    <input type="email" placeholder="Your email address" class="flex-grow px-6 py-3 rounded-full focus:outline-none focus:ring-2 focus:ring-white">
                    <button type="submit" class="bg-dark hover:bg-dark/80 text-white font-medium px-8 py-3 rounded-full transition-custom hover-lift whitespace-nowrap">
                        Subscribe Now
                    </button>
                </form>
                
                <p class="text-white/60 text-sm mt-4">We respect your privacy. Unsubscribe at any time.</p>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="py-20 bg-white">
        <div class="container mx-auto px-4">
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-12">
                <div>
                    <h2 class="text-[clamp(1.5rem,3vw,2.5rem)] font-bold mb-4">Get In Touch</h2>
                    <p class="text-gray-600 mb-8">Have questions about our products or need assistance? We're here to help.</p>
                    
                    <div class="space-y-6 mb-8">
                        <div class="flex items-start">
                            <div class="w-12 h-12 bg-primary/10 rounded-full flex items-center justify-center mr-4 flex-shrink-0">
                                <i class="fa fa-map-marker text-primary"></i>
                            </div>
                            <div>
                                <h4 class="font-medium text-lg mb-1">Visit Our Store</h4>
                                <p class="text-gray-600">123 Sneaker Street, New York, NY 10001, United States</p>
                            </div>
                        </div>
                        
                        <div class="flex items-start">
                            <div class="w-12 h-12 bg-primary/10 rounded-full flex items-center justify-center mr-4 flex-shrink-0">
                                <i class="fa fa-phone text-primary"></i>
                            </div>
                            <div>
                                <h4 class="font-medium text-lg mb-1">Call Us</h4>
                                <p class="text-gray-600">+1 (555) 123-4567</p>
                                <p class="text-gray-500 text-sm">Mon-Fri, 9:00 AM - 6:00 PM EST</p>
                            </div>
                        </div>
                        
                        <div class="flex items-start">
                            <div class="w-12 h-12 bg-primary/10 rounded-full flex items-center justify-center mr-4 flex-shrink-0">
                                <i class="fa fa-envelope text-primary"></i>
                            </div>
                            <div>
                                <h4 class="font-medium text-lg mb-1">Email Us</h4>
                                <p class="text-gray-600">info@sneakercollection.com</p>
                                <p class="text-gray-500 text-sm">We respond within 24 hours</p>
                            </div>
                        </div>
                    </div>
                    
                    <div>
                        <h4 class="font-medium text-lg mb-4">Follow Us</h4>
                        <div class="flex space-x-4">
                            <a href="#" class="w-10 h-10 bg-primary/10 hover:bg-primary hover:text-white text-primary rounded-full flex items-center justify-center transition-custom">
                                <i class="fa fa-facebook"></i>
                            </a>
                            <a href="#" class="w-10 h-10 bg-primary/10 hover:bg-primary hover:text-white text-primary rounded-full flex items-center justify-center transition-custom">
                                <i class="fa fa-twitter"></i>
                            </a>
                            <a href="#" class="w-10 h-10 bg-primary/10 hover:bg-primary hover:text-white text-primary rounded-full flex items-center justify-center transition-custom">
                                <i class="fa fa-instagram"></i>
                            </a>
                            <a href="#" class="w-10 h-10 bg-primary/10 hover:bg-primary hover:text-white text-primary rounded-full flex items-center justify-center transition-custom">
                                <i class="fa fa-youtube-play"></i>
                            </a>
                        </div>
                    </div>
                </div>
                
                <div>
                    <form class="bg-light p-8 rounded-xl">
                        <h3 class="text-xl font-bold mb-6">Send Us a Message</h3>
                        
                        <div class="grid grid-cols-1 sm:grid-cols-2 gap-6 mb-6">
                            <div>
                                <label for="name" class="block text-gray-700 font-medium mb-2">Your Name</label>
                                <input type="text" id="name" class="w-full px-4 py-3 rounded-lg border border-gray-300 focus:outline-none focus:ring-2 focus:ring-primary focus:border-transparent">
                            </div>
                            
                            <div>
                                <label for="email" class="block text-gray-700 font-medium mb-2">Your Email</label>
                                <input type="email" id="email" class="w-full px-4 py-3 rounded-lg border border-gray-300 focus:outline-none focus:ring-2 focus:ring-primary focus:border-transparent">
                            </div>
                        </div>
                        
                        <div class="mb-6">
                            <label for="subject" class="block text-gray-700 font-medium mb-2">Subject</label>
                            <input type="text" id="subject" class="w-full px-4 py-3 rounded-lg border border-gray-300 focus:outline-none focus:ring-2 focus:ring-primary focus:border-transparent">
                        </div>
                        
                        <div class="mb-6">
                            <label for="message" class="block text-gray-700 font-medium mb-2">Your Message</label>
                            <textarea id="message" rows="5" class="w-full px-4 py-3 rounded-lg border border-gray-300 focus:outline-none focus:ring-2 focus:ring-primary focus:border-transparent"></textarea>
                        </div>
                        
                        <button type="submit" class="w-full bg-primary hover:bg-primary/90 text-white font-medium px-6 py-3 rounded-lg transition-custom hover-lift">
                            Send Message
                        </button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-dark text-white pt-16 pb-8">
        <div class="container mx-auto px-4">
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8 mb-12">
                <div>
                    <h3 class="text-2xl font-bold mb-6">STEP</h3>
                    <p class="text-gray-400 mb-6">Premium sneakers designed for style, comfort, and performance in any environment.</p>
                    <div class="flex space-x-4">
                        <a href="#" class="text-gray-400 hover:text-primary transition-custom">
                            <i class="fa fa-facebook"></i>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-primary transition-custom">
                            <i class="fa fa-twitter"></i>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-primary transition-custom">
                            <i class="fa fa-instagram"></i>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-primary transition-custom">
                            <i class="fa fa-youtube-play"></i>
                        </a>
                    </div>
                </div>
                
                <div>
                    <h4 class="text-lg font-semibold mb-6">Shop</h4>
                    <ul class="space-y-3">
                        <li><a href="#" class="text-gray-400 hover:text-primary transition-custom">Mesh Sneakers</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-primary transition-custom">Outdoor Collection</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-primary transition-custom">Casual Styles</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-primary transition-custom">New Arrivals</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-primary transition-custom">Sale Items</a></li>
                    </ul>
                </div>
                
                <div>
                    <h4 class="text-lg font-semibold mb-6">Help</h4>
                    <ul class="space-y-3">
                        <li><a href="#" class="text-gray-400 hover:text-primary transition-custom">Customer Service</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-primary transition-custom">FAQs</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-primary transition-custom">Shipping & Returns</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-primary transition-custom">Size Guide</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-primary transition-custom">Contact Us</a></li>
                    </ul>
                </div>
                
                <div>
                    <h4 class="text-lg font-semibold mb-6">About</h4>
                    <ul class="space-y-3">
                        <li><a href="#" class="text-gray-400 hover:text-primary transition-custom">Our Story</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-primary transition-custom">Sustainability</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-primary transition-custom">Materials & Technology</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-primary transition-custom">Careers</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-primary transition-custom">Press</a></li>
                    </ul>
                </div>
            </div>
            
            <div class="border-t border-gray-800 pt-8">
                <div class="flex flex-col md:flex-row justify-between items-center">
                    <p class="text-gray-500 text-sm mb-4 md:mb-0">© 2023 STEP. All rights reserved.</p>
                    <div class="flex space-x-6">
                        <a href="#" class="text-gray-500 hover:text-primary text-sm transition-custom">Privacy Policy</a>
                        <a href="#" class="text-gray-500 hover:text-primary text-sm transition-custom">Terms of Service</a>
                        <a href="#" class="text-gray-500 hover:text-primary text-sm transition-custom">Cookie Policy</a>
                    </div>
                </div>
            </div>
        </div>
    </footer>

    <!-- Back to Top Button -->
    <button id="backToTop" class="fixed bottom-8 right-8 bg-primary text-white w-12 h-12 rounded-full flex items-center justify-center shadow-lg opacity-0 invisible transition-all duration-300 z-50 hover:bg-primary/90">
        <i class="fa fa-chevron-up"></i>
    </button>

    <script>
        // Navbar scroll effect
        const navbar = document.getElementById('navbar');
        const scrollIndicator = document.getElementById('scrollIndicator');
        
        window.addEventListener('scroll', function() {
            if (window.scrollY > 50) {
                navbar.classList.add('bg-dark', 'shadow-md');
                navbar.classList.remove('bg-transparent');
            } else {
                navbar.classList.remove('bg-dark', 'shadow-md');
                navbar.classList.add('bg-transparent');
            }
            
            // Update scroll indicator
            const winScroll = document.body.scrollTop || document.documentElement.scrollTop;
            const height = document.documentElement.scrollHeight - document.documentElement.clientHeight;
            const scrolled = (winScroll / height) * 100;
            scrollIndicator.style.width = scrolled + "%";
            
            // Back to top button visibility
            const backToTopBtn = document.getElementById('backToTop');
            if (window.scrollY > 300) {
                backToTopBtn.classList.remove('opacity-0', 'invisible');
                backToTopBtn.classList.add('opacity-100', 'visible');
            } else {
                backToTopBtn.classList.add('opacity-0', 'invisible');
                backToTopBtn.classList.remove('opacity-100', 'visible');
            }
        });
        
        // Mobile menu toggle
        const mobileMenuBtn = document.getElementById('mobileMenuBtn');
        const mobileMenu = document.getElementById('mobileMenu');
        
        mobileMenuBtn.addEventListener('click', function() {
            if (mobileMenu.classList.contains('opacity-0')) {
                mobileMenu.classList.remove('opacity-0', '-translate-y-full', 'pointer-events-none');
                mobileMenu.classList.add('opacity-100', 'translate-y-0', 'pointer-events-auto');
                mobileMenuBtn.innerHTML = '<i class="fa fa-times"></i>';
            } else {
                mobileMenu.classList.add('opacity-0', '-translate-y-full', 'pointer-events-none');
                mobileMenu.classList.remove('opacity-100', 'translate-y-0', 'pointer-events-auto');
                mobileMenuBtn.innerHTML = '<i class="fa fa-bars"></i>';
            }
        });
        
        // Back to top functionality
        document.getElementById('backToTop').addEventListener('click', function() {
            window.scrollTo({
                top: 0,
                behavior: 'smooth'
            });
        });
        
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                // Close mobile menu if open
                if (!mobileMenu.classList.contains('opacity-0')) {
                    mobileMenu.classList.add('opacity-0', '-translate-y-full', 'pointer-events-none');
                    mobileMenu.classList.remove('opacity-100', 'translate-y-0', 'pointer-events-auto');
                    mobileMenuBtn.innerHTML = '<i class="fa fa-bars"></i>';
                }
                
                const targetId = this.getAttribute('href');
                if (targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if (targetElement) {
                    targetElement.scrollIntoView({
                        behavior: 'smooth'
                    });
                }
            });
        });
        
        // Collection filter functionality
        const filterButtons = document.querySelectorAll('.collection-filter');
        
        filterButtons.forEach(button => {
            button.addEventListener('click', function() {
                // Remove active class from all buttons
                filterButtons.forEach(btn => {
                    btn.classList.remove('active', 'bg-primary', 'text-white');
                    btn.classList.add('bg-gray-200');
                });
                
                // Add active class to clicked button
                this.classList.add('active', 'bg-primary', 'text-white');
                this.classList.remove('bg-gray-200');
                
                // Here you would typically filter products based on selection
                // For demo purposes, we're just showing the active state
            });
        });
    </script>
</body>
</html>
    
