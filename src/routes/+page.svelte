<script>
	import { goto } from '$app/navigation';

	function startSelection() {
		goto('/os-selection');
	}
</script>

<div class="container mx-auto p-4">
	<h1 class="text-3xl font-bold mb-4">Install Script Generator</h1>
	<p class="mb-4">
		Welcome to the Install Script Generator. Choose your operating system to get started.
	</p>
	<button
		on:click={startSelection}
		class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded"
	>
		Start
	</button>
</div>
