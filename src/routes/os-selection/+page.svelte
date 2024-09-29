<script>
	import { operatingSystems } from '$lib/data/osData';
	import { selectedOS } from '$lib/stores/appState';
	import { goto } from '$app/navigation';

	function selectOS(os) {
		selectedOS.set(os);
		goto('/app-selection');
	}
</script>

<div class="container mx-auto p-4">
	<h2 class="text-2xl font-bold mb-4">Select Your Operating System</h2>
	<div class="grid grid-cols-2 md:grid-cols-4 gap-4">
		{#each operatingSystems as os}
			<button
				on:click={() => selectOS(os)}
				class="p-4 border rounded-lg hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-blue-500"
			>
				<div class="text-4xl mb-2">{os.icon}</div>
				<div>{os.name}</div>
			</button>
		{/each}
	</div>
</div>
