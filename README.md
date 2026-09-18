<!DOCTYPE html><html lang="bn">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Modern Dashboard</title>  <script src="https://cdn.tailwindcss.com"></script>  <script>
    tailwind.config = {
      theme: {
        extend: {
          animation: {
            float: "float 6s ease-in-out infinite",
            pulseSlow: "pulseSlow 3s ease-in-out infinite",
          },
          keyframes: {
            float: {
              "0%, 100%": { transform: "translateY(0px)" },
              "50%": { transform: "translateY(-18px)" }
            },
            pulseSlow: {
              "0%, 100%": { transform: "scale(1)" },
              "50%": { transform: "scale(1.05)" }
            }
          }
        }
      }
    }
  </script>  <style>
    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      font-family: Inter, system-ui, sans-serif;
      background:
        radial-gradient(circle at 10% 20%, rgba(99,102,241,.25), transparent 30%),
        radial-gradient(circle at 90% 10%, rgba(236,72,153,.22), transparent 30%),
        radial-gradient(circle at 50% 100%, rgba(14,165,233,.2), transparent 35%),
        #080b18;
      color: white;
      min-height: 100vh;
      overflow-x: hidden;
    }

    .glass {
      background: rgba(255,255,255,.08);
      border: 1px solid rgba(255,255,255,.12);
      backdrop-filter: blur(20px);
      -webkit-backdrop-filter: blur(20px);
      box-shadow: 0 20px 60px rgba(0,0,0,.25);
    }

    .glow {
      box-shadow:
        0 0 30px rgba(99,102,241,.18),
        0 20px 60px rgba(0,0,0,.25);
    }

    .nav-link {
      transition: .25s ease;
    }

    .nav-link:hover {
      background: rgba(255,255,255,.1);
      transform: translateY(-2px);
    }

    .card {
      transition: .3s ease;
    }

    .card:hover {
      transform: translateY(-7px);
      border-color: rgba(255,255,255,.22);
    }
  </style></head><body>  <!-- Background Decorations -->  <div class="fixed inset-0 pointer-events-none overflow-hidden">
    <div class="absolute -top-32 -left-32 w-80 h-80 bg-indigo-600/20 rounded-full blur-3xl"></div>
    <div class="absolute top-1/3 -right-32 w-96 h-96 bg-pink-500/15 rounded-full blur-3xl"></div>
    <div class="absolute -bottom-40 left-1/3 w-96 h-96 bg-cyan-500/15 rounded-full blur-3xl"></div>
  </div>  <!-- Navbar -->  <header class="relative z-20">
    <nav class="max-w-7xl mx-auto px-4 sm:px-6 py-5">  <div class="glass rounded-2xl px-5 py-4 flex items-center justify-between">

    <!-- Logo -->
    <div class="flex items-center gap-3">
      <div class="w-11 h-11 rounded-xl bg-gradient-to-br from-indigo-500 via-purple-500 to-pink-500 flex items-center justify-center font-black text-xl shadow-lg">
        A
      </div>

      <div>
        <h1 class="font-bold text-lg">ABIR</h1>
        <p class="text-xs text-white/50">Creative Space</p>
      </div>
    </div>

    <!-- Desktop Menu -->
    <div class="hidden md:flex items-center gap-2">
      <a href="#" class="nav-link px-4 py-2 rounded-xl text-sm text-white/80">Home</a>
      <a href="#" class="nav-link px-4 py-2 rounded-xl text-sm text-white/80">Projects</a>
      <a href="#" class="nav-link px-4 py-2 rounded-xl text-sm text-white/80">About</a>
      <a href="#" class="nav-link px-4 py-2 rounded-xl text-sm text-white/80">Contact</a>
    </div>

    <!-- Button -->
    <button
      onclick="showMessage()"
      class="hidden sm:block px-5 py-2.5 rounded-xl bg-white text-black font-semibold text-sm hover:scale-105 transition">
      Get Started
    </button>

    <!-- Mobile Button -->
    <button
      onclick="toggleMenu()"
      class="md:hidden w-11 h-11 rounded-xl glass flex items-center justify-center text-xl">
      ☰
    </button>
  </div>

  <!-- Mobile Menu -->
  <div id="mobileMenu" class="hidden glass rounded-2xl mt-3 p-3 md:hidden">
    <a href="#" class="block p-3 rounded-xl hover:bg-white/10">Home</a>
    <a href="#" class="block p-3 rounded-xl hover:bg-white/10">Projects</a>
    <a href="#" class="block p-3 rounded-xl hover:bg-white/10">About</a>
    <a href="#" class="block p-3 rounded-xl hover:bg-white/10">Contact</a>
  </div>

