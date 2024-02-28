<script>
	import { injectSpeedInsights } from '@vercel/speed-insights/sveltekit';
	import './style.css';
	import Nav from './Nav.svelte';
	import Footer from './Footer.svelte';
	import Home from './Home.svelte';

	// Vercel Perf widget
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
		padding: 1rem;
		box-sizing: border-box; /* Include padding in element's total height */
		position: absolute;
		inset: 0;
		@media screen and (min-width: 768px) {
			padding: 2rem;
		}
		background-image: repeating-radial-gradient(
			circle at 50% 50%,
			#477e53 5%,
			#08515c 50%,
			#477e53 100%
		);
	}

	.content {
		display: flex;
		flex-direction: column;
		flex-grow: 1;
	}
</style>
