<script lang="ts">
  let open = false;
</script>

<div id="top" class="min-h-screen flex flex-col">
  <!-- 0 - Gradient bar -->
  <div class="h-[5px] bg-gradient-to-r from-emerald-500 to-yellow-400"></div>

  <!-- 1 - Navbar -->
  <nav class="flex items-center justify-between px-6 py-4">
    <div class="flex items-center space-x-3">
      <!-- simple logo -->
      <div class="w-10 h-10 bg-black rounded-sm flex items-center justify-center text-white font-bold">AP</div>
      <span class="font-semibold">Alma Perissinotti</span>
    </div>

    <div class="hidden md:flex items-center space-x-4">
      <a href="#" class="text-sm">Work</a>
      <a href="/contact" class="text-sm">Contact</a>
    </div>

    <!-- burger menu -->
    <button class="md:hidden p-2" on:click={() => (open = !open)} aria-label="menu">
      <svg width="28" height="28" viewBox="0 0 24 24" fill="none" stroke="currentColor" class="text-gray-800">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
      </svg>
    </button>
  </nav>

  <!-- mobile menu -->
  {#if open}
    <div class="md:hidden px-6 pb-4 space-y-2">
      <a href="#" class="block">Work</a>
      <a href="/contact" class="block">Contact</a>
    </div>
  {/if}

  <!-- 2 - Hero full screen background with left card -->
  <header class="flex-1 relative">
    <div class="absolute inset-0 bg-cover bg-center" style="background-image: url('/images/hero.svg');"></div>
    <div class="absolute inset-0 bg-black/30"></div>

    <div class="relative z-10 container mx-auto h-full flex items-start">
      <div class="mt-24 max-w-md bg-white/80 backdrop-blur-sm p-6 rounded-lg shadow-lg m-6">
        <h1 class="text-2xl font-bold mb-2">Arte terapia</h1>
        <p class="text-sm mb-4">Un percorso creativo per ritrovare equilibrio e espressione interiore attraverso l'arte.</p>
        <a href="/contact" class="inline-block bg-emerald-500 hover:bg-emerald-600 text-white py-2 px-4 rounded">Scopri di più</a>
      </div>
    </div>
  </header>

  <!-- 3 - Social proof -->
  <section class="container mx-auto py-16 px-6">
    <h2 class="text-center text-xl font-semibold mb-8">Testimonianze</h2>
    <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
      <article class="bg-white rounded-lg shadow p-6 flex flex-col items-center text-center">
        <img src="/images/person1.svg" alt="persona 1" class="w-24 h-24 rounded-full mb-4" />
        <strong>Giulia R.</strong>
        <p class="text-sm mt-2 text-gray-700">"Partecipare al laboratorio è stato un cambio di prospettiva: ho ritrovato serenità e creatività."</p>
      </article>

      <article class="bg-white rounded-lg shadow p-6 flex flex-col items-center text-center">
        <img src="/images/person2.svg" alt="persona 2" class="w-24 h-24 rounded-full mb-4" />
        <strong>Marco L.</strong>
        <p class="text-sm mt-2 text-gray-700">"Alma guida con grande umanità. L'arte terapia mi ha aiutato ad aprirmi."</p>
      </article>

      <article class="bg-white rounded-lg shadow p-6 flex flex-col items-center text-center">
        <img src="/images/person3.svg" alt="persona 3" class="w-24 h-24 rounded-full mb-4" />
        <strong>Sara Pa.</strong>
        <p class="text-sm mt-2 text-gray-700">"Atmosfera calda e accogliente, tecniche semplici e trasformative."</p>
      </article>
    </div>
  </section>

  <!-- 4 - Footer -->
  <footer class="bg-gray-100 py-8 mt-auto">
    <div class="container mx-auto px-6 text-center">
      <p class="mb-4">Contatti: <a href="mailto:alma@example.com" class="text-emerald-600">alma@example.com</a></p>
      <a href="#top" class="inline-block bg-gray-200 hover:bg-gray-300 py-2 px-4 rounded">Torna su</a>
    </div>
  </footer>
</div>