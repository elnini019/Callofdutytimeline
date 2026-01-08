<!DOCTYPE html><html lang="en"><head>
    <meta charset="UTF-8"/>
    <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
    <title>Modern Warfare Trilogy - The Legendary FPS Series</title>
    <meta name="description" content="Explore the legendary Call of Duty Modern Warfare trilogy. Discover iconic characters, memorable missions, and the evolution of modern military shooters."/>
    
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.loli.net"/>
    <link rel="preconnect" href="https://gstatic.loli.net" crossorigin=""/>
    <link href="https://fonts.loli.net/css2?family=Orbitron:wght@400;700;900&amp;family=Inter:wght@300;400;500;600;700&amp;family=JetBrains+Mono:wght@400;500&amp;display=swap" rel="stylesheet"/>
    
    <!-- Core Libraries -->
    <script src="https://s4.zstatic.net/ajax/libs/animejs/3.2.1/anime.min.js"></script>
    <script src="https://s4.zstatic.net/ajax/libs/typed.js/2.0.12/typed.min.js"></script>
    <script src="https://cdn.jsdmirror.com/npm/@splidejs/splide@4.1.4/dist/js/splide.min.js"></script>
    <link href="https://cdn.jsdmirror.com/npm/@splidejs/splide@4.1.4/dist/css/splide.min.css" rel="stylesheet"/>
    <script src="https://s4.zstatic.net/npm/splitting@1.0.6/dist/splitting.min.js"></script>
    <link href="https://s4.zstatic.net/npm/splitting@1.0.6/dist/splitting.css" rel="stylesheet"/>
    
    <style>
        :root {
            --primary-bg: #1a1a1a;
            --secondary-bg: #0d0d0d;
            --accent-amber: #f59e0b;
            --accent-red: #dc2626;
            --text-light: #e5e7eb;
            --text-gray: #6b7280;
            --military-olive: #4a5d23;
        }
        
        body {
            font-family: 'Inter', sans-serif;
            background-color: var(--primary-bg);
            color: var(--text-light);
            overflow-x: hidden;
        }
        
        .font-orbitron {
            font-family: 'Orbitron', monospace;
        }
        
        .font-jetbrains {
            font-family: 'JetBrains Mono', monospace;
        }
        
        /* Hero Section */
        .hero-section {
            height: 100vh;
            background: linear-gradient(rgba(0,0,0,0.4), rgba(0,0,0,0.6)), url('resources/hero-image.png');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
        }
        
        /* Navigation */
        .nav-blur {
            backdrop-filter: blur(10px);
            background: rgba(13, 13, 13, 0.8);
        }
        
        .nav-link {
            position: relative;
            transition: all 0.3s ease;
        }
        
        .nav-link:hover {
            color: var(--accent-amber);
        }
        
        .nav-link::after {
            content: '';
            position: absolute;
            bottom: -2px;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--accent-red);
            transition: width 0.3s ease;
        }
        
        .nav-link:hover::after {
            width: 100%;
        }
        
        /* Game Timeline */
        .timeline-container {
            position: relative;
        }
        
        .timeline-line {
            position: absolute;
            top: 50%;
            left: 0;
            right: 0;
            height: 2px;
            background: linear-gradient(90deg, var(--accent-amber), var(--accent-red));
            z-index: 1;
        }
        
        .timeline-item {
            position: relative;
            z-index: 2;
            background: var(--secondary-bg);
            border: 2px solid var(--accent-amber);
            transition: all 0.3s ease;
            cursor: pointer;
        }
        
        .timeline-item:hover {
            transform: translateY(-5px) scale(1.02);
            box-shadow: 0 10px 30px rgba(245, 158, 11, 0.3);
            border-color: var(--accent-red);
        }
        
        /* Game Cards */
        .game-card {
            background: linear-gradient(135deg, var(--secondary-bg), #2a2a2a);
            border: 1px solid #333;
            transition: all 0.3s ease;
        }
        
        .game-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 15px 40px rgba(0,0,0,0.5);
            border-color: var(--accent-amber);
        }
        
        /* Character Cards */
        .character-card {
            background: var(--secondary-bg);
            border: 1px solid #333;
            transition: all 0.3s ease;
            cursor: pointer;
        }
        
        .character-card:hover {
            transform: scale(1.05);
            border-color: var(--accent-red);
            box-shadow: 0 8px 25px rgba(220, 38, 38, 0.3);
        }
        
        .character-portrait {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            border: 3px solid var(--accent-amber);
            object-fit: cover;
        }
        
        /* Mission Cards */
        .mission-card {
            background: var(--secondary-bg);
            border: 1px solid #333;
            transition: all 0.3s ease;
            cursor: pointer;
        }
        
        .mission-card:hover {
            transform: translateY(-3px);
            border-color: var(--accent-red);
            box-shadow: 0 5px 20px rgba(220, 38, 38, 0.2);
        }
        
        /* Buttons */
        .btn-primary {
            background: linear-gradient(135deg, var(--accent-amber), #d97706);
            color: var(--secondary-bg);
            font-weight: 600;
            transition: all 0.3s ease;
        }
        
        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(245, 158, 11, 0.4);
        }
        
        .btn-secondary {
            background: transparent;
            border: 2px solid var(--accent-red);
            color: var(--accent-red);
            font-weight: 600;
            transition: all 0.3s ease;
        }
        
        .btn-secondary:hover {
            background: var(--accent-red);
            color: white;
            transform: translateY(-2px);
        }
        
        /* Animations */
        .fade-in {
            opacity: 0.9;
            transform: translateY(20px);
        }
        
        .stagger-in > * {
            opacity: 0;
            transform: translateY(30px);
        }
        
        /* Scrollbar Styling */
        ::-webkit-scrollbar {
            width: 8px;
        }
        
        ::-webkit-scrollbar-track {
            background: var(--secondary-bg);
        }
        
        ::-webkit-scrollbar-thumb {
            background: var(--accent-amber);
            border-radius: 4px;
        }
        
        ::-webkit-scrollbar-thumb:hover {
            background: var(--accent-red);
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .hero-section {
                background-attachment: scroll;
            }
            
            .timeline-line {
                display: none;
            }
            
            .character-portrait {
                width: 80px;
                height: 80px;
            }
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav class="fixed top-0 left-0 right-0 z-50 nav-blur">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-16">
                <div class="flex items-center">
                    <h1 class="text-xl font-orbitron font-bold text-amber-400">MW TRILOGY</h1>
                </div>
                
                <div class="hidden md:block">
                    <div class="ml-10 flex items-baseline space-x-8">
                        <a href="index.html" class="nav-link text-white hover:text-amber-400 px-3 py-2 text-sm font-medium">Home</a>
                        <a href="games.html" class="nav-link text-gray-300 hover:text-amber-400 px-3 py-2 text-sm font-medium">Games</a>
                        <a href="gallery.html" class="nav-link text-gray-300 hover:text-amber-400 px-3 py-2 text-sm font-medium">Gallery</a>
                    </div>
                </div>
                
                <div class="md:hidden">
                    <button id="mobile-menu-btn" class="text-gray-400 hover:text-white">
                        <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
                        </svg>
                    </button>
                </div>
            </div>
        </div>
        
        <div id="mobile-menu" class="md:hidden hidden">
            <div class="px-2 pt-2 pb-3 space-y-1 sm:px-3 bg-black bg-opacity-90">
                <a href="index.html" class="text-white block px-3 py-2 text-base font-medium">Home</a>
                <a href="games.html" class="text-gray-300 hover:text-white block px-3 py-2 text-base font-medium">Games</a>
                <a href="gallery.html" class="text-gray-300 hover:text-white block px-3 py-2 text-base font-medium">Gallery</a>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero-section flex items-center justify-center relative">
        <div class="text-center z-10 max-w-4xl mx-auto px-4">
            <h1 class="hero-title font-orbitron text-4xl md:text-6xl lg:text-7xl font-black text-white mb-6"></h1>
            <p class="text-xl md:text-2xl text-gray-300 mb-8 max-w-3xl mx-auto">
                Experience the legendary trilogy that defined modern military shooters. 
                From the streets of Pripyat to the battlefields of World War III.
            </p>
            <div class="flex flex-col sm:flex-row gap-4 justify-center">
                <a href="games.html" class="btn-primary px-8 py-3 rounded-lg text-lg font-semibold">
                    Explore the Games
                </a>
                <a href="gallery.html" class="btn-secondary px-8 py-3 rounded-lg text-lg font-semibold">
                    View Gallery
                </a>
            </div>
        </div>
        
        <!-- Scroll indicator -->
        <div class="absolute bottom-8 left-1/2 transform -translate-x-1/2 animate-bounce">
            <svg class="w-6 h-6 text-amber-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 14l-7 7m0 0l-7-7m7 7V3"></path>
            </svg>
        </div>
    </section>

    <!-- Game Timeline Section -->
    <section class="py-20 bg-gradient-to-b from-gray-900 to-black">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16 fade-in">
                <h2 class="text-4xl md:text-5xl font-orbitron font-bold text-white mb-6">
                    The Trilogy Timeline
                </h2>
                <p class="text-xl text-gray-400 max-w-3xl mx-auto">
                    Three games that changed the landscape of modern military shooters forever
                </p>
            </div>
            
            <div class="timeline-container mb-16">
                <div class="timeline-line"></div>
                <div class="grid grid-cols-1 md:grid-cols-3 gap-8 stagger-in">
                    <!-- Modern Warfare 1 -->
                    <div class="timeline-item p-6 rounded-lg text-center" data-game="mw1">
                        <div class="mb-4">
                            <img src="https://kimi-web-img.moonshot.cn/img/shared.fastly.steamstatic.com/241efe682b3d89c51677784ebdc00a157c1372a9.jpg" alt="Modern Warfare 1" class="w-full h-48 object-cover rounded-lg mb-4"/>
                        </div>
                        <h3 class="text-2xl font-orbitron font-bold text-amber-400 mb-2">Modern Warfare</h3>
                        <p class="text-lg text-amber-300 mb-2">2007</p>
                        <p class="text-gray-400 text-sm">The beginning of a revolution</p>
                    </div>
                    
                    <!-- Modern Warfare 2 -->
                    <div class="timeline-item p-6 rounded-lg text-center" data-game="mw2">
                        <div class="mb-4">
                            <img src="https://kimi-web-img.moonshot.cn/img/shared.fastly.steamstatic.com/b850115bff7752abac56f39f4ddd0267f7720754.jpg" alt="Modern Warfare 2" class="w-full h-48 object-cover rounded-lg mb-4"/>
                        </div>
                        <h3 class="text-2xl font-orbitron font-bold text-amber-400 mb-2">Modern Warfare 2</h3>
                        <p class="text-lg text-amber-300 mb-2">2009</p>
                        <p class="text-gray-400 text-sm">Task Force 141 rises</p>
                    </div>
                    
                    <!-- Modern Warfare 3 -->
                    <div class="timeline-item p-6 rounded-lg text-center" data-game="mw3">
                        <div class="mb-4">
                            <img src="https://kimi-web-img.moonshot.cn/img/shared.fastly.steamstatic.com/b14cc99c7a1d8b2322356475a48df7c9af65d1b5.jpg" alt="Modern Warfare 3" class="w-full h-48 object-cover rounded-lg mb-4"/>
                        </div>
                        <h3 class="text-2xl font-orbitron font-bold text-amber-400 mb-2">Modern Warfare 3</h3>
                        <p class="text-lg text-amber-300 mb-2">2011</p>
                        <p class="text-gray-400 text-sm">World War III begins</p>
                    </div>
                </div>
            </div>
            
            <!-- Game Details Panel -->
            <div id="game-details" class="bg-gray-900 rounded-lg p-8 border border-gray-700 fade-in">
                <p class="text-center text-gray-400">Click on a game above to learn more</p>
            </div>
        </div>
    </section>

    <!-- Featured Characters Section -->
    <section class="py-20 bg-black">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16 fade-in">
                <h2 class="text-4xl md:text-5xl font-orbitron font-bold text-white mb-6">
                    Legendary Characters
                </h2>
                <p class="text-xl text-gray-400 max-w-3xl mx-auto">
                    Meet the iconic soldiers who defined a generation of gaming
                </p>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 stagger-in">
                <!-- Captain Price -->
                <div class="character-card p-6 rounded-lg text-center" data-character="price" data-faction="sas">
                    <div class="mb-4">
                        <img src="https://kimi-web-img.moonshot.cn/img/rare-gallery.com/48894eb9257488fa742bad7afd7f5f7a880c1a69.jpg" alt="Captain Price" class="character-portrait mx-auto"/>
                    </div>
                    <h3 class="text-xl font-bold text-white mb-2">Captain John Price</h3>
                    <p class="text-amber-400 mb-2">SAS Captain</p>
                    <p class="text-gray-400 text-sm">Veteran operative and mentor to Soap</p>
                </div>
                
                <!-- Soap MacTavish -->
                <div class="character-card p-6 rounded-lg text-center" data-character="soap" data-faction="sas">
                    <div class="mb-4">
                        <img src="https://kimi-web-img.moonshot.cn/img/img1b.gamersky.com/fd7fbd331ff66b2c0c233ac91f4bbf0c06195777.jpg" alt="Soap MacTavish" class="character-portrait mx-auto"/>
                    </div>
                    <h3 class="text-xl font-bold text-white mb-2">John &#34;Soap&#34; MacTavish</h3>
                    <p class="text-amber-400 mb-2">Task Force 141 Commander</p>
                    <p class="text-gray-400 text-sm">From rookie to legendary commander</p>
                </div>
                
                <!-- Ghost -->
                <div class="character-card p-6 rounded-lg text-center" data-character="ghost" data-faction="task-force">
                    <div class="mb-4">
                        <img src="https://kimi-web-img.moonshot.cn/img/static.wikia.nocookie.net/03e08cb12e0d87eec04432167eda0eb296ddf59e" alt="Ghost" class="character-portrait mx-auto"/>
                    </div>
                    <h3 class="text-xl font-bold text-white mb-2">Simon &#34;Ghost&#34; Riley</h3>
                    <p class="text-amber-400 mb-2">Task Force 141 Lieutenant</p>
                    <p class="text-gray-400 text-sm">Master of stealth and tactics</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Iconic Missions Section -->
    <section class="py-20 bg-gradient-to-b from-black to-gray-900">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16 fade-in">
                <h2 class="text-4xl md:text-5xl font-orbitron font-bold text-white mb-6">
                    Unforgettable Missions
                </h2>
                <p class="text-xl text-gray-400 max-w-3xl mx-auto">
                    Relive the moments that defined modern gaming history
                </p>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6 stagger-in">
                <!-- All Ghillied Up -->
                <div class="mission-card p-4 rounded-lg" data-mission="all-ghillied-up">
                    <div class="mb-4">
                        <img src="https://kimi-web-img.moonshot.cn/img/portforward.com/df2772ecc4b571364846f032e547adb1b9902016.webp" alt="All Ghillied Up" class="w-full h-32 object-cover rounded-lg"/>
                    </div>
                    <h3 class="text-lg font-bold text-white mb-2">All Ghillied Up</h3>
                    <p class="text-amber-400 text-sm mb-2">Call of Duty 4</p>
                    <p class="text-gray-400 text-sm">The stealth mission that started it all</p>
                </div>
                
                <!-- No Russian -->
                <div class="mission-card p-4 rounded-lg" data-mission="no-russian">
                    <div class="mb-4">
                        <img src="https://kimi-web-img.moonshot.cn/img/oyster.ignimgs.com/6a6e559069ce04ec066bad60504d7be233636974.jpg" alt="No Russian" class="w-full h-32 object-cover rounded-lg"/>
                    </div>
                    <h3 class="text-lg font-bold text-white mb-2">No Russian</h3>
                    <p class="text-amber-400 text-sm mb-2">Modern Warfare 2</p>
                    <p class="text-gray-400 text-sm">The controversial airport mission</p>
                </div>
                
                <!-- Cliffhanger -->
                <div class="mission-card p-4 rounded-lg" data-mission="cliffhanger">
                    <div class="mb-4">
                        <img src="https://kimi-web-img.moonshot.cn/img/portforward.com/d406692699b9b0dd48c2416d4a69e3bb6964565b.webp" alt="Cliffhanger" class="w-full h-32 object-cover rounded-lg"/>
                    </div>
                    <h3 class="text-lg font-bold text-white mb-2">Cliffhanger</h3>
                    <p class="text-amber-400 text-sm mb-2">Modern Warfare 2</p>
                    <p class="text-gray-400 text-sm">Ice climbing and snowmobile chase</p>
                </div>
                
                <!-- Dust to Dust -->
                <div class="mission-card p-4 rounded-lg" data-mission="dust-to-dust">
                    <div class="mb-4">
                        <img src="https://kimi-web-img.moonshot.cn/img/static.wikia.nocookie.net/04562ac778c7cbadbebe08786f9c004e2c912861" alt="Dust to Dust" class="w-full h-32 object-cover rounded-lg"/>
                    </div>
                    <h3 class="text-lg font-bold text-white mb-2">Dust to Dust</h3>
                    <p class="text-amber-400 text-sm mb-2">Modern Warfare 3</p>
                    <p class="text-gray-400 text-sm">The final confrontation</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-black border-t border-gray-800 py-8">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center">
                <p class="text-gray-400 text-sm">
                    © 2024 Modern Warfare Trilogy Tribute. This is a fan-made website celebrating the legendary series.
                </p>
                <p class="text-gray-500 text-xs mt-2">
                    Call of Duty and Modern Warfare are trademarks of Activision Publishing, Inc.
                </p>
            </div>
        </div>
    </footer>

    <!-- Character Detail Modal -->
    <div id="character-modal" class="modal fixed inset-0 bg-black bg-opacity-75 flex items-center justify-center z-50 hidden">
        <div class="modal-backdrop absolute inset-0"></div>
        <div class="bg-gray-900 rounded-lg p-8 max-w-2xl mx-4 relative border border-gray-700">
            <button class="close-modal absolute top-4 right-4 text-gray-400 hover:text-white">
                <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
                </svg>
            </button>
            <div id="character-modal-content"></div>
        </div>
    </div>

    <!-- Main JavaScript -->
    <script src="main.js"></script>

</body></html>
