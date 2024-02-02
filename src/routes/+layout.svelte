<script>
	import { injectSpeedInsights } from '@vercel/speed-insights/sveltekit';
	import './style.css';
	import Nav from './Nav.svelte';
	import Footer from './Footer.svelte';
	import Home from './Home.svelte';
	import { onMount } from 'svelte';

	// Vercel Perf widget
	injectSpeedInsights();

	// Function to set the height of .app to match the inner height of the window

	function adjustAppHeight() {
		const appElement = document.querySelector('.app');
		if (appElement instanceof HTMLElement) {
			appElement.style.height = `${window.innerHeight}px`;
		}
	}

	onMount(() => {
		adjustAppHeight();
		window.addEventListener('resize', adjustAppHeight);
	});
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
		padding: 1.6rem;
		box-sizing: border-box; /* Include padding in element's total height */
		height: 100svh;

		@media screen and (min-width: 1024px) {
			padding: var(--default-padding);
			height: 100vh;
		}
	}

	.content {
		display: flex;
		flex-direction: column;
		justify-content: flex-end;
		flex-grow: 1;

		@media screen and (min-width: 768px) {
			max-width: 70%;
		}
	}
</style>
