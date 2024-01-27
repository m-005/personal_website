<script>
	import { page } from '$app/stores';
	$: home = $page.url.pathname == '/' ? 'Montez.' : 'M.';
</script>

<footer>
	<h1><a href="/">{home.toUpperCase()}</a></h1>
	<h3>{' Engineered in Atlanta'.toUpperCase()}<a></a></h3>
</footer>

<style>
	footer {
		padding: 0 4rem 4rem 4rem;
	}
</style>
