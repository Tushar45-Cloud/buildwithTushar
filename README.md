# buildwithTushar
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>buildwithTushar • Portfolio</title>
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@200;300;400;500;600;700&display=swap" rel="stylesheet">
  <script src="https://cdn.tailwindcss.com"></script>
  <script src="https://unpkg.com/lucide@latest"></script>
  <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
</head>

<body class="font-[Inter] bg-zinc-900 text-zinc-100 antialiased selection:bg-indigo-500/60">
  <!-- Skip link -->
  <a href="#main" class="sr-only focus:not-sr-only absolute top-2 left-2 bg-indigo-600 text-sm px-3 py-2 rounded-md z-50">Skip to content</a>

  <!-- NAV -->
  <header class="sticky top-0 z-40 backdrop-blur bg-zinc-900/70 border-b border-zinc-800">
    <div class="max-w-7xl mx-auto flex items-center justify-between px-6 py-4">
      <h1 class="text-lg font-semibold tracking-tight"><a href="#" aria-label="Home">TUSHAR BANSODE</a></h1>

      <nav aria-label="Main" class="hidden md:flex gap-10 text-sm font-medium">
        <a href="#about" class="hover:text-indigo-400 transition-colors">About</a>
        <a href="#skills" class="hover:text-indigo-400 transition-colors">Skills</a>
        <a href="#projects" class="hover:text-indigo-400 transition-colors">Projects</a>
        <a href="#contact" class="hover:text-indigo-400 transition-colors">Contact</a>
      </nav>

      <button id="menu-btn" aria-label="Open mobile menu" class="md:hidden p-2 rounded hover:bg-zinc-800/50 focus:outline-none focus:ring-2 focus:ring-indigo-500">
        <i data-lucide="menu" class="w-6 h-6"></i>
      </button>
    </div>

    <!-- Mobile nav -->
    <div id="mobile-nav" class="hidden flex-col px-6 pb-8 md:hidden space-y-4">
      <a href="#about" class="block py-1 hover:text-indigo-400">About</a>
      <a href="#skills" class="block py-1 hover:text-indigo-400">Skills</a>
      <a href="#projects" class="block py-1 hover:text-indigo-400">Projects</a>
      <a href="#contact" class="block py-1 hover:text-indigo-400">Contact</a>
    </div>
  </header>

  <main id="main">
    <!-- HERO -->
    <section class="relative flex flex-col-reverse md:flex-row items-center max-w-7xl mx-auto px-6 pt-20 md:pt-32 pb-32">
      <!-- Text -->
      <div class="w-full md:w-1/2 space-y-8 reveal">
        <h2 class="text-5xl lg:text-6xl font-semibold tracking-tight leading-tight">
          Hey, I’m <span class="text-indigo-500">Tushar</span>
        </h2>
        <p class="text-zinc-400 max-w-md">
          Full-stack engineer crafting performant & accessible web products with TypeScript, Go, and modern tooling.
        </p>
        <div class="flex gap-4 pt-2">
          <a href="#projects" class="px-6 py-3 rounded-md bg-indigo-600 hover:bg-indigo-500 font-medium transition-colors focus:outline-none focus:ring-2 focus:ring-indigo-500">See work</a>
          <a href="#contact" class="px-6 py-3 rounded-md border border-zinc-700 hover:bg-zinc-800 font-medium transition-colors focus:outline-none focus:ring-2 focus:ring-indigo-500">Get in touch</a>
        </div>
      </div>

      <!-- Image -->
      <div class="w-full md:w-1/2 mb-12 md:mb-0 relative reveal delay-150">
        <img src="https://images.unsplash.com/photo-1621619856624-42fd193a0661?auto=format&fit=crop&w=900&q=80"
             alt="Portrait of Tushar Bansode" class="w-full h-[26rem] md:h-[32rem] object-cover rounded-xl shadow-xl">
        <div class="absolute -inset-1 bg-indigo-600 opacity-40 blur rounded-xl -z-10"></div>
      </div>
    </section>

    <!-- ABOUT -->
    <section id="about" class="border-t border-zinc-800 py-24 px-6">
      <div class="max-w-4xl mx-auto space-y-6 reveal">
        <h3 class="text-3xl font-semibold tracking-tight">About me</h3>
        <p class="text-zinc-400 leading-relaxed">
          I’ve spent the last 4+ years building resilient back-ends, polished UIs, and delighting users. I favor clean architecture,
          accessible design, and collaboration. When I’m not coding, you’ll find me sketching UI concepts or exploring the latest dev-ops toys.
        </p>
      </div>
    </section>

    <!-- SKILLS -->
    <section id="skills" class="border-t border-zinc-800 py-24 px-6">
      <div class="max-w-7xl mx-auto grid md:grid-cols-2 gap-20">
        <div class="space-y-6 reveal">
          <h3 class="text-3xl font-semibold tracking-tight">Skill snapshot</h3>
          <p class="text-zinc-400">Here’s a quick glance at the tools I wield most often.</p>
        </div>

        <div class="reveal delay-150 justify-self-center">
          <div class="relative w-72 h-72">
            <canvas id="skillsChart" class="absolute inset-0"></canvas>
            <p class="absolute inset-0 flex items-center justify-center text-xl font-medium">Proficiency</p>
          </div>
        </div>
      </div>
    </section>

    <!-- PROJECTS -->
    <section id="projects" class="border-t border-zinc-800 py-24 px-6">
      <div class="max-w-7xl mx-auto">
        <h3 class="text-3xl font-semibold tracking-tight mb-12 reveal">Selected projects</h3>

        <div class="grid sm:grid-cols-2 lg:grid-cols-3 gap-10">
          <!-- Card -->
          <article class="group relative rounded-xl overflow-hidden border border-zinc-700 hover:border-indigo-500 transition-colors reveal">
            <img src="https://images.unsplash.com/photo-1542744173-8e7e53415bb0?auto=format&fit=crop&w=800&q=80"
                 alt="Realtime Chat App preview" class="object-cover h-44 w-full">
            <div class="p-6 space-y-3 bg-zinc-800/50 backdrop-blur">
              <h4 class="font-semibold group-hover:text-indigo-400 transition-colors">Realtime Chat App</h4>
              <p class="text-sm text-zinc-400">Socket.io chat with auth & offline mode.</p>
              <a href="#" class="inline-flex items-center text-indigo-400 text-sm hover:text-indigo-300">
                Visit <i data-lucide="arrow-up-right" class="w-4 h-4 ml-1"></i>
              </a>
            </div>
          </article>
          <!-- Card -->
          <article class="group relative rounded-xl overflow-hidden border border-zinc-700 hover:border-indigo-500 transition-colors reveal delay-150">
            <img src="https://images.unsplash.com/photo-1642615835477-d303d7dc9ee9?auto=format&fit=crop&w=800&q=80"
                 alt="E-commerce Platform preview" class="object-cover h-44 w-full">
            <div class="p-6 space-y-3 bg-zinc-800/50 backdrop-blur">
              <h4 class="font-semibold group-hover:text-indigo-400 transition-colors">E-commerce Platform</h4>
              <p class="text-sm text-zinc-400">Headless storefront with serverless backend.</p>
              <a href="#" class="inline-flex items-center text-indigo-400 text-sm hover:text-indigo-300">
                Visit <i data-lucide="arrow-up-right" class="w-4 h-4 ml-1"></i>
              </a>
            </div>
          </article>
          <!-- Card -->
          <article class="group relative rounded-xl overflow-hidden border border-zinc-700 hover:border-indigo-500 transition-colors reveal delay-300">
            <img src="https://images.unsplash.com/photo-1635151227785-429f420c6b9d?auto=format&fit=crop&w=800&q=80"
                 alt="Analytics Dashboard preview" class="object-cover h-44 w-full">
            <div class="p-6 space-y-3 bg-zinc-800/50 backdrop-blur">
              <h4 class="font-semibold group-hover:text-indigo-400 transition-colors">Analytics Dashboard</h4>
              <p class="text-sm text-zinc-400">Visualizing big data with custom widgets.</p>
              <a href="#" class="inline-flex items-center text-indigo-400 text-sm hover:text-indigo-300">
                Visit <i data-lucide="arrow-up-right" class="w-4 h-4 ml-1"></i>
              </a>
            </div>
          </article>
        </div>
      </div>
    </section>

    <!-- CONTACT -->
    <section id="contact" class="border-t border-zinc-800 py-24 px-6">
      <div class="max-w-4xl mx-auto">
        <h3 class="text-3xl font-semibold tracking-tight mb-10 reveal">Let’s connect</h3>

        <form action="#" class="space-y-8">
          <div class="grid md:grid-cols-2 gap-6 reveal">
            <label class="w-full">
              <span class="sr-only">Name</span>
              <input type="text" placeholder="Name" required
                     class="w-full bg-zinc-800/50 border border-zinc-700 rounded-md px-4 py-3 placeholder-zinc-500 focus:outline-none focus:border-indigo-500 focus:ring-2 focus:ring-indigo-500">
            </label>
            <label class="w-full">
              <span class="sr-only">Email</span>
              <input type="email" placeholder="Email" required
                     class="w-full bg-zinc-800/50 border border-zinc-700 rounded-md px-4 py-3 placeholder-zinc-500 focus:outline-none focus:border-indigo-500 focus:ring-2 focus:ring-indigo-500">
            </label>
          </div>

          <label class="w-full block reveal delay-150">
            <span class="sr-only">Message</span>
            <textarea rows="5" placeholder="Message"
                      class="w-full bg-zinc-800/50 border border-zinc-700 rounded-md px-4 py-3 placeholder-zinc-500 focus:outline-none focus:border-indigo-500 focus:ring-2 focus:ring-indigo-500"></textarea>
          </label>

          <button type="submit"
                  class="px-8 py-3 bg-indigo-600 hover:bg-indigo-500 rounded-md font-medium transition-colors focus:outline-none focus:ring-2 focus:ring-indigo-500 reveal delay-300">
            Send message
          </button>
        </form>

        <!-- socials -->
        <div class="flex gap-8 mt-14 reveal delay-500">
          <a href="https://github.com" aria-label="GitHub" target="_blank"
             class="hover:text-indigo-400 focus:outline-none focus:ring-2 focus:ring-indigo-500 rounded">
            <i data-lucide="github" class="w-6 h-6"></i>
          </a>
          <a href="https://linkedin.com" aria-label="LinkedIn" target="_blank"
             class="hover:text-indigo-400 focus:outline-none focus:ring-2 focus:ring-indigo-500 rounded">
            <i data-lucide="linkedin" class="w-6 h-6"></i>
          </a>
          <a href="mailto:email@example.com" aria-label="Email"
             class="hover:text-indigo-400 focus:outline-none focus:ring-2 focus:ring-indigo-500 rounded">
            <i data-lucide="mail" class="w-6 h-6"></i>
          </a>
        </div>
      </div>
    </section>
  </main>

  <!-- FOOTER -->
  <footer class="border-t border-zinc-800 py-8 text-center text-sm text-zinc-500">
    © <span id="year"></span> Tushar Bansode. All rights reserved.
  </footer>

  <!-- SCRIPTS -->
  <script>
    // Mobile nav
    const menuBtn = document.getElementById('menu-btn');
    const mobileNav = document.getElementById('mobile-nav');
    menuBtn.addEventListener('click', () => mobileNav.classList.toggle('hidden'));

    // Reveal intersection
    const reveals = document.querySelectorAll('.reveal');
    const io = new IntersectionObserver(entries => {
      entries.forEach(e => {
        if (e.isIntersecting) {
          e.target.classList.remove('opacity-0', 'translate-y-10');
          io.unobserve(e.target);
        }
      });
    }, { threshold: 0.15 });
    reveals.forEach(el => {
      el.classList.add('opacity-0', 'translate-y-10', 'transition-all', 'duration-700');
      io.observe(el);
    });

    // Icons
    lucide.createIcons();

    // Year
    document.getElementById('year').textContent = new Date().getFullYear();

    // Chart
    const ctx = document.getElementById('skillsChart');
    new Chart(ctx, {
      type: 'doughnut',
      data: {
        labels: ['JavaScript', 'TypeScript', 'React', 'Node.js', 'Go'],
        datasets: [{
          data: [90, 84, 82, 75, 65],
          backgroundColor: ['#6366f1', '#818cf8', '#a5b4fc', '#c7d2fe', '#e0e7ff'],
          borderWidth: 0
        }]
      },
      options: { plugins: { legend: { display: false } }, cutout: '73%' }
    });
  </script>
</body>
</html>
