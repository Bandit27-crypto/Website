<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>FUTURE • Enterprise Experience</title>
  <meta name="description" content="Futuristic demo site — modern, professional, mindful design." />
  
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800&display=swap" rel="stylesheet">

  <script src="https://cdn.jsdelivr.net/npm/apexcharts"></script>

  <script>
    tailwind = {
      config: {
        theme: {
          extend: {
            colors: {
              'neon-cyan': '#00F5FF',
              'neon-magenta': '#FF3CA6',
              'midnight-1': '#030418',
              'midnight-2': '#071027',
              'glass': 'rgba(255,255,255,0.06)'
            },
            fontFamily: {
              sans: ['Inter', 'ui-sans-serif', 'system-ui']
            }
          }
        }
      }
    }
  </script>
  <script src="https://cdn.tailwindcss.com"></script>
  
  <style>
    /* Custom styling for ApexCharts tooltip to match the dark theme */
    .apexcharts-tooltip {
      background: #071027 !important;
      border-color: #334155 !important;
      color: #fff;
    }
    .apexcharts-tooltip-title {
      background: #030418 !important;
      border-bottom: 1px solid #334155 !important;
    }
    /* Menambah kelas khusus untuk container lebar, menggunakan max-w-screen-2xl untuk layar ultra-lebar */
    .wide-container {
        max-width: 1536px; /* max-w-screen-2xl */
        margin-left: auto;
        margin-right: auto;
        padding-left: 1.5rem; /* px-6 */
        padding-right: 1.5rem; /* px-6 */
    }
    /* Menyesuaikan padding untuk layar besar */
    @media (min-width: 1280px) { /* xl */
        .wide-container {
            padding-left: 2rem; /* xl:px-8 */
            padding-right: 2rem; /* xl:px-8 */
        }
    }
  </style>
