<script>
	import Header from '../lib/Header.svelte';
</script>

<main>
	<Header />
	<slot />
</main>

<style>
	main {
		background-color: #232626;
		min-height: 100vh;
	}
</style>
