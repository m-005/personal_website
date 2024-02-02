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

	<content>
		<slot />
	</content>

	<Home />
	<Footer />
</div>

<style>
	.app {
		display: flex;
		flex-direction: column;
		max-height: 100vh;
		padding: var(--default-padding);
	}

	@media (max-width: 768px) {
		.app {
			padding: var(--default-padding) * var(--mobile-padding-offset);
		}
	}

	content {
		display: flex;
		flex-direction: column;
		justify-content: flex-end;
		flex: 1;
		max-width: 70%;
	}

	@media (max-width: 768px) {
		content {
			max-width: 100%;
		}
	}
</style>