</nav>

  </header>  <!-- Hero -->  <main class="relative z-10 max-w-7xl mx-auto px-4 sm:px-6 pt-10 pb-20"><section class="grid lg:grid-cols-2 gap-8 items-center">

  <!-- Left -->
  <div>

    <div class="inline-flex items-center gap-2 glass px-4 py-2 rounded-full mb-6">
      <span class="w-2.5 h-2.5 bg-green-400 rounded-full animate-pulse"></span>
      <span class="text-sm text-white/70">Everything is ready</span>
    </div>

    <h2 class="text-5xl sm:text-6xl lg:text-7xl font-black leading-tight">
      Build Your
      <span class="block bg-gradient-to-r from-indigo-400 via-purple-400 to-pink-400 bg-clip-text text-transparent">
        Dream Design
      </span>
    </h2>

    <p class="mt-6 text-white/60 text-base sm:text-lg leading-8 max-w-xl">
      A modern, beautiful and fully responsive interface
      designed for every screen size. Fast, clean and easy
      to customize.
    </p>

    <div class="flex flex-wrap gap-4 mt-8">

      <button
        onclick="showMessage()"
        class="px-7 py-3.5 rounded-2xl bg-gradient-to-r from-indigo-500 to-purple-600 font-bold shadow-lg hover:scale-105 transition">
        Explore Now →
      </button>

      <button
        onclick="showMessage()"
        class="px-7 py-3.5 rounded-2xl glass font-semibold hover:bg-white/15 transition">
        Learn More
      </button>

    </div>

  </div>


  <!-- Right Preview -->
  <div class="relative">

    <div class="glass glow rounded-[2rem] p-4 sm:p-6 animate-float">

      <!-- Fake Browser -->
      <div class="rounded-3xl bg-black/30 overflow-hidden border border-white/10">

        <div class="px-5 py-4 border-b border-white/10 flex items-center gap-2">
          <span class="w-3 h-3 rounded-full bg-red-400"></span>
          <span class="w-3 h-3 rounded-full bg-yellow-400"></span>
          <span class="w-3 h-3 rounded-full bg-green-400"></span>

          <div class="ml-4 flex-1 h-7 rounded-lg bg-white/5"></div>
        </div>

        <div class="p-5">

          <div class="flex items-center justify-between mb-6">
            <div>
              <div class="w-28 h-3 bg-white/20 rounded mb-2"></div>
              <div class="w-40 h-2 bg-white/10 rounded"></div>
            </div>

            <div class="w-10 h-10 rounded-xl bg-gradient-to-br from-purple-500 to-pink-500"></div>
          </div>

          <div class="grid grid-cols-2 gap-4">

            <div class="card glass rounded-2xl p-5">
              <div class="text-3xl mb-3">🚀</div>
              <div class="text-2xl font-bold">98%</div>
              <div class="text-xs text-white/40 mt-1">Performance</div>
            </div>

            <div class="card glass rounded-2xl p-5">
              <div class="text-3xl mb-3">⚡</div>
              <div class="text-2xl font-bold">Fast</div>
              <div class="text-xs text-white/40 mt-1">Experience</div>
            </div>

          </div>

          <div class="glass rounded-2xl mt-4 p-5">

            <div class="flex justify-between mb-4">
              <span class="text-sm text-white/60">Activity</span>
              <span class="text-sm text-green-400">+24%</span>
            </div>

            <div class="flex items-end gap-2 h-28">

              <div class="flex-1 bg-indigo-500/30 rounded-t-lg h-[35%]"></div>
              <div class="flex-1 bg-indigo-500/40 rounded-t-lg h-[55%]"></div>
              <div class="flex-1 bg-purple-500/50 rounded-t-lg h-[45%]"></div>
              <div class="flex-1 bg-purple-500/60 rounded-t-lg h-[70%]"></div>
              <div class="flex-1 bg-pink-500/70 rounded-t-lg h-[90%]"></div>
              <div class="flex-1 bg-pink-500 rounded-t-lg h-[75%]"></div>

            </div>

          </div>

        </div>
      </div>

    </div>

    <!-- Floating Card -->
    <div class="absolute -bottom-5 -left-3 sm:-left-8 glass rounded-2xl p-4 animate-pulseSlow">
      <div class="flex items-center gap-3">
        <div class="w-10 h-10 rounded-xl bg-green-500/20 flex items-center justify-center">
          ✓
        </div>
        <div>
          <p class="font-semibold text-sm">Project Ready</p>
          <p class="text-xs text-white/40">Successfully completed</p>
        </div>
      </div>
    </div>

  </div>

</section>


<!-- Feature Cards -->
<section class="grid sm:grid-cols-2 lg:grid-cols-3 gap-5 mt-20">

  <div class="card glass rounded-3xl p-6">
    <div class="w-12 h-12 rounded-2xl bg-indigo-500/20 flex items-center justify-center text-2xl">
      🎨
    </div>
    <h3 class="text-xl font-bold mt-5">Beautiful Design</h3>
    <p class="text-white/50 mt-2 leading-7">
      Modern visual design with smooth effects and clean spacing.
    </p>
  </div>

  <div class="card glass rounded-3xl p-6">
    <div class="w-12 h-12 rounded-2xl bg-purple-500/20 flex items-center justify-center text-2xl">
      📱
    </div>
    <h3 class="text-xl font-bold mt-5">Fully Responsive</h3>
    <p class="text-white/50 mt-2 leading-7">
      Works smoothly on mobile, tablet, laptop and desktop.
    </p>
  </div>

  <div class="card glass rounded-3xl p-6 sm:col-span-2 lg:col-span-1">
    <div class="w-12 h-12 rounded-2xl bg-pink-500/20 flex items-center justify-center text-2xl">
      ⚡
    </div>
    <h3 class="text-xl font-bold mt-5">Fast Experience</h3>
    <p class="text-white/50 mt-2 leading-7">
      Lightweight structure with smooth animations and interactions.
    </p>
  </div>

</section>

  </main>  <!-- Footer -->  <footer class="relative z-10 border-t border-white/10">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 py-7 text-center text-sm text-white/40">
      © 2026 ABIR. All rights reserved.
    </div>
  </footer>  <!-- JavaScript -->  <script>
    function toggleMenu() {
      const menu = document.getElementById("mobileMenu");
      menu.classList.toggle("hidden");
    }

    function showMessage() {
      alert("Welcome! Your project is ready 🚀");
    }
  </script></body>
</html>
