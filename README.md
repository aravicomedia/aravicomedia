<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ARAVICO Media | Crafting Future Media</title>
    <!-- Tailwind CSS v4 Browser Script -->
    <script src="https://unpkg.com/@tailwindcss/browser@4"></script>
    <style type="text/tailwindcss">
        @theme {
            --font-sans: -apple-system, BlinkMacSystemFont, 'SF Pro Display', 'SF Pro Text', 'Inter', 'Helvetica Neue', sans-serif;
            --color-ios-bg: #000000;
            --color-ios-card: rgba(28, 28, 30, 0.7);
            --color-ios-accent: #0A84FF;
            --color-ios-text: #FFFFFF;
            --color-ios-border: rgba(255, 255, 255, 0.1);
        }

        @layer base {
            body {
                @apply bg-ios-bg text-ios-text font-sans antialiased selection:bg-ios-accent/30;
                overflow-x: hidden;
            }
        }

        @layer utilities {
            .ios-glass {
                @apply bg-ios-card backdrop-blur-[40px] border border-ios-border;
            }
            
            .ios-pill {
                @apply bg-white/10 backdrop-blur-[10px] border border-white/5 rounded-full px-4 py-1.5 text-xs font-medium;
            }

            .text-gradient {
                @apply bg-clip-text text-transparent bg-linear-to-b from-white to-[#888];
            }

            .mesh-glow {
                background: radial-gradient(circle at center, rgba(10, 132, 255, 0.15) 0%, transparent 70%);
            }
        }

        .mesh-gradient-bg {
            position: absolute;
            top: -20%;
            right: -10%;
            width: 600px;
            height: 600px;
            z-index: -1;
            pointer-events: none;
        }

        /* Reveal animations */
        .reveal {
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 0.8s ease-out, transform 0.8s ease-out;
        }

        .reveal.active {
            opacity: 1;
            transform: translateY(0);
        }

        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="min-h-screen">
    <div class="mesh-gradient-bg mesh-glow"></div>

    <!-- Navigation -->
    <nav id="nav" class="fixed top-0 left-0 right-0 z-50 transition-all duration-500 px-10 py-8">
        <div class="max-w-7xl mx-auto flex justify-between items-center">
            <div class="flex items-center gap-4">
                <span class="font-bold tracking-tighter text-xl uppercase text-white">Aravico Media</span>
            </div>
            
            <div class="hidden md:flex items-center gap-4">
                <div class="ios-pill uppercase tracking-widest opacity-80">Jakarta / 2026</div>
                <div class="ios-pill uppercase tracking-widest text-[#0A84FF]">Status: Live</div>
                <a 
                    href="https://www.instagram.com/aravico.media?igsh=cW5zY2pjYTF6dmM5"
                    target="_blank"
                    rel="noopener noreferrer"
                    class="hidden lg:flex px-6 py-2.5 ios-glass rounded-full text-xs font-bold uppercase tracking-widest hover:bg-white/10 transition-all items-center no-underline text-white"
                >
                    Connect <i data-lucide="instagram" class="ml-2 w-3 h-3"></i>
                </a>
            </div>

            <button id="menu-toggle" class="md:hidden ios-glass p-3 rounded-full text-white cursor-pointer">
                <i data-lucide="menu" id="menu-icon" class="w-5 h-5"></i>
            </button>
        </div>

        <!-- Mobile Menu -->
        <div id="mobile-menu" class="hidden md:hidden ios-glass mt-4 rounded-2xl overflow-hidden p-6">
            <div class="flex flex-col gap-4">
                <a href="#services" class="text-lg font-medium text-white/80 no-underline">Services</a>
                <a href="#portfolio" class="text-lg font-medium text-white/80 no-underline">Portfolio</a>
                <a href="https://www.instagram.com/aravico.media" target="_blank" class="text-lg font-medium text-white/80 flex items-center gap-2 no-underline">
                    Instagram <i data-lucide="instagram" class="w-4 h-4"></i>
                </a>
            </div>
        </div>
    </nav>

    <main>
        <!-- Hero Section -->
        <section class="relative min-h-screen flex flex-col items-center justify-center px-10 overflow-hidden pt-20 text-center lg:text-left">
            <div class="max-w-7xl mx-auto w-full grid grid-cols-1 lg:grid-cols-[1.2fr_0.8fr] gap-20 items-center">
                <div class="hero-left reveal active">
                    <h1 class="text-7xl md:text-[104px] font-extrabold tracking-[-0.05em] mb-6 leading-[0.9] text-gradient">
                        CRAFTING<br>FUTURE<br>MEDIA.
                    </h1>
                    
                    <p class="max-w-md mx-auto lg:mx-0 text-white/60 text-xl md:text-2xl mb-12 font-light leading-relaxed">
                        Visionary storytelling and digital cinematography for the next generation of creators.
                    </p>

                    <div class="flex flex-col sm:flex-row items-center lg:items-start gap-6">
                        <a
                            href="https://www.instagram.com/aravico.media"
                            target="_blank"
                            rel="noopener noreferrer"
                            class="px-10 py-5 bg-white text-black font-bold rounded-full flex items-center gap-3 text-lg transition-transform hover:scale-105 active:scale-95 no-underline"
                        >
                            Visit Instagram <i data-lucide="instagram" class="w-5 h-5 text-black"></i>
                        </a>
                        <div class="flex flex-col text-center sm:text-left">
                            <span class="text-white/40 text-sm font-medium tracking-widest uppercase">Available Globally</span>
                            <span class="text-white/20 text-sm font-mono mt-1">@aravico.media</span>
                        </div>
                    </div>
                </div>

                <!-- Bento Grid -->
                <div class="hidden lg:grid grid-cols-2 grid-rows-2 gap-5">
                   <div class="ios-glass p-8 rounded-[32px] flex flex-col justify-between h-[200px] reveal active" style="transition-delay: 0.1s">
                      <div class="w-11 h-11 bg-white/5 rounded-xl flex items-center justify-center">
                         <i data-lucide="camera" class="text-[#0A84FF] w-5 h-5"></i>
                      </div>
                      <div>
                        <div class="text-[0.9rem] font-semibold opacity-50 uppercase tracking-widest">Production</div>
                        <div class="text-3xl font-semibold mt-2">4K Cinema</div>
                      </div>
                   </div>
                   <div class="ios-glass p-8 rounded-[32px] flex flex-col justify-between h-[200px] reveal active" style="transition-delay: 0.2s">
                      <div class="w-11 h-11 bg-white/5 rounded-xl flex items-center justify-center">
                         <i data-lucide="bar-chart-3" class="text-[#34C759] w-5 h-5"></i>
                      </div>
                      <div>
                        <div class="text-[0.9rem] font-semibold opacity-50 uppercase tracking-widest">Social</div>
                        <div class="text-3xl font-semibold mt-2">85K+ Reach</div>
                      </div>
                   </div>
                   <div class="col-span-2 ios-glass p-8 rounded-[32px] flex flex-col justify-between reveal active" style="transition-delay: 0.3s">
                      <div class="w-11 h-11 bg-white/5 rounded-xl flex items-center justify-center">
                         <i data-lucide="sparkles" class="text-[#FF3B30] w-5 h-5"></i>
                      </div>
                      <div>
                        <div class="text-[0.9rem] font-semibold opacity-50 uppercase tracking-widest">Agency Strategy</div>
                        <div class="text-2xl font-semibold mt-2">Modern Digital Presence & Ecosystem</div>
                      </div>
                   </div>
                </div>
            </div>
        </section>

        <!-- Services Section -->
        <section id="services" class="py-24 px-10 max-w-7xl mx-auto">
            <div class="flex flex-col md:flex-row justify-between items-end mb-16 gap-8">
                <div class="max-w-2xl reveal">
                    <span class="text-white/40 text-sm font-bold uppercase tracking-widest mb-4 block">Our Expertise</span>
                    <h2 class="text-4xl md:text-6xl font-bold tracking-tight">Full-service digital creation.</h2>
                </div>
            </div>

            <div class="grid md:grid-cols-3 gap-6">
                <div class="group ios-glass p-10 rounded-[32px] relative overflow-hidden flex flex-col h-full hover:border-[#0A84FF]/50 transition-colors duration-500 reveal">
                    <div class="absolute inset-0 bg-gradient-to-br from-blue-500/20 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
                    <div class="w-14 h-14 bg-white/5 rounded-2xl flex items-center justify-center mb-8 group-hover:bg-white group-hover:text-black transition-all duration-300 z-10">
                        <i data-lucide="camera" class="w-7 h-7"></i>
                    </div>
                    <h3 class="text-2xl font-bold mb-4 z-10">Content Production</h3>
                    <p class="text-white/50 text-lg leading-relaxed z-10">Cinematic video and high-end photography that captures the soul of your brand.</p>
                </div>
                <div class="group ios-glass p-10 rounded-[32px] relative overflow-hidden flex flex-col h-full hover:border-[#0A84FF]/50 transition-colors duration-500 reveal" style="transition-delay: 0.1s">
                    <div class="absolute inset-0 bg-gradient-to-br from-purple-500/20 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
                    <div class="w-14 h-14 bg-white/5 rounded-2xl flex items-center justify-center mb-8 group-hover:bg-white group-hover:text-black transition-all duration-300 z-10">
                        <i data-lucide="bar-chart-3" class="w-7 h-7"></i>
                    </div>
                    <h3 class="text-2xl font-bold mb-4 z-10">Growth Strategy</h3>
                    <p class="text-white/50 text-lg leading-relaxed z-10">Data-driven social media management designed to scale your impact globally.</p>
                </div>
                <div class="group ios-glass p-10 rounded-[32px] relative overflow-hidden flex flex-col h-full hover:border-[#0A84FF]/50 transition-colors duration-500 reveal" style="transition-delay: 0.2s">
                    <div class="absolute inset-0 bg-gradient-to-br from-orange-500/20 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
                    <div class="w-14 h-14 bg-white/5 rounded-2xl flex items-center justify-center mb-8 group-hover:bg-white group-hover:text-black transition-all duration-300 z-10">
                        <i data-lucide="zap" class="w-7 h-7"></i>
                    </div>
                    <h3 class="text-2xl font-bold mb-4 z-10">Digital Ecosystem</h3>
                    <p class="text-white/50 text-lg leading-relaxed z-10">Crafting beautiful, high-performance digital experiences for the next generation.</p>
                </div>
            </div>
        </section>

        <!-- Portfolio Section -->
        <section id="portfolio" class="py-24 px-10 max-w-7xl mx-auto">
            <div class="flex items-center justify-between mb-16 reveal">
                <h2 class="text-4xl md:text-6xl font-bold tracking-tight">Recent Work</h2>
            </div>

            <div class="grid grid-cols-2 md:grid-cols-3 auto-rows-[250px] gap-6">
                <div class="group rounded-[32px] relative overflow-hidden ios-glass col-span-2 row-span-2 reveal">
                    <img src="https://picsum.photos/seed/neon/1200/800" alt="Neon Flux" class="absolute inset-0 w-full h-full object-cover transition-transform duration-700 group-hover:scale-110 opacity-60">
                    <div class="absolute inset-0 bg-gradient-to-t from-black/80 via-transparent to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 p-8 flex flex-col justify-end">
                        <span class="text-xs font-bold uppercase tracking-widest text-white/60 mb-2">Commercial</span>
                        <h4 class="text-2xl font-bold text-white">Neon Flux</h4>
                    </div>
                </div>
                <div class="group rounded-[32px] relative overflow-hidden ios-glass col-span-1 row-span-1 reveal" style="transition-delay: 0.1s">
                    <img src="https://picsum.photos/seed/view/800/800" alt="Short Film" class="absolute inset-0 w-full h-full object-cover transition-transform duration-700 group-hover:scale-110 opacity-60">
                    <div class="absolute inset-0 bg-gradient-to-t from-black/80 via-transparent to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 p-8 flex flex-col justify-end">
                        <span class="text-xs font-bold uppercase tracking-widest text-white/60 mb-2">Short Film</span>
                        <h4 class="text-2xl font-bold text-white">Ethereal View</h4>
                    </div>
                </div>
                <div class="group rounded-[32px] relative overflow-hidden ios-glass col-span-1 row-span-1 reveal" style="transition-delay: 0.2s">
                    <img src="https://picsum.photos/seed/soul/800/800" alt="Branding" class="absolute inset-0 w-full h-full object-cover transition-transform duration-700 group-hover:scale-110 opacity-60">
                    <div class="absolute inset-0 bg-linear-to-t from-black/80 via-transparent to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 p-8 flex flex-col justify-end">
                        <span class="text-xs font-bold uppercase tracking-widest text-white/60 mb-2">Branding</span>
                        <h4 class="text-2xl font-bold text-white">Digital Soul</h4>
                    </div>
                </div>
            </div>
        </section>

        <!-- CTA Section -->
        <section class="py-32 px-10">
            <div class="max-w-5xl mx-auto ios-glass p-10 md:p-20 rounded-[3rem] text-center relative overflow-hidden reveal">
                <div class="absolute top-0 right-0 w-64 h-64 bg-white/5 blur-[80px] rounded-full translate-x-1/2 -translate-y-1/2"></div>
                
                <h2 class="text-4xl md:text-7xl font-bold mb-8 leading-tight text-white">Ready to transcend the ordinary?</h2>
                <p class="text-white/50 text-lg md:text-xl mb-12 max-w-2xl mx-auto">
                    Join our network of elite partners and redefine your brand presence in the digital age.
                </p>
                
                <a
                    href="https://www.instagram.com/aravico.media"
                    target="_blank"
                    rel="noopener noreferrer"
                    class="inline-flex items-center gap-3 px-10 py-5 bg-white text-black font-bold rounded-full text-xl hover:scale-105 active:scale-95 transition-all no-underline"
                >
                    Visit Instagram <i data-lucide="instagram" class="w-6 h-6 text-black"></i>
                </a>
            </div>
        </section>
    </main>

    <!-- Footer -->
    <footer class="py-20 px-10 border-t border-white/5 opacity-40 font-medium text-xs tracking-widest uppercase reveal">
        <div class="max-w-7xl mx-auto flex flex-col md:flex-row justify-between items-center gap-8">
            <div>© 2026 ARAVICO MEDIA. ALL RIGHTS RESERVED.</div>
            <div>DESIGNED FOR IOS 26 ENVIRONMENT</div>
        </div>
    </footer>

    <!-- Lucide Icons Library -->
    <script src="https://unpkg.com/lucide@latest"></script>
    <script>
        // Initialize Icons
        lucide.createIcons();

        // Navbar Scroll Effect
        const nav = document.getElementById('nav');
        window.addEventListener('scroll', () => {
            if (window.scrollY > 50) {
                nav.classList.add('backdrop-blur-xl', 'bg-black/40');
            } else {
                nav.classList.remove('backdrop-blur-xl', 'bg-black/40');
            }
        });

        // Mobile Menu Toggle
        const menuToggle = document.getElementById('menu-toggle');
        const mobileMenu = document.getElementById('mobile-menu');

        menuToggle.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });

        // Scroll Reveal Animation
        const revealElements = document.querySelectorAll('.reveal');
        const observerOptions = { threshold: 0.1 };
        
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('active');
                }
            });
        }, observerOptions);

        revealElements.forEach(el => observer.observe(el));
    </script>
</body>
</html>
