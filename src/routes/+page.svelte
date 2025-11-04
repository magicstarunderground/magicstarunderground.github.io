<script lang="ts">

  let open = false;
  let workOpen = true; // show examples by default when menu opens
</script>

<div id="top" class="min-h-screen flex flex-col">

  <!-- mobile menu -->
  {#if open}
    <div class="md:hidden px-6 pb-4 space-y-2 relative z-20">
      <div>
        <button class="w-full text-left flex items-center justify-between py-2" on:click={() => (workOpen = !workOpen)} aria-expanded={workOpen}>
          <span class="font-medium">Work</span>
          <svg class="w-5 h-5" viewBox="0 0 20 20" fill="currentColor"><path fill-rule="evenodd" d="M5.23 7.21a.75.75 0 011.06.02L10 10.94l3.71-3.71a.75.75 0 111.06 1.06l-4.24 4.24a.75.75 0 01-1.06 0L5.21 8.29a.75.75 0 01.02-1.08z" clip-rule="evenodd"/></svg>
        </button>

        {#if workOpen}
          <ul class="mt-2 pl-4 space-y-1">
            <li><a href="#arte-terapia" class="block text-sm text-gray-700">Arte terapia (landing)</a></li>
            <li><a href="#workshop-pittura" class="block text-sm text-gray-700">Workshop: Pittura ad olio</a></li>
            <li><a href="#workshop-collage" class="block text-sm text-gray-700">Workshop: Collage terapeutico</a></li>
            <li><a href="#portfolio" class="block text-sm text-gray-700">Portfolio / Mostre</a></li>
          </ul>
        {/if}
      </div>

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