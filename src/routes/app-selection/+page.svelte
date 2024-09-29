<script>
	import { selectedOS } from '$lib/stores/appState';

	let os;
	selectedOS.subscribe((value) => {
		os = value;
	});
</script>

<div class="container mx-auto p-4">
	<h2 class="text-2xl font-bold mb-4">Select Applications for {os ? os.name : 'Your OS'}</h2>
	<p>This page is under construction. You selected: {os ? os.name : 'No OS selected'}</p>
</div>
