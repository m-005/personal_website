<script>
	import { page } from '$app/stores';
	$: home = $page.url.pathname == '/' ? 'Montez.' : 'M.';
</script>

<h1><a href="/">{home.toUpperCase()}</a></h1>

<style>
	/* h1 {
		padding: 0 0 0 var(--default-padding);
	} */
</style>
