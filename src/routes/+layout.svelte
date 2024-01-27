<script>
	import './style.css';
	import Nav from './Nav.svelte';
	import Footer from './Footer.svelte';
</script>

<div class="app">
	<Nav />

	<content>
		<slot />
	</content>

	<Footer />
</div>

<style>
	.app {
		display: flex;
		flex-direction: column;
		min-height: 100vh;
	}

	content {
		display: flex;
		flex-direction: column;
		justify-content: flex-end;
		flex: 1;
	}
</style>
