<script>
	import { injectSpeedInsights } from '@vercel/speed-insights/sveltekit';
	import './style.css';
	import Nav from './Nav.svelte';
	import Footer from './Footer.svelte';

	injectSpeedInsights();
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
		max-width: 70%;
		padding: 4rem;
	}
</style>
