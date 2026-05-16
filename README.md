<!DOCTYPE html>
<html lang="bn" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>রাজকীয় চিংড়ি | প্রিমিয়াম চিংড়ি আচার</title>
    
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Hind+Siliguri:wght@300;400;500;600;700&family=Poppins:wght@300;400;500;600&display=swap" rel="stylesheet">
    
    <!-- Font Awesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>

    <!-- Tailwind Configuration -->
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        primary: '#10b981', // Emerald green
                        'primary-dark': '#047857',
                        gold: '#D4AF37', // Luxury Gold
                        'gold-light': '#F3E5AB',
                        dark: '#111827',
                        light: '#f9fafb',
                        whatsapp: '#25D366'
                    },
                    fontFamily: {
                        hind: ['Hind Siliguri', 'sans-serif'],
                        poppins: ['Poppins', 'sans-serif']
                    },
                    boxShadow: {
                        'luxury': '0 20px 40px -15px rgba(16, 185, 129, 0.15)',
                        'glow': '0 0 20px rgba(16, 185, 129, 0.4)',
                        'gold-glow': '0 0 20px rgba(212, 175, 55, 0.4)',
                        'glass': '0 8px 32px 0 rgba(31, 38, 135, 0.07)'
                    },
                    animation: {
                        'float': 'float 6s ease-in-out infinite',
                        'float-delayed': 'float 6s ease-in-out 3s infinite',
                        'spin-slow': 'spin 8s linear infinite',
                        'blob': 'blob 7s infinite',
                        'scroll-vertical': 'scrollVertical 20s linear infinite'
                    },
                    keyframes: {
                        float: {
                            '0%, 100%': { transform: 'translateY(0)' },
                            '50%': { transform: 'translateY(-20px)' },
                        },
                        blob: {
                            '0%': { transform: 'translate(0px, 0px) scale(1)' },
                            '33%': { transform: 'translate(30px, -50px) scale(1.1)' },
                            '66%': { transform: 'translate(-20px, 20px) scale(0.9)' },
                            '100%': { transform: 'translate(0px, 0px) scale(1)' }
                        },
                        scrollVertical: {
                            '0%': { transform: 'translateY(0)' },
                            '100%': { transform: 'translateY(-50%)' }
                        }
                    }
                }
            }
        }
    </script>

    <style>
        /* Base styling */
        body { font-family: 'Hind Siliguri', sans-serif; background-color: #f9fafb; overflow-x: hidden; }
        .font-en { font-family: 'Poppins', sans-serif; }
        
        /* Custom Scrollbar */
        ::-webkit-scrollbar { width: 8px; }
        ::-webkit-scrollbar-track { background: #f1f1f1; }
        ::-webkit-scrollbar-thumb { background: #10b981; border-radius: 10px; }
        ::-webkit-scrollbar-thumb:hover { background: #047857; }

        /* Hide scrollbar for review section but keep functionality */
        .no-scrollbar::-webkit-scrollbar { display: none; }
        .no-scrollbar { -ms-overflow-style: none; scrollbar-width: none; }

        /* Glassmorphism Classes */
        .glass {
            background: rgba(255, 255, 255, 0.85);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border: 1px solid rgba(255, 255, 255, 0.3);
        }

        .glass-dark {
            background: rgba(17, 24, 39, 0.85);
            backdrop-filter: blur(12px);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        /* Loading Screen */
        #loader {
            transition: opacity 0.6s cubic-bezier(0.83, 0, 0.17, 1);
        }

        /* Scroll Reveal Animations */
        .reveal {
            opacity: 0;
            transform: translateY(40px);
            transition: all 0.8s cubic-bezier(0.5, 0, 0, 1);
        }
        .reveal.active {
            opacity: 1;
            transform: translateY(0);
        }

        /* Image Hover Zoom */
        .img-zoom-container { overflow: hidden; }
        .img-zoom-container img {
            transition: transform 0.6s cubic-bezier(0.25, 0.46, 0.45, 0.94);
        }
        .group:hover .img-zoom-container img {
            transform: scale(1.08);
        }

        /* 3D Tilt Effect simulate on hover */
        .hover-tilt { transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275); }
        .hover-tilt:hover { transform: translateY(-10px) scale(1.02); }

        /* FAQ Accordion */
        .faq-answer {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.4s ease-in-out;
        }
        .faq-item.active .faq-answer { max-height: 200px; }
        .faq-item.active .faq-icon { transform: rotate(180deg); }

        /* Cart Sidebar */
        #cart-sidebar {
            transform: translateX(100%);
            transition: transform 0.5s cubic-bezier(0.4, 0, 0.2, 1);
        }
        #cart-sidebar.open { transform: translateX(0); }

        /* Toast Animation */
        @keyframes slideInUp {
            from { transform: translateY(100%); opacity: 0; }
            to { transform: translateY(0); opacity: 1; }
        }
        .toast-enter { animation: slideInUp 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275) forwards; }
    </style>
</head>
<body class="text-dark antialiased selection:bg-primary selection:text-white">

    <!-- Preloader -->
    <div id="loader" class="fixed inset-0 z-[9999] bg-white flex flex-col items-center justify-center">
        <div class="relative w-24 h-24 mb-6">
            <div class="absolute inset-0 border-4 border-primary/20 rounded-full"></div>
            <div class="absolute inset-0 border-4 border-primary rounded-full border-t-transparent animate-spin"></div>
            <div class="absolute inset-0 flex items-center justify-center text-gold text-2xl">
                <i class="fa-solid fa-shrimp"></i>
            </div>
        </div>
        <h2 class="text-2xl font-bold text-dark tracking-wide bg-clip-text text-transparent bg-gradient-to-r from-primary to-gold">রাজকীয় চিংড়ি</h2>
        <p class="text-gray-500 mt-2 font-medium animate-pulse">স্বাদ লোডিং হচ্ছে...</p>
    </div>

    <!-- Sticky Navbar -->
    <nav class="fixed w-full top-0 z-50 glass shadow-glass transition-all duration-300 py-4" id="navbar">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center">
                <!-- Logo -->
                <a href="#" class="flex items-center gap-3 group">
                    <div class="w-10 h-10 rounded-full bg-primary flex items-center justify-center text-white shadow-glow group-hover:rotate-12 transition-transform duration-300">
                        <i class="fa-solid fa-shrimp text-lg"></i>
                    </div>
                    <span class="text-2xl font-bold text-dark group-hover:text-primary transition-colors">রাজকীয়<span class="text-gold">.</span></span>
                </a>

                <!-- Desktop Menu -->
                <div class="hidden md:flex items-center space-x-8">
                    <a href="#home" class="font-medium hover:text-primary transition-colors relative after:absolute after:bottom-0 after:left-0 after:w-0 after:h-0.5 after:bg-primary hover:after:w-full after:transition-all after:duration-300">হোম</a>
                    <a href="#products" class="font-medium hover:text-primary transition-colors relative after:absolute after:bottom-0 after:left-0 after:w-0 after:h-0.5 after:bg-primary hover:after:w-full after:transition-all after:duration-300">আচার সমূহ</a>
                    <a href="#process" class="font-medium hover:text-primary transition-colors relative after:absolute after:bottom-0 after:left-0 after:w-0 after:h-0.5 after:bg-primary hover:after:w-full after:transition-all after:duration-300">প্রস্তুত প্রণালী</a>
                    <a href="#reviews" class="font-medium hover:text-primary transition-colors relative after:absolute after:bottom-0 after:left-0 after:w-0 after:h-0.5 after:bg-primary hover:after:w-full after:transition-all after:duration-300">মতামত</a>
                </div>

                <!-- Icons (Cart & Mobile Menu) -->
                <div class="flex items-center gap-5">
                    <button onclick="toggleCart()" class="relative text-dark hover:text-primary transition-colors p-2 rounded-full hover:bg-primary/10">
                        <i class="fa-solid fa-shopping-bag text-xl"></i>
                        <span id="cart-count" class="absolute top-0 right-0 -mt-1 -mr-1 bg-gold text-white text-xs font-bold rounded-full w-5 h-5 flex items-center justify-center shadow-md font-en">0</span>
                    </button>
                    <button class="md:hidden text-dark text-2xl p-2" onclick="document.getElementById('mobile-menu').classList.toggle('hidden')">
                        <i class="fa-solid fa-bars"></i>
                    </button>
                </div>
            </div>
        </div>

        <!-- Mobile Menu Panel -->
        <div id="mobile-menu" class="hidden md:hidden absolute top-full left-0 w-full glass border-t border-gray-200">
            <div class="px-4 pt-2 pb-6 space-y-3 flex flex-col text-center">
                <a href="#home" class="block py-2 text-lg font-medium hover:text-primary">হোম</a>
                <a href="#products" class="block py-2 text-lg font-medium hover:text-primary">আচার সমূহ</a>
                <a href="#process" class="block py-2 text-lg font-medium hover:text-primary">প্রস্তুত প্রণালী</a>
                <a href="#reviews" class="block py-2 text-lg font-medium hover:text-primary">মতামত</a>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="relative pt-32 pb-20 lg:pt-48 lg:pb-32 overflow-hidden">
        <!-- Background decorative blobs -->
        <div class="absolute top-0 left-[-10%] w-72 h-72 bg-primary/20 rounded-full mix-blend-multiply filter blur-3xl opacity-70 animate-blob"></div>
        <div class="absolute top-0 right-[-10%] w-72 h-72 bg-gold/20 rounded-full mix-blend-multiply filter blur-3xl opacity-70 animate-blob animation-delay-2000"></div>
        <div class="absolute -bottom-32 left-20 w-72 h-72 bg-green-300/20 rounded-full mix-blend-multiply filter blur-3xl opacity-70 animate-blob animation-delay-4000"></div>

        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
            <div class="grid lg:grid-cols-2 gap-12 lg:gap-8 items-center">
                <!-- Hero Text -->
                <div class="reveal">
                    <div class="inline-flex items-center gap-2 px-4 py-2 rounded-full bg-gold/10 text-gold-dark border border-gold/20 mb-6 shadow-sm">
                        <i class="fa-solid fa-star text-sm"></i>
                        <span class="text-sm font-semibold tracking-wide">১০০% অর্গানিক ও ঘরোয়া তৈরি</span>
                    </div>
                    <h1 class="text-5xl lg:text-7xl font-bold leading-tight mb-6 text-dark">
                        খাঁটি স্বাদের<br>
                        <span class="text-transparent bg-clip-text bg-gradient-to-r from-primary to-emerald-400">রাজকীয় চিংড়ি</span><br>
                        আচার
                    </h1>
                    <p class="text-lg text-gray-600 mb-10 max-w-lg leading-relaxed">
                        বাছাই করা তাজা চিংড়ি এবং নিজস্ব রেসিপিতে তৈরি খাঁটি মসলার এক অপূর্ব মিলন। প্রতি লোকমায় অনুভব করুন আভিজাত্য আর তৃপ্তি।
                    </p>
                    <div class="flex flex-wrap gap-4">
                        <a href="#products" class="px-8 py-4 bg-primary text-white font-semibold rounded-full shadow-luxury hover:shadow-glow hover:-translate-y-1 transition-all duration-300 flex items-center gap-2">
                            <i class="fa-solid fa-cart-shopping"></i> অর্ডার করুন
                        </a>
                        <a href="#process" class="px-8 py-4 bg-white text-dark border border-gray-200 font-semibold rounded-full hover:border-primary hover:text-primary shadow-sm hover:-translate-y-1 transition-all duration-300 flex items-center gap-2 group">
                            কীভাবে তৈরি <i class="fa-solid fa-arrow-right group-hover:translate-x-1 transition-transform"></i>
                        </a>
                    </div>
                    
                    <div class="mt-12 flex items-center gap-6 text-sm font-medium text-gray-500">
                        <div class="flex items-center gap-2"><i class="fa-solid fa-truck-fast text-primary text-lg"></i> সারা দেশে ডেলিভারি</div>
                        <div class="flex items-center gap-2"><i class="fa-solid fa-shield-halved text-primary text-lg"></i> ১০০% কোয়ালিটি গ্যারান্টি</div>
                    </div>
                </div>

                <!-- Hero Image -->
                <div class="relative reveal lg:ml-auto">
                    <!-- Decorative circle behind image -->
                    <div class="absolute inset-0 bg-gradient-to-tr from-primary/20 to-gold/20 rounded-full transform scale-105 filter blur-2xl"></div>
                    
                    <!-- Main floating image -->
                    <div class="relative z-10 w-full max-w-md mx-auto">
                        <img src="src=image_7d6921.png.jpeg" alt="Premium Chingri Achar Jar" class="w-full h-auto object-cover rounded-3xl shadow-2xl animate-float border-4 border-white">
                        
                        <!-- Floating Badge 1 -->
                        <div class="absolute -top-6 -right-6 bg-white p-4 rounded-2xl shadow-xl animate-float-delayed glass border-none flex items-center gap-3">
                            <div class="w-10 h-10 rounded-full bg-gold/20 flex items-center justify-center text-gold">
                                <i class="fa-solid fa-thumbs-up"></i>
                            </div>
                            <div>
                                <p class="text-xs text-gray-500 font-medium">কাস্টমার রেটিং</p>
                                <p class="text-dark font-bold">৪.৯/৫.০</p>
                            </div>
                        </div>

                        <!-- Floating Badge 2 -->
                        <div class="absolute -bottom-8 -left-8 bg-white p-4 rounded-2xl shadow-xl animate-float glass border-none flex items-center gap-3">
                            <div class="w-10 h-10 rounded-full bg-primary/20 flex items-center justify-center text-primary">
                                <i class="fa-solid fa-fire"></i>
                            </div>
                            <div>
                                <p class="text-xs text-gray-500 font-medium">বেস্ট সেলার</p>
                                <p class="text-dark font-bold">স্পেশাল ঝাল</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Products Section -->
    <section id="products" class="py-24 bg-white relative">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16 reveal">
                <span class="text-gold font-bold tracking-wider uppercase text-sm mb-2 block">আমাদের আয়োজন</span>
                <h2 class="text-4xl md:text-5xl font-bold text-dark mb-4">সবচেয়ে জনপ্রিয় আচার</h2>
                <div class="w-24 h-1 bg-primary mx-auto rounded-full"></div>
            </div>

            <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8" id="product-container">
                <!-- Products injected via JS, showing static placeholders for structure -->
            </div>
        </div>
    </section>

    <!-- Making Process -->
    <section id="process" class="py-24 bg-dark text-white relative overflow-hidden">
        <!-- Abstract BG patterns -->
        <div class="absolute top-0 right-0 w-full h-full opacity-5" style="background-image: radial-gradient(#10b981 1px, transparent 1px); background-size: 30px 30px;"></div>
        
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
            <div class="text-center mb-16 reveal">
                <span class="text-primary font-bold tracking-wider text-sm mb-2 block">প্রস্তুত প্রণালী</span>
                <h2 class="text-4xl md:text-5xl font-bold mb-4">যেভাবে তৈরি হয় আমাদের আচার</h2>
                <p class="text-gray-400 max-w-2xl mx-auto">সম্পূর্ণ স্বাস্থ্যকর ও ঘরোয়া পরিবেশে প্রতিটি ধাপ নিপুণভাবে সম্পন্ন করা হয়।</p>
            </div>

            <div class="grid md:grid-cols-3 gap-8 relative">
                <!-- Connecting Line -->
                <div class="hidden md:block absolute top-1/2 left-0 w-full h-0.5 bg-gray-800 -z-10 transform -translate-y-1/2"></div>

                <!-- Step 1 -->
                <div class="bg-gray-900/80 glass-dark p-8 rounded-3xl border border-gray-800 hover:border-primary/50 transition-colors reveal group text-center hover-tilt">
                    <div class="w-20 h-20 mx-auto bg-gray-800 rounded-full flex items-center justify-center mb-6 group-hover:bg-primary transition-colors duration-300 shadow-lg relative">
                        <i class="fa-solid fa-water text-3xl text-primary group-hover:text-white transition-colors group-hover:rotate-12 duration-300"></i>
                        <span class="absolute -top-2 -right-2 w-8 h-8 bg-gold rounded-full flex items-center justify-center text-dark font-bold font-en border-2 border-gray-900">1</span>
                    </div>
                    <h3 class="text-xl font-bold mb-3">তাজা চিংড়ি সংগ্রহ</h3>
                    <p class="text-gray-400 text-sm">সরাসরি নদী থেকে সংগৃহীত বাছাইকৃত তাজা চিংড়ি পরিষ্কার করা হয় নিখুঁতভাবে।</p>
                </div>

                <!-- Step 2 -->
                <div class="bg-gray-900/80 glass-dark p-8 rounded-3xl border border-gray-800 hover:border-primary/50 transition-colors reveal group text-center hover-tilt" style="transition-delay: 100ms;">
                    <div class="w-20 h-20 mx-auto bg-gray-800 rounded-full flex items-center justify-center mb-6 group-hover:bg-primary transition-colors duration-300 shadow-lg relative">
                        <i class="fa-solid fa-mortar-pestle text-3xl text-primary group-hover:text-white transition-colors group-hover:-rotate-12 duration-300"></i>
                        <span class="absolute -top-2 -right-2 w-8 h-8 bg-gold rounded-full flex items-center justify-center text-dark font-bold font-en border-2 border-gray-900">2</span>
                    </div>
                    <h3 class="text-xl font-bold mb-3">খাঁটি মসলার মিশ্রণ</h3>
                    <p class="text-gray-400 text-sm">নিজস্ব ভাঙানো সরিষার তেল এবং বাছাই করা খাঁটি মসলার বিশেষ মিশ্রণ তৈরি করা হয়।</p>
                </div>

                <!-- Step 3 -->
                <div class="bg-gray-900/80 glass-dark p-8 rounded-3xl border border-gray-800 hover:border-primary/50 transition-colors reveal group text-center hover-tilt" style="transition-delay: 200ms;">
                    <div class="w-20 h-20 mx-auto bg-gray-800 rounded-full flex items-center justify-center mb-6 group-hover:bg-primary transition-colors duration-300 shadow-lg relative">
                        <i class="fa-solid fa-jar text-3xl text-primary group-hover:text-white transition-colors group-hover:scale-110 duration-300"></i>
                        <span class="absolute -top-2 -right-2 w-8 h-8 bg-gold rounded-full flex items-center justify-center text-dark font-bold font-en border-2 border-gray-900">3</span>
                    </div>
                    <h3 class="text-xl font-bold mb-3">রান্না ও সংরক্ষণ</h3>
                    <p class="text-gray-400 text-sm">সঠিক তাপমাত্রায় রান্না করে জীবাণুমুক্ত কাঁচের বয়ামে দীর্ঘদিন ভালো থাকার জন্য সংরক্ষণ।</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Reviews Section -->
    <section id="reviews" class="py-24 bg-light overflow-hidden">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid lg:grid-cols-2 gap-16 items-center">
                <div class="reveal">
                    <span class="text-primary font-bold tracking-wider text-sm mb-2 block">গ্রাহকদের মতামত</span>
                    <h2 class="text-4xl md:text-5xl font-bold text-dark mb-6 leading-tight">স্বাদ নিয়ে আমাদের গ্রাহকরা যা বলেন</h2>
                    <p class="text-gray-600 mb-8 text-lg">আমাদের শত শত সন্তুষ্ট গ্রাহকই আমাদের পণ্যের মানের সেরা প্রমাণ। আপনার মতামতের অপেক্ষায় আছি আমরাও।</p>
                    
                    <div class="flex items-center gap-6 mb-8">
                        <div class="flex -space-x-4">
                            <img class="w-12 h-12 rounded-full border-2 border-white object-cover" src="https://placehold.co/100x100/10b981/ffffff?text=U1" alt="User">
                            <img class="w-12 h-12 rounded-full border-2 border-white object-cover" src="https://placehold.co/100x100/d4af37/ffffff?text=U2" alt="User">
                            <img class="w-12 h-12 rounded-full border-2 border-white object-cover" src="https://placehold.co/100x100/111827/ffffff?text=U3" alt="User">
                            <div class="w-12 h-12 rounded-full border-2 border-white bg-gray-100 flex items-center justify-center text-xs font-bold text-dark font-en">+5k</div>
                        </div>
                        <div>
                            <div class="flex text-gold text-sm">
                                <i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i>
                            </div>
                            <span class="text-sm font-medium text-gray-500 font-en">4.9/5.0 <span class="font-hind">(৫০০০+ রিভিউ)</span></span>
                        </div>
                    </div>
                </div>

                <!-- Auto vertical scrolling reviews -->
                <div class="h-[500px] overflow-hidden relative rounded-3xl">
                    <!-- Gradient Overlays for smooth fade -->
                    <div class="absolute top-0 left-0 w-full h-20 bg-gradient-to-b from-light to-transparent z-10"></div>
                    <div class="absolute bottom-0 left-0 w-full h-20 bg-gradient-to-t from-light to-transparent z-10"></div>
                    
                    <div class="animate-scroll-vertical flex flex-col gap-6 pt-10">
                        <!-- Duplicated list for seamless loop -->
                        <script>
                            const reviews = [
                                { name: "রাকিবুল হাসান", text: "অসাধারণ স্বাদ! একবার মুখে দিলে বারবার খেতে ইচ্ছে করে। প্যাকেজিং অনেক প্রিমিয়াম ছিল।", time: "২ দিন আগে" },
                                { name: "সাদিয়া ইসলাম", text: "আমি ঝাল আচারটা অর্ডার করেছিলাম। একদম পারফেক্ট ঝাল এবং চিংড়ির পরিমাণও অনেক বেশি ছিল।", time: "১ সপ্তাহ আগে" },
                                { name: "আহমেদ জুবায়ের", text: "হোটেল বা রেস্টুরেন্টের থেকেও ভালো। একদম মায়ের হাতের রান্নার মতো স্বাদ। ধন্যবাদ রাজকীয় চিংড়ি।", time: "৩ সপ্তাহ আগে" },
                                { name: "নুসরাত জাহান", text: "তেল এবং মসলার ব্যালেন্স খুব সুন্দর। ভাত বা পোলাও সবকিছুর সাথেই দারুণ মানিয়ে যায়।", time: "১ মাস আগে" }
                            ];
                            let reviewHTML = '';
                            // Duplicate twice for infinite scroll
                            for(let i=0; i<8; i++){
                                const r = reviews[i % reviews.length];
                                reviewHTML += `
                                    <div class="bg-white p-6 rounded-2xl shadow-sm border border-gray-100 hover:shadow-md transition-shadow mx-4">
                                        <div class="flex justify-between items-start mb-4">
                                            <div class="flex items-center gap-3">
                                                <div class="w-10 h-10 rounded-full bg-primary/10 text-primary flex items-center justify-center font-bold text-lg">${r.name.charAt(0)}</div>
                                                <div>
                                                    <h4 class="font-bold text-dark">${r.name}</h4>
                                                    <div class="flex text-gold text-xs mt-1">
                                                        <i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i>
                                                    </div>
                                                </div>
                                            </div>
                                            <span class="text-xs text-gray-400">${r.time}</span>
                                        </div>
                                        <p class="text-gray-600 text-sm leading-relaxed">"${r.text}"</p>
                                    </div>
                                `;
                            }
                            document.write(reviewHTML);
                        </script>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- FAQ Section -->
    <section class="py-24 bg-white">
        <div class="max-w-3xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16 reveal">
                <h2 class="text-3xl md:text-4xl font-bold text-dark mb-4">সাধারণ জিজ্ঞাসা</h2>
                <div class="w-16 h-1 bg-gold mx-auto rounded-full"></div>
            </div>

            <div class="space-y-4 reveal" id="faq-container">
                <!-- FAQs will be generated by JS -->
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-dark pt-20 pb-10 text-white relative border-t-4 border-primary">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-12 mb-16">
                <!-- Brand Info -->
                <div class="space-y-6">
                    <a href="#" class="flex items-center gap-3 group inline-flex">
                        <div class="w-10 h-10 rounded-full bg-primary flex items-center justify-center text-white">
                            <i class="fa-solid fa-shrimp text-lg"></i>
                        </div>
                        <span class="text-2xl font-bold text-white">রাজকীয়<span class="text-gold">.</span></span>
                    </a>
                    <p class="text-gray-400 text-sm leading-relaxed">খাঁটি উপাদান ও নিজস্ব রেসিপিতে তৈরি বাংলাদেশের প্রিমিয়াম চিংড়ি আচার ব্র্যান্ড।</p>
                    <div class="flex gap-4">
                        <a href="#" class="w-10 h-10 rounded-full bg-gray-800 flex items-center justify-center hover:bg-primary transition-colors hover:-translate-y-1"><i class="fa-brands fa-facebook-f"></i></a>
                        <a href="#" class="w-10 h-10 rounded-full bg-gray-800 flex items-center justify-center hover:bg-primary transition-colors hover:-translate-y-1"><i class="fa-brands fa-instagram"></i></a>
                        <a href="#" class="w-10 h-10 rounded-full bg-gray-800 flex items-center justify-center hover:bg-primary transition-colors hover:-translate-y-1"><i class="fa-brands fa-youtube"></i></a>
                    </div>
                </div>

                <!-- Links -->
                <div>
                    <h4 class="text-lg font-bold mb-6 text-white border-b border-gray-800 pb-2 inline-block">দ্রুত লিংক</h4>
                    <ul class="space-y-3 text-gray-400 text-sm">
                        <li><a href="#home" class="hover:text-primary transition-colors flex items-center gap-2"><i class="fa-solid fa-angle-right text-xs"></i> হোম</a></li>
                        <li><a href="#products" class="hover:text-primary transition-colors flex items-center gap-2"><i class="fa-solid fa-angle-right text-xs"></i> আমাদের পণ্য</a></li>
                        <li><a href="#process" class="hover:text-primary transition-colors flex items-center gap-2"><i class="fa-solid fa-angle-right text-xs"></i> প্রস্তুত প্রণালী</a></li>
                        <li><a href="#" class="hover:text-primary transition-colors flex items-center gap-2"><i class="fa-solid fa-angle-right text-xs"></i> শর্তাবলী</a></li>
                    </ul>
                </div>

                <!-- Contact -->
                <div>
                    <h4 class="text-lg font-bold mb-6 text-white border-b border-gray-800 pb-2 inline-block">যোগাযোগ</h4>
                    <ul class="space-y-4 text-gray-400 text-sm">
                        <li class="flex items-start gap-3">
                            <i class="fa-solid fa-location-dot mt-1 text-primary"></i>
                            <span>ধানমন্ডি ২৭, ঢাকা, বাংলাদেশ</span>
                        </li>
                        <li class="flex items-center gap-3">
                            <i class="fa-solid fa-phone text-primary"></i>
                            <span class="font-en">+880 1234 567890</span>
                        </li>
                        <li class="flex items-center gap-3">
                            <i class="fa-solid fa-envelope text-primary"></i>
                            <span class="font-en">support@rajkio.com</span>
                        </li>
                    </ul>
                </div>

                <!-- Newsletter -->
                <div>
                    <h4 class="text-lg font-bold mb-6 text-white border-b border-gray-800 pb-2 inline-block">অফার পেতে সাবস্ক্রাইব করুন</h4>
                    <form class="flex flex-col gap-3" onsubmit="event.preventDefault(); showToast('ধন্যবাদ! আপনি সফলভাবে সাবস্ক্রাইব করেছেন।');">
                        <input type="email" placeholder="আপনার ইমেইল ঠিকানা" class="px-4 py-3 bg-gray-800 border border-gray-700 rounded-xl focus:outline-none focus:border-primary text-sm w-full transition-colors text-white font-en" required>
                        <button type="submit" class="bg-primary hover:bg-primary-dark text-white font-semibold py-3 rounded-xl transition-colors w-full shadow-lg shadow-primary/20">সাবস্ক্রাইব</button>
                    </form>
                </div>
            </div>
            
            <div class="border-t border-gray-800 pt-8 flex flex-col md:flex-row justify-between items-center gap-4 text-sm text-gray-500">
                <p>&copy; 2026 রাজকীয় চিংড়ি. সর্বস্বত্ব সংরক্ষিত।</p>
                <div class="flex gap-4">
                    <i class="fa-brands fa-cc-visa text-2xl hover:text-white transition-colors"></i>
                    <i class="fa-brands fa-cc-mastercard text-2xl hover:text-white transition-colors"></i>
                    <i class="fa-brands fa-cc-amex text-2xl hover:text-white transition-colors"></i>
                </div>
            </div>
        </div>
    </footer>

    <!-- Floating WhatsApp Button -->
    <a href="https://wa.me/1234567890" target="_blank" class="fixed bottom-6 left-6 z-40 bg-whatsapp text-white w-14 h-14 rounded-full flex items-center justify-center text-3xl shadow-[0_0_20px_rgba(37,211,102,0.5)] hover:scale-110 hover:shadow-[0_0_30px_rgba(37,211,102,0.8)] transition-all duration-300 animate-bounce cursor-pointer">
        <i class="fa-brands fa-whatsapp"></i>
    </a>

    <!-- Overlay for Cart -->
    <div id="cart-overlay" class="fixed inset-0 bg-dark/50 z-40 hidden backdrop-blur-sm transition-opacity opacity-0" onclick="toggleCart()"></div>

    <!-- Right Sidebar Cart -->
    <div id="cart-sidebar" class="fixed top-0 right-0 h-full w-full max-w-md bg-white z-50 shadow-2xl flex flex-col">
        <!-- Cart Header -->
        <div class="p-6 border-b border-gray-100 flex justify-between items-center bg-light">
            <h3 class="text-xl font-bold text-dark flex items-center gap-2">
                <i class="fa-solid fa-cart-shopping text-primary"></i> আপনার কার্ট
            </h3>
            <button onclick="toggleCart()" class="w-8 h-8 rounded-full bg-gray-200 hover:bg-red-100 hover:text-red-500 flex items-center justify-center transition-colors">
                <i class="fa-solid fa-xmark"></i>
            </button>
        </div>

        <!-- Cart Items -->
        <div id="cart-items" class="flex-1 overflow-y-auto p-6 space-y-4 no-scrollbar">
            <!-- Items injected by JS -->
            <div class="text-center text-gray-400 mt-20 flex flex-col items-center">
                <i class="fa-solid fa-basket-shopping text-6xl mb-4 opacity-20"></i>
                <p>কার্ট খালি আছে!</p>
            </div>
        </div>

        <!-- Cart Footer -->
        <div class="p-6 border-t border-gray-100 bg-light shadow-[0_-10px_20px_rgba(0,0,0,0.02)]">
            <div class="flex justify-between items-center mb-2">
                <span class="text-gray-500">সাবটোটাল</span>
                <span class="font-bold text-dark font-en" id="cart-subtotal">৳0</span>
            </div>
            <div class="flex justify-between items-center mb-6">
                <span class="text-gray-500">ডেলিভারি চার্জ</span>
                <span class="text-sm text-primary">চেকআউটে হিসাব করা হবে</span>
            </div>
            <button onclick="checkout()" class="w-full bg-primary hover:bg-primary-dark text-white font-bold py-4 rounded-2xl transition-all shadow-luxury hover:-translate-y-1 flex justify-center items-center gap-2">
                চেকআউট করুন <i class="fa-solid fa-arrow-right"></i>
            </button>
        </div>
    </div>

    <!-- Toast Container -->
    <div id="toast-container" class="fixed bottom-6 right-6 z-50 flex flex-col gap-3"></div>

    <!-- Scripts -->
    <script>
        // --- DATA ---
        const products = [
            {
                id: 1,
                name: "প্রিমিয়াম চিংড়ি আচার (রেগুলার)",
                weight: "৩০০ গ্রাম",
                price: 550,
                image: "src=image_7d6921.png.jpeg",
                badge: "বেস্ট সেলার"
            },
            {
                id: 2,
                name: "স্পেশাল বোম্বাই মরিচ চিংড়ি",
                weight: "৩০০ গ্রাম",
                price: 600,
                image: "https://images.unsplash.com/photo-1605646194781-a67b2d5fcb2a?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80",
                badge: "হট & স্পাইসি"
            },
            {
                id: 3,
                name: "রসুন ও চিংড়ি স্পেশাল",
                weight: "৩০০ গ্রাম",
                price: 580,
                image: "https://images.unsplash.com/photo-1589301760014-d929f3979dbc?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80",
                badge: "নতুন"
            }
        ];

        const faqs = [
            { q: "আচার কতদিন ভালো থাকে?", a: "আমাদের আচার সম্পূর্ণ প্রিজারভেটিভ মুক্ত। স্বাভাবিক তাপমাত্রায় ৩-৪ মাস এবং ফ্রিজে রাখলে ৬ মাস পর্যন্ত নিশ্চিন্তে খেতে পারবেন। তবে ব্যবহারের সময় সবসময় শুকনো চামচ ব্যবহার করবেন।" },
            { q: "ডেলিভারি চার্জ কত?", a: "ঢাকার ভেতরে ডেলিভারি চার্জ ৬০ টাকা এবং ঢাকার বাইরে ১২০ টাকা। ২টির বেশি অর্ডার করলে ঢাকার ভেতর ডেলিভারি ফ্রি!" },
            { q: "ক্যাশ অন ডেলিভারি আছে কি?", a: "হ্যাঁ, সারা বাংলাদেশে আমাদের ক্যাশ অন ডেলিভারি সুবিধা রয়েছে। পণ্য হাতে পেয়ে চেক করে মূল্য পরিশোধ করতে পারবেন।" },
            { q: "আচারে কি কি উপাদান থাকে?", a: "তাজা নদীর চিংড়ি, খাঁটি সরিষার তেল, দেশি রসুন, আদা, বোম্বাই মরিচ এবং আমাদের নিজস্ব বিশেষ মসলার মিশ্রণ। কোনো ক্ষতিকর রং বা কেমিক্যাল নেই।" }
        ];

        let cart = [];

        // --- INITIALIZATION ---
        document.addEventListener("DOMContentLoaded", () => {
            renderProducts();
            renderFAQs();
            
            // Hide Loader
            setTimeout(() => {
                const loader = document.getElementById('loader');
                loader.style.opacity = '0';
                setTimeout(() => loader.style.display = 'none', 600);
            }, 1500);

            // Init Scroll Reveal
            initScrollReveal();
        });

        // --- RENDER FUNCTIONS ---
        function renderProducts() {
            const container = document.getElementById('product-container');
            container.innerHTML = products.map((p, index) => `
                <div class="bg-white rounded-3xl overflow-hidden shadow-[0_8px_30px_rgb(0,0,0,0.04)] hover:shadow-luxury hover-tilt group relative border border-gray-100 reveal" style="transition-delay: ${index * 100}ms">
                    ${p.badge ? `<div class="absolute top-4 left-4 z-20 bg-gold text-white text-xs font-bold px-3 py-1 rounded-full shadow-md">${p.badge}</div>` : ''}
                    <div class="img-zoom-container relative h-64 bg-gray-100">
                        <img src="${p.image}" alt="${p.name}" class="w-full h-full object-cover">
                        <!-- Hover Overlay -->
                        <div class="absolute inset-0 bg-dark/20 opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-center justify-center">
                            <button onclick="quickView(${p.id})" class="bg-white text-dark w-12 h-12 rounded-full flex items-center justify-center transform translate-y-4 group-hover:translate-y-0 opacity-0 group-hover:opacity-100 transition-all duration-300 hover:bg-primary hover:text-white delay-100">
                                <i class="fa-solid fa-eye"></i>
                            </button>
                        </div>
                    </div>
                    <div class="p-6">
                        <div class="flex justify-between items-start mb-2">
                            <h3 class="text-xl font-bold text-dark leading-tight group-hover:text-primary transition-colors">${p.name}</h3>
                        </div>
                        <p class="text-gray-500 text-sm mb-4">পরিমাণ: <span class="font-en">${p.weight}</span></p>
                        <div class="flex justify-between items-center mt-6">
                            <div class="text-2xl font-bold text-primary font-en">৳${p.price}</div>
                            <button onclick="addToCart(${p.id})" class="w-12 h-12 rounded-full bg-light border border-gray-200 text-dark flex items-center justify-center hover:bg-primary hover:text-white hover:border-primary transition-all duration-300 shadow-sm group-hover:shadow-md">
                                <i class="fa-solid fa-plus"></i>
                            </button>
                        </div>
                    </div>
                </div>
            `).join('');
        }

        function renderFAQs() {
            const container = document.getElementById('faq-container');
            container.innerHTML = faqs.map((faq, i) => `
                <div class="faq-item border border-gray-100 rounded-2xl bg-light overflow-hidden transition-all duration-300 hover:border-primary/30 hover:shadow-sm cursor-pointer" onclick="toggleFaq(this)">
                    <div class="p-5 flex justify-between items-center">
                        <h4 class="font-bold text-lg text-dark">${faq.q}</h4>
                        <div class="w-8 h-8 rounded-full bg-white flex items-center justify-center shadow-sm text-primary faq-icon transition-transform duration-300">
                            <i class="fa-solid fa-chevron-down"></i>
                        </div>
                    </div>
                    <div class="faq-answer px-5 pb-0 bg-white">
                        <p class="text-gray-600 pb-5 pt-2 leading-relaxed text-sm">${faq.a}</p>
                    </div>
                </div>
            `).join('');
        }

        // --- INTERACTIONS ---
        function toggleFaq(element) {
            const isActive = element.classList.contains('active');
            // Close all
            document.querySelectorAll('.faq-item').forEach(item => item.classList.remove('active'));
            // Open clicked
            if (!isActive) element.classList.add('active');
        }

        // Navbar scroll effect
        window.addEventListener('scroll', () => {
            const nav = document.getElementById('navbar');
            if (window.scrollY > 50) {
                nav.classList.add('py-2');
                nav.classList.remove('py-4');
                nav.classList.add('bg-white/95');
            } else {
                nav.classList.add('py-4');
                nav.classList.remove('py-2');
                nav.classList.remove('bg-white/95');
            }
        });

        // Intersection Observer for scroll animations
        function initScrollReveal() {
            const reveals = document.querySelectorAll('.reveal');
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.classList.add('active');
                        // observer.unobserve(entry.target); // Unobserve if you want it to trigger only once
                    }
                });
            }, { threshold: 0.1 });

            reveals.forEach(reveal => observer.observe(reveal));
        }

        // --- CART LOGIC ---
        function toggleCart() {
            const sidebar = document.getElementById('cart-sidebar');
            const overlay = document.getElementById('cart-overlay');
            
            if (sidebar.classList.contains('open')) {
                sidebar.classList.remove('open');
                overlay.style.opacity = '0';
                setTimeout(() => overlay.classList.add('hidden'), 300);
            } else {
                sidebar.classList.add('open');
                overlay.classList.remove('hidden');
                setTimeout(() => overlay.style.opacity = '1', 10);
            }
        }

        function addToCart(productId) {
            const product = products.find(p => p.id === productId);
            const existingItem = cart.find(item => item.id === productId);

            if (existingItem) {
                existingItem.qty += 1;
            } else {
                cart.push({ ...product, qty: 1 });
            }

            updateCartUI();
            showToast(`<b>${product.name}</b> কার্টে যোগ করা হয়েছে!`);
            
            // Animation on cart icon
            const cartIcon = document.getElementById('cart-count');
            cartIcon.classList.add('scale-150');
            setTimeout(() => cartIcon.classList.remove('scale-150'), 300);
        }

        function updateQuantity(productId, delta) {
            const item = cart.find(i => i.id === productId);
            if (item) {
                item.qty += delta;
                if (item.qty <= 0) {
                    cart = cart.filter(i => i.id !== productId);
                }
                updateCartUI();
            }
        }

        function updateCartUI() {
            const container = document.getElementById('cart-items');
            const count = document.getElementById('cart-count');
            const subtotal = document.getElementById('cart-subtotal');

            // Update Count
            const totalQty = cart.reduce((sum, item) => sum + item.qty, 0);
            count.innerText = totalQty;

            // Render Items
            if (cart.length === 0) {
                container.innerHTML = `
                    <div class="text-center text-gray-400 mt-20 flex flex-col items-center">
                        <i class="fa-solid fa-basket-shopping text-6xl mb-4 opacity-20"></i>
                        <p>আপনার কার্ট খালি!</p>
                    </div>`;
                subtotal.innerText = `৳0`;
                return;
            }

            let totalAmount = 0;
            container.innerHTML = cart.map(item => {
                totalAmount += item.price * item.qty;
                return `
                <div class="flex gap-4 p-4 bg-white rounded-2xl border border-gray-100 shadow-sm relative group">
                    <img src="${item.image}" alt="${item.name}" class="w-20 h-20 object-cover rounded-xl">
                    <div class="flex-1">
                        <h4 class="font-bold text-sm text-dark leading-tight pr-6">${item.name}</h4>
                        <div class="text-primary font-bold text-sm mt-1 font-en">৳${item.price}</div>
                        
                        <div class="flex items-center gap-3 mt-2 bg-light w-max rounded-full p-1 border border-gray-100">
                            <button onclick="updateQuantity(${item.id}, -1)" class="w-6 h-6 rounded-full bg-white shadow-sm flex items-center justify-center text-dark hover:text-primary transition"><i class="fa-solid fa-minus text-xs"></i></button>
                            <span class="text-sm font-bold w-4 text-center font-en">${item.qty}</span>
                            <button onclick="updateQuantity(${item.id}, 1)" class="w-6 h-6 rounded-full bg-white shadow-sm flex items-center justify-center text-dark hover:text-primary transition"><i class="fa-solid fa-plus text-xs"></i></button>
                        </div>
                    </div>
                    <button onclick="updateQuantity(${item.id}, -${item.qty})" class="absolute top-4 right-4 text-gray-300 hover:text-red-500 transition-colors opacity-0 group-hover:opacity-100">
                        <i class="fa-solid fa-trash"></i>
                    </button>
                </div>
                `;
            }).join('');

            subtotal.innerText = `৳${totalAmount}`;
        }

        function checkout() {
            if(cart.length === 0) {
                showToast('আগে কার্টে পণ্য যোগ করুন!', 'error');
                return;
            }
            toggleCart();
            showToast('অর্ডার প্রসেসিং হচ্ছে... (ডেমো)', 'success');
        }

        // --- UTILITIES ---
        function showToast(message, type='success') {
            const container = document.getElementById('toast-container');
            const toast = document.createElement('div');
            
            const icon = type === 'success' ? '<i class="fa-solid fa-circle-check text-primary text-xl"></i>' : '<i class="fa-solid fa-circle-exclamation text-red-500 text-xl"></i>';
            const borderColor = type === 'success' ? 'border-primary' : 'border-red-500';

            toast.className = `bg-white px-5 py-4 rounded-xl shadow-luxury border-l-4 ${borderColor} flex items-center gap-3 min-w-[300px] toast-enter z-50`;
            toast.innerHTML = `
                ${icon}
                <span class="text-dark text-sm font-medium">${message}</span>
            `;

            container.appendChild(toast);

            // Remove after 3s
            setTimeout(() => {
                toast.style.animation = 'slideInUp 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275) reverse forwards';
                setTimeout(() => toast.remove(), 400);
            }, 3000);
        }

        function quickView(id) {
            showToast('Quick view detail modal will open here.');
        }

    </script>
</body>
</html>


![image alt]([image url](https://github.com/rezvikhanofficial/portfolio-website/blob/9d0416c4b5f96eb1219bab04f487950eb0847006/src%3Dimage_7d6921.png.jpeg
))


