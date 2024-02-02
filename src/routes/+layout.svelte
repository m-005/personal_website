<script>
	import { injectSpeedInsights } from '@vercel/speed-insights/sveltekit';
	import './style.css';
	import Nav from './Nav.svelte';
	import Footer from './Footer.svelte';
	import Home from './Home.svelte';

	injectSpeedInsights();
</script>

<div class="app">
	<Nav />

	<div class="content">
		<slot />
	</div>

	<Home />
	<Footer />
</div>

<style>
	.app {
		display: flex;
		flex-direction: column;
		padding: var(--default-padding);
		box-sizing: border-box; /* Include padding in element's total height */
		height: 100vh;
	}

	.content {
		display: flex;
		flex-direction: column;
		justify-content: flex-end;
		max-width: 60%;
		flex-grow: 1;
	}
</style>