</head>
<body class="antialiased font-sans bg-gradient-to-b from-midnight-1 via-midnight-2 to-black text-slate-100">

  <div class="fixed inset-0 -z-20 pointer-events-none">
    <svg class="w-full h-full" preserveAspectRatio="xMidYMid slice" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1600 900" aria-hidden="true">
      <defs>
        <linearGradient id="g1" x1="0%" y1="0%" x2="100%" y2="100%">
          <stop offset="0%" stop-color="#001122" />
          <stop offset="40%" stop-color="#041234" />
          <stop offset="100%" stop-color="#0b0b1a" />
        </linearGradient>
        <radialGradient id="radA">
          <stop offset="0%" stop-color="#001F3F" stop-opacity="1"/>
          <stop offset="100%" stop-color="#001F3F" stop-opacity="0"/>
        </radialGradient>
        <radialGradient id="radB">
          <stop offset="0%" stop-color="#0ff" stop-opacity="0.10"/>
          <stop offset="100%" stop-color="#f0f" stop-opacity="0"/>
        </radialGradient>
      </defs>
      <rect width="100%" height="100%" fill="url(#g1)"/>
      <ellipse cx="200" cy="120" rx="360" ry="140" fill="url(#radB)">
        <animate attributeName="cx" dur="14s" values="200;400;260;200" repeatCount="indefinite"/>
        <animate attributeName="cy" dur="10s" values="120;80;140;120" repeatCount="indefinite"/>
      </ellipse>
      <ellipse cx="1400" cy="660" rx="420" ry="170" fill="#10254a" opacity="0.12">
        <animate attributeName="cx" dur="18s" values="1400;1200;1360;1400" repeatCount="indefinite"/>
        <animate attributeName="cy" dur="12s" values="660;700;620;660" repeatCount="indefinite"/>
      </ellipse>
      <g opacity="0.02" stroke="#ffffff">
        <line x1="0" y1="50" x2="1600" y2="50" />
        <line x1="0" y1="100" x2="1600" y2="100" />
        <line x1="0" y1="150" x2="1600" y2="150" />
      </g>
    </svg>
  </div>

  <header class="fixed top-0 left-0 right-0 z-40 backdrop-blur-md bg-black/30 border-b border-white/6">
    <div class="wide-container py-4 flex items-center justify-between gap-6">
      <a href="#" class="flex items-center gap-3">
        <svg class="w-10 h-10 rounded-2xl bg-gradient-to-br from-neon-cyan to-neon-magenta p-2 drop-shadow-lg" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
          <rect width="24" height="24" rx="5" fill="white" opacity="0.06"/>
          <path d="M4 12c2.5-6 14-6 16 0" stroke="#00F5FF" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"/>
        </svg>
        <div class="leading-tight">
          <div class="text-sm font-semibold">FUTURE • EXPERIENCE</div>
          <div class="text-xs text-slate-400 -mt-0.5">Enterprise • Design • Velocity</div>
        </div>
      </a>

      <nav class="hidden lg:flex items-center gap-6 text-sm text-slate-300">
        <a href="#market" class="hover:text-white transition text-neon-cyan">Live Market</a>
        <a href="#features" class="hover:text-white transition">Fitur</a>
        <a href="#platform" class="hover:text-white transition">Platform</a>
        <a href="#case" class="hover:text-white transition">Case Study</a>
        <a href="#pricing" class="hover:text-white transition">Harga</a>
      </nav>

      <div class="flex items-center gap-3">
        <button id="demo-btn" class="hidden md:inline-flex items-center gap-2 px-4 py-2 rounded-full bg-gradient-to-r from-neon-cyan to-neon-magenta text-white font-semibold shadow-lg">Minta Demo
        </button>
        <button id="menuToggle" class="lg:hidden p-2 rounded-md bg-white/5">
          <svg class="w-5 h-5" viewBox="0 0 24 24" fill="none" stroke="currentColor"><path d="M4 6h16M4 12h16M4 18h16" stroke-width="1.5" stroke-linecap="round"/></svg>
        </button>
      </div>
    </div>
  </header>

  <div class="h-20"></div>

  <section class="wide-container py-16 lg:py-20">
    <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
      <div class="space-y-6 reveal opacity-0 translate-y-8 transition-all duration-700">
        <p class="inline-flex items-center gap-3 text-sm text-slate-300 font-medium">
          <span class="px-2 py-1 rounded-full bg-white/5 text-xs">Enterprise</span>
          Real-time Data • Scalable
        </p>

        <h1 class="text-4xl md:text-6xl font-extrabold leading-tight tracking-tight">
          Visualisasi Data & <br/><span>Market Intelligence</span>
        </h1>

        <p class="text-lg text-slate-300 max-w-xl">
          Platform terpadu untuk memantau pergerakan market kripto dan saham IHSG dengan latensi ultra-rendah. Akurasi tinggi untuk keputusan cepat.
        </p>

        <div class="flex gap-4 items-center">
          <a href="#market" class="px-6 py-3 rounded-2xl bg-gradient-to-r from-neon-cyan to-neon-magenta text-white font-semibold shadow-xl">Lihat Grafik</a>
          <a href="#case" class="px-5 py-3 rounded-2xl border border-white/10 text-slate-200 hover:bg-white/5 transition">Case Study</a>
        </div>
      </div>

      <div class="reveal opacity-0 translate-y-8 transition-all duration-700">
        <div class="rounded-3xl overflow-hidden border border-white/6 bg-gradient-to-b from-white/6 to-white/3 shadow-2xl p-6">
          <div class="flex items-start justify-between">
            <div>
              <div class="text-xs text-slate-400">Realtime • Dashboard</div>
              <div class="text-2xl font-semibold mt-1">MARKET OVERVIEW</div>
            </div>
            <div class="text-xs text-slate-300">Status: <span class="text-neon-cyan font-semibold animate-pulse">● Live Streaming</span></div>
          </div>

          <div class="mt-6 p-4 rounded-xl bg-black/40 border border-white/5 relative h-48 flex items-center justify-center overflow-hidden">
                         <svg class="w-full h-full absolute bottom-0 left-0" preserveAspectRatio="none" viewBox="0 0 200 100">
                 <path d="M0 80 Q 20 70 40 85 T 80 60 T 120 40 T 160 50 T 200 20" fill="none" stroke="url(#gradLine)" stroke-width="3"/>
                 <defs>
                   <linearGradient id="gradLine" x1="0" y1="0" x2="1" y2="0">
                       <stop offset="0%" stop-color="#00F5FF"/>
                       <stop offset="100%" stop-color="#FF3CA6"/>
                   </linearGradient>
                 </defs>
             </svg>
             <div class="text-center z-10">
                 <div class="text-3xl font-bold tracking-widest">FUTURE<span class="text-neon-cyan">.AI</span></div>
                 <div class="text-xs text-slate-400 mt-1">Processing 1.2M signals/sec</div>
             </div>
          </div>

          <div class="mt-6 grid grid-cols-3 gap-3">
            <div class="p-2 rounded-lg bg-white/3 text-center">
              <div class="text-xs text-slate-300">BTC Dominance</div>
              <div class="font-semibold text-neon-cyan">52.4%</div>
            </div>
            <div class="p-2 rounded-lg bg-white/3 text-center">
              <div class="text-xs text-slate-300">ETH Gas</div>
              <div class="font-semibold text-neon-magenta">14 gwei</div>
            </div>
            <div class="p-2 rounded-lg bg-white/3 text-center">
              <div class="text-xs text-slate-300">IHSG Vol</div>
              <div class="font-semibold text-emerald-400">High</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <section id="market" class="py-12 border-t border-white/6 bg-black/20 relative">
    <div class="absolute top-0 left-0 w-full h-px bg-gradient-to-r from-transparent via-neon-cyan to-transparent opacity-30"></div>
    
    <div class="wide-container">
      <div class="flex items-center justify-between mb-8">
        <h2 class="text-2xl font-bold flex items-center gap-2">
          <span class="w-2 h-8 bg-neon-cyan rounded-full"></span>
          Live Market Intelligence
        </h2>
        <div class="text-xs text-slate-400 flex items-center gap-2">
          <span class="w-2 h-2 bg-red-500 rounded-full animate-pulse"></span> Live Data Feed
        </div>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
        <div class="reveal opacity-0 translate-y-8 transition-all duration-700 p-5 rounded-2xl bg-gradient-to-b from-white/5 to-midnight-2 border border-white/10 shadow-lg hover:border-neon-cyan/50 transition-colors group">
          <div class="flex justify-between items-start mb-2">
            <div class="flex items-center gap-3">
              <div class="w-10 h-10 rounded-full bg-orange-500/20 flex items-center justify-center text-orange-400 font-bold border border-orange-500/30">₿</div>
              <div>
                <div class="font-bold text-lg group-hover:text-neon-cyan transition-colors">Bitcoin</div>
                <div class="text-xs text-slate-400">BTC/USD</div>
              </div>
            </div>
            <div class="text-right">
              <div id="price-btc" class="text-lg font-mono font-bold text-slate-100">$42,105</div>
              <div class="text-xs text-emerald-400 flex justify-end items-center gap-1">▲ 2.4%</div>
            </div>
          </div>
          <div id="chart-btc" class="h-32 -mx-2"></div>
        </div>

        <div class="reveal opacity-0 translate-y-8 transition-all duration-700 delay-100 p-5 rounded-2xl bg-gradient-to-b from-white/5 to-midnight-2 border border-white/10 shadow-lg hover:border-neon-magenta/50 transition-colors group">
          <div class="flex justify-between items-start mb-2">
            <div class="flex items-center gap-3">
              <div class="w-10 h-10 rounded-full bg-purple-500/20 flex items-center justify-center text-purple-400 font-bold border border-purple-500/30">Ξ</div>
              <div>
                <div class="font-bold text-lg group-hover:text-neon-magenta transition-colors">Ethereum</div>
                <div class="text-xs text-slate-400">ETH/USD (Alt)</div>
              </div>
            </div>
            <div class="text-right">
              <div id="price-eth" class="text-lg font-mono font-bold text-slate-100">$2,240</div>
              <div class="text-xs text-emerald-400 flex justify-end items-center gap-1">▲ 1.8%</div>
            </div>
          </div>
          <div id="chart-eth" class="h-32 -mx-2"></div>
        </div>

        <div class="reveal opacity-0 translate-y-8 transition-all duration-700 delay-200 p-5 rounded-2xl bg-gradient-to-b from-white/5 to-midnight-2 border border-white/10 shadow-lg hover:border-emerald-400/50 transition-colors group">
          <div class="flex justify-between items-start mb-2">
            <div class="flex items-center gap-3">
              <div class="w-10 h-10 rounded-full bg-emerald-500/20 flex items-center justify-center text-emerald-400 font-bold border border-emerald-500/30">📈</div>
              <div>
                <div class="font-bold text-lg group-hover:text-emerald-400 transition-colors">IHSG</div>
                <div class="text-xs text-slate-400">JKSE Composite</div>
              </div>
            </div>
            <div class="text-right">
              <div id="price-ihsg" class="text-lg font-mono font-bold text-slate-100">7,120.45</div>
              <div class="text-xs text-red-400 flex justify-end items-center gap-1">▼ 0.2%</div>
            </div>
          </div>
          <div id="chart-ihsg" class="h-32 -mx-2"></div>
        </div>
      </div>
    </div>
  </section>

  <section id="features" class="py-12">
    <div class="wide-container">
        <div class="text-center max-w-3xl mx-auto">
        <h2 class="text-3xl font-bold">Fitur Platform</h2>
        <p class="text-slate-300 mt-3">Rangkaian fitur inti untuk Market Intelligence, kecepatan pengambilan keputusan, dan keunggulan operasional.</p>
        </div>

      <div class="mt-10 grid grid-cols-1 md:grid-cols-3 gap-6">
        <article class="reveal opacity-0 translate-y-8 transition-all duration-700 p-6 rounded-2xl bg-gradient-to-b from-white/4 to-white/2 border border-white/6">
            <div class="flex items-start gap-4">
            <div class="w-12 h-12 rounded-xl bg-white/5 flex items-center justify-center text-2xl">📊</div>
            <div>
              <h3 class="font-semibold text-lg">Visualisasi Real-time</h3>
              <p class="text-slate-300 mt-1 text-sm">Grafik dan dashboard yang diperbarui secara langsung dengan latensi kurang dari 100ms.</p>
            </div>
            </div>
        </article>

        <article class="reveal opacity-0 translate-y-8 transition-all duration-700 delay-100 p-6 rounded-2xl bg-gradient-to-b from-white/4 to-white/2 border border-white/6">
            <div class="flex items-start gap-4">
            <div class="w-12 h-12 rounded-xl bg-white/5 flex items-center justify-center text-2xl">🧠</div>
            <div>
              <h3 class="font-semibold text-lg">AI Anomaly Detection</h3>
              <p class="text-slate-300 mt-1 text-sm">Mendeteksi anomali pergerakan harga secara instan dan memberikan peringatan dini.</p>
            </div>
            </div>
        </article>

        <article class="reveal opacity-0 translate-y-8 transition-all duration-700 delay-200 p-6 rounded-2xl bg-gradient-to-b from-white/4 to-white/2 border border-white/6">
            <div class="flex items-start gap-4">
            <div class="w-12 h-12 rounded-xl bg-white/5 flex items-center justify-center text-2xl">🌐</div>
            <div>
              <h3 class="font-semibold text-lg">Global Data Aggregation</h3>
              <p class="text-slate-300 mt-1 text-sm">Menggabungkan data dari berbagai bursa global, memastikan cakupan market yang komprehensif.</p>
            </div>
            </div>
        </article>
      </div>
    </div>
  </section>

  <section id="platform" class="py-16">
    <div class="wide-container grid grid-cols-1 lg:grid-cols-2 gap-12 items-start">
      <div class="reveal opacity-0 translate-y-8 transition-all duration-700">
        <h3 class="text-2xl font-bold">Platform Arsitektur</h3>
        <p class="text-slate-300 mt-2 max-w-lg">Platform kami dibangun dengan prinsip reliability, developer happiness, dan observability-first.</p>

        <dl class="mt-6 space-y-4">
          <div class="flex gap-4">
            <dt class="w-12 h-12 rounded-lg bg-white/4 flex items-center justify-center text-xl">1</dt>
            <dd>
              <div class="font-semibold">Edge Routing & CDN</div>
              <div class="text-slate-300 text-sm">Penempatan titik-titik entry global untuk mengurangi latensi.</div>
            </dd>
          </div>
          <div class="flex gap-4">
            <dt class="w-12 h-12 rounded-lg bg-white/4 flex items-center justify-center text-xl">2</dt>
            <dd>
              <div class="font-semibold">AI-Assisted Ops</div>
              <div class="text-slate-300 text-sm">Prediksi beban, rekomendasi autoscaling, dan anomaly detection.</div>
            </dd>
          </div>
        </dl>

        <div class="mt-6 flex gap-3">
          <a href="#pricing" class="px-5 py-3 rounded-xl bg-gradient-to-r from-neon-cyan to-neon-magenta text-white font-semibold">Cek Harga & Paket</a>
        </div>
      </div>

      <div class="reveal opacity-0 translate-y-8 transition-all duration-700">
        <div class="rounded-2xl p-6 bg-gradient-to-b from-white/5 to-white/3 border border-white/6 shadow-xl">
          <div class="flex items-center justify-between">
            <div class="text-sm text-slate-300">Environment</div>
            <div class="text-xs text-slate-400">Production • eu-west-1</div>
          </div>
          <div class="mt-4 grid grid-cols-1 xl:grid-cols-2 gap-4">
            <div class="p-4 rounded-lg bg-black/30">
              <div class="text-xs text-slate-300">Latency (p95)</div>
              <div class="text-lg font-semibold mt-1">78 ms</div>
              <div class="mt-3 h-2 w-full bg-white/6 rounded-full overflow-hidden">
                <div class="h-2 rounded-full bg-gradient-to-r from-neon-cyan to-neon-magenta" style="width:78%"></div>
              </div>
            </div>
            <div class="p-4 rounded-lg bg-black/30">
              <div class="text-xs text-slate-300">Error Rate</div>
              <div class="text-lg font-semibold mt-1">0.02%</div>
              <div class="mt-3 h-2 w-full bg-white/6 rounded-full overflow-hidden">
                <div class="h-2 rounded-full bg-gradient-to-r from-red-500 to-orange-400" style="width:2%"></div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <section id="case" class="py-16 border-t border-white/6">
    <div class="wide-container">
      <div class="text-center">
        <h2 class="text-3xl font-bold">Case Studies</h2>
        <p class="text-slate-300 mt-2 max-w-2xl mx-auto">Dampak nyata transformasi digital.</p>
        </div>
        <div class="mt-10 grid grid-cols-1 md:grid-cols-3 gap-6">
          <article class="reveal opacity-0 translate-y-8 transition-all duration-700 p-6 rounded-2xl bg-gradient-to-b from-white/4 to-white/2 border border-white/6">
            <div class="font-semibold">Fintech X</div>
            <p class="text-slate-300 text-sm mt-2">Migrasi ke edge reduced latency by 45% dan throughput naik 3x.</p>
            <div class="mt-4 text-xs text-slate-400">Hasil: +45% perf, -30% cost</div>
          </article>
          <article class="reveal opacity-0 translate-y-8 transition-all duration-700 delay-100 p-6 rounded-2xl bg-gradient-to-b from-white/4 to-white/2 border border-white/6">
            <div class="font-semibold">Retail Z</div>
            <p class="text-slate-300 text-sm mt-2">Integrasi observability meningkatkan MTTR dari 4 jam menjadi 20 menit.</p>
            <div class="mt-4 text-xs text-slate-400">Hasil: MTTR ⬇ 90%</div>
          </article>
          <article class="reveal opacity-0 translate-y-8 transition-all duration-700 delay-200 p-6 rounded-2xl bg-gradient-to-b from-white/4 to-white/2 border border-white/6">
            <div class="font-semibold">Media Y</div>
            <p class="text-slate-300 text-sm mt-2">Autoscaling cerdas menahan peak 20x tanpa downtime saat event besar.</p>
            <div class="mt-4 text-xs text-slate-400">Hasil: 0 downtime saat peak</div>
          </article>
        </div>
      </div>
    </section>

  <section id="pricing" class="py-16 border-t border-white/6">
    <div class="wide-container text-center">
      <h2 class="text-3xl font-bold">Pilih Paket</h2>
      <p class="text-slate-300 mt-2 max-w-2xl mx-auto">Transparan dan dapat diskalakan.</p>

      <div class="mt-6 inline-flex items-center gap-3 bg-white/3 p-1 rounded-full">
        <span class="text-xs text-slate-300 px-3">Bulanan</span>
        <button id="billingToggle" class="relative w-14 h-7 bg-gradient-to-r from-neon-cyan to-neon-magenta rounded-full p-1 shadow-sm" aria-pressed="false" aria-label="Toggle billing">
          <span id="toggleKnob" class="block w-5 h-5 rounded-full bg-black transition-transform duration-300"></span>
        </button>
        <span class="text-xs text-slate-300 px-3">Tahunan (-20%)</span>
      </div>

      <div class="mt-8 grid grid-cols-1 md:grid-cols-3 gap-6">
        <div class="p-6 rounded-2xl bg-white/4 border border-white/6">
          <div class="text-sm text-slate-300">Starter</div>
          <div class="mt-2 text-3xl font-bold price" data-monthly="€29" data-yearly="€23">€29</div>
          <div class="text-xs text-slate-400 mt-2">Per developer / bulan</div>
          <ul class="mt-4 space-y-2 text-sm text-slate-300">
            <li>Edge CDN</li>
            <li>Basic Charts</li>
          </ul>
          <div class="mt-6"><button class="w-full px-4 py-3 rounded-lg bg-white/5">Mulai</button></div>
        </div>

        <div class="p-6 rounded-2xl bg-gradient-to-r from-white/6 to-white/4 border border-white/6 shadow-lg">
          <div class="text-sm text-slate-300">Professional</div>
          <div class="mt-2 text-4xl font-bold price" data-monthly="€99" data-yearly="€79">€99</div>
          <div class="text-xs text-slate-400 mt-2">Dalam paket tim</div>
          <ul class="mt-4 space-y-2 text-sm text-slate-300">
            <li>All Starter features</li>
            <li>Advanced Real-time Charts</li>
            <li>24/7 support</li>
          </ul>
          <div class="mt-6">
            <button class="w-full px-4 py-3 rounded-lg bg-black text-neon-cyan font-semibold">Request Demo</button>
          </div>
        </div>

        <div class="p-6 rounded-2xl bg-white/4 border border-white/6">
          <div class="text-sm text-slate-300">Enterprise</div>
          <div class="mt-2 text-3xl font-bold price" data-monthly="Custom" data-yearly="Custom">Custom</div>
          <div class="text-xs text-slate-400 mt-2">Tailored</div>
          <ul class="mt-4 space-y-2 text-sm text-slate-300">
            <li>Dedicated support</li>
            <li>Multi-region failover</li>
          </ul>
          <div class="mt-6">
            <button class="w-full px-4 py-3 rounded-lg bg-gradient-to-r from-neon-cyan to-neon-magenta text-white font-semibold">Hubungi Sales</button>
          </div>
        </div>
      </div>
    </div>
  </section>

  <footer class="border-t border-white/6 pt-10 pb-16 mt-12">
    <div class="wide-container grid grid-cols-1 md:grid-cols-4 gap-6">
      <div>
        <div class="font-semibold">FUTURE • EXPERIENCE</div>
        <div class="text-slate-400 mt-2 text-sm">Platform modern untuk tim yang serius terhadap kualitas dan performa.</div>
      </div>
      <div>
        <div class="font-semibold">Produk</div>
        <ul class="mt-3 text-sm text-slate-300 space-y-2">
          <li>Platform</li>
          <li>Observability</li>
          <li>Live Market</li>
          </ul>
      </div>
      <div>
        <div class="font-semibold">Company</div>
        <ul class="mt-3 text-sm text-slate-300 space-y-2">
          <li>About</li>
          <li>Careers</li>
        </ul>
      </div>
      <div>
        <div class="font-semibold">Legal</div>
        <ul class="mt-3 text-sm text-slate-300 space-y-2">
          <li>Privacy</li>
          <li>Terms</li>
        </ul>
      </div>
    </div>
    <div class="wide-container mt-8 text-sm text-slate-400">
      <div>© <span id="year"></span> FUTURE • EXPERIENCE — All rights reserved.</div>
    </div>
  </footer>

  <script>
    document.getElementById('year').textContent = new Date().getFullYear();

    // Intersection Observer for Scroll Animations
    document.addEventListener('DOMContentLoaded', () => {
      const observer = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
          if (entry.isIntersecting) {
            entry.target.classList.remove('opacity-0','translate-y-8');
            entry.target.classList.add('opacity-100','translate-y-0');
            observer.unobserve(entry.target);
          }
        });
      }, { threshold: 0.1 });
      document.querySelectorAll('.reveal').forEach(el => observer.observe(el));
    });

    // Billing Toggle Logic (Monthly/Yearly)
    (function() {
      const toggle = document.getElementById('billingToggle');
      const knob = document.getElementById('toggleKnob');
      let yearly = false;
      toggle.addEventListener('click', () => {
        yearly = !yearly;
        // Animasi knob menggunakan CSS transition (transform di style.css/Tailwind config)
        knob.style.transform = yearly ? 'translateX(22px)' : 'translateX(0)';
        toggle.setAttribute('aria-pressed', yearly ? 'true' : 'false');
        document.querySelectorAll('.price').forEach(el => {
          el.textContent = yearly ? el.getAttribute('data-yearly') : el.getAttribute('data-monthly');
        });
      });
    })();
    
    // Function to generate simulated market data
    function generateData(count, min, max) {
      let data = [];
      let prev = (min + max) / 2;
      for(let i=0; i<count; i++) {
        let move = (Math.random() - 0.5) * (max - min) * 0.1;
        let val = prev + move;
        if(val < min) val = min;
        if(val > max) val = max;
        data.push(val);
        prev = val;
      }
      return data;
    }

    // Common options for ApexCharts sparklines
    const commonOptions = {
      chart: {
        type: 'area',
        height: 120,
        sparkline: { enabled: true },
        animations: { enabled: true, easing: 'linear', dynamicAnimation: { speed: 1000 } }
      },
      stroke: { curve: 'smooth', width: 2 },
      fill: { type: 'gradient', gradient: { shadeIntensity: 1, opacityFrom: 0.4, opacityTo: 0.05, stops: [0, 100] } },
      tooltip: { fixed: { enabled: false }, x: { show: false }, y: { title: { formatter: () => '' } }, marker: { show: false } }
    };

    // Initialize BTC Chart
    const btcData = generateData(20, 40000, 43000);
    const chartBTC = new ApexCharts(document.querySelector("#chart-btc"), {
      ...commonOptions,
      series: [{ name: 'Bitcoin', data: btcData }],
      colors: ['#00F5FF']
    });
    chartBTC.render();

    // Initialize ETH Chart
    const ethData = generateData(20, 2000, 2400);
    const chartETH = new ApexCharts(document.querySelector("#chart-eth"), {
      ...commonOptions,
      series: [{ name: 'Ethereum', data: ethData }],
      colors: ['#FF3CA6']
    });
    chartETH.render();

    // Initialize IHSG Chart
    const ihsgData = generateData(20, 7000, 7200);
    const chartIHSG = new ApexCharts(document.querySelector("#chart-ihsg"), {
      ...commonOptions,
      series: [{ name: 'IHSG', data: ihsgData }],
      colors: ['#34D399']
    });
    chartIHSG.render();

    // Live Data Update Simulation
    setInterval(() => {
      // BTC Update
      const lastBtc = btcData[btcData.length-1];
      const newBtc = lastBtc + (Math.random() - 0.5) * 200;
      btcData.push(newBtc);
      btcData.shift();
      chartBTC.updateSeries([{ data: btcData }]);
      document.getElementById('price-btc').innerText = '$' + Math.floor(newBtc).toLocaleString();

      // ETH Update
      const lastEth = ethData[ethData.length-1];
      const newEth = lastEth + (Math.random() - 0.5) * 20;
      ethData.push(newEth);
      ethData.shift();
      chartETH.updateSeries([{ data: ethData }]);
      document.getElementById('price-eth').innerText = '$' + Math.floor(newEth).toLocaleString();

      // IHSG Update
      const lastIhsg = ihsgData[ihsgData.length-1];
      const newIhsg = lastIhsg + (Math.random() - 0.5) * 15;
      ihsgData.push(newIhsg);
      ihsgData.shift();
      chartIHSG.updateSeries([{ data: ihsgData }]);
      document.getElementById('price-ihsg').innerText = newIhsg.toFixed(2).toLocaleString();
    }, 1500); 
  </script>
</body>
</html>
