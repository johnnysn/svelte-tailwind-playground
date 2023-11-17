<script>
	import Sidebar from '$lib/sidebar.svelte';
import '../app.css';
	import '@fontsource/bebas-neue';

	
</script>

<svelte:head>
	<title>Svelte Playground</title>
</svelte:head>

<div class="app-container h-screen relative bg-zinc-900 text-zinc-50">
	<div class="flex flex-col h-screen">
		<main class="flex-1 py-4 pl-20">
			<slot />
		</main>

		<footer class="h-[48px] flex items-center justify-center z-50 bg-zinc-950 text-zinc-50">
			Footer
		</footer>
	</div>

  <Sidebar />
	
</div>

<style>
	.app-container {
		font-family: 'Bebas Neue', sans-serif;
	}
</style>
