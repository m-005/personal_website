<script>
	import { page } from '$app/stores';
	$: home = $page.url.pathname == '/' ? 'Montez.' : 'M.';
</script>

<h1><a href="/">{home.toUpperCase()}</a></h1>
<h3>{' Engineered in Atlanta'.toUpperCase()}</h3>
