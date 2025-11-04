    <!-- 0 - Gradient bar -->
  <div class="h-[5px] bg-linear-to-tr from-emerald-300 to-emerald-200"></div>        


  <!-- 1 - Navbar -->
  <nav class="relative z-20 flex items-center justify-between px-6 py-4">
    <div class="flex items-center space-x-3">
      <!-- simple logo -->
      <div class="w-10 h-10 bg-black rounded-sm flex items-center justify-center text-white font-bold">AP</div>
      <a href="/">
         <span class="font-semibold">Alma Perissinotti</span>
      </a>
    </div>

    <div class="hidden md:flex items-center space-x-4">
      <!-- Desktop dropdown for Work -->
      <div class="relative group">
        <button class="text-sm font-medium flex items-center space-x-2">
          <span>Work</span>
          <svg class="w-4 h-4" viewBox="0 0 20 20" fill="currentColor"><path d="M5.23 7.21a.75.75 0 011.06.02L10 10.94l3.71-3.71a.75.75 0 111.06 1.06l-4.24 4.24a.75.75 0 01-1.06 0L5.21 8.29a.75.75 0 01.02-1.08z"/></svg>
        </button>

        <div class="absolute right-0 mt-2 w-56 bg-white rounded shadow-lg opacity-0 invisible group-hover:opacity-100 group-hover:visible transform group-hover:translate-y-0 transition-all">
          <a href="/arte-terapia" class="block px-4 py-3 text-sm hover:bg-gray-50">Arte terapia (landing)</a>
          <a href="/workshops/pittura" class="block px-4 py-3 text-sm hover:bg-gray-50">Workshop: Pittura ad olio</a>
          <a href="/workshops/collage" class="block px-4 py-3 text-sm hover:bg-gray-50">Workshop: Collage terapeutico</a>
          <a href="/portfolio" class="block px-4 py-3 text-sm hover:bg-gray-50">Portfolio / Mostre</a>
        </div>
      </div>

      <a href="/contact" class="text-sm">Contact</a>
    </div>

    <!-- burger menu -->
    <button class="md:hidden p-2" on:click={() => (open = !open)} aria-label="menu">
      <svg width="28" height="28" viewBox="0 0 24 24" fill="none" stroke="currentColor" class="text-gray-800">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
      </svg>
    </button>
  </nav>