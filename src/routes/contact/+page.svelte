<script lang="ts">
	let name = '';
	let email = '';
	let message = '';

	function submitForm(e: Event) {
		e.preventDefault();
		// fallback: open mail client with prefilled subject/body
		const subject = encodeURIComponent(`Contatto da sito — ${name}`);
		const body = encodeURIComponent(`Nome: ${name}%0AEmail: ${email}%0A%0A${message}`);
		window.location.href = `mailto:alma@example.com?subject=${subject}&body=${body}`;
	}
</script>

<div class="container mx-auto px-6 py-12">
	<div class="max-w-5xl mx-auto bg-white shadow rounded-lg overflow-hidden">
		<div class="grid grid-cols-1 md:grid-cols-2">
			<!-- Left: contact info (KVK-inspired clean box) -->
			<aside class="p-8 bg-gray-50">
				<h1 class="text-2xl font-semibold mb-2">Contattami</h1>
				<p class="text-sm text-gray-600 mb-6">Per informazioni sul progetto "Arte terapia" o per prenotare un incontro, puoi usare il modulo o i contatti diretti qui sotto.</p>

				<div class="space-y-4">
					<div>
						<h3 class="text-xs text-gray-500 uppercase">Email</h3>
						<a href="mailto:alma@example.com" class="text-emerald-600">alma@example.com</a>
					</div>

					<div>
						<h3 class="text-xs text-gray-500 uppercase">Telefono</h3>
						<a href="tel:+391234567890" class="text-gray-800">+39 123 456 7890</a>
					</div>

					<div>
						<h3 class="text-xs text-gray-500 uppercase">Indirizzo</h3>
						<address class="not-italic text-gray-800">Via Esempio 12<br/>20100 Milano, Italia</address>
					</div>

					<div>
						<h3 class="text-xs text-gray-500 uppercase">Orari</h3>
						<p class="text-gray-800">Lun-Ven: 09:00 — 18:00<br/>Sabato: su appuntamento</p>
					</div>
				</div>

				<div class="mt-6">
					<h3 class="text-xs text-gray-500 uppercase mb-2">Dove trovarmi</h3>
					<div class="w-full h-40 bg-white rounded border flex items-center justify-center text-sm text-gray-400">Mappa placeholder</div>
				</div>
			</aside>

			<!-- Right: contact form -->
			<main class="p-8">
				<h2 class="text-lg font-medium mb-4">Invia un messaggio</h2>

				<form on:submit|preventDefault={submitForm} class="space-y-4">
					<div>
						<label class="block text-sm text-gray-700 mb-1" for="name">Nome</label>
						<input id="name" class="w-full border rounded px-3 py-2" bind:value={name} required />
					</div>

					<div>
						<label class="block text-sm text-gray-700 mb-1" for="email">Email</label>
						<input id="email" type="email" class="w-full border rounded px-3 py-2" bind:value={email} required />
					</div>

					<div>
						<label class="block text-sm text-gray-700 mb-1" for="message">Messaggio</label>
						<textarea id="message" rows="6" class="w-full border rounded px-3 py-2" bind:value={message} required></textarea>
					</div>

					<div class="flex items-center space-x-3">
						<button type="submit" class="bg-emerald-500 hover:bg-emerald-600 text-white px-4 py-2 rounded">Invia via email</button>
						<a href="mailto:alma@example.com" class="text-sm text-gray-600">Oppure invia direttamente una mail</a>
					</div>
				</form>

				<p class="mt-6 text-xs text-gray-500">I dati inviati non verranno condivisi. Rispondo generalmente entro 48 ore.</p>
			</main>
		</div>
	</div>
</div>

