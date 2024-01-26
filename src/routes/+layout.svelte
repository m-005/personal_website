<script>
	import './style.css';
</script>

<div id="nav">
	<h2><a href="/projects">{'Projects'.toUpperCase()}</a></h2>
	<h2><a href="https://are.na/montez">{'Archive'.toUpperCase()}</a></h2>
	<h2><a href="mailto:email@montez.cloud">{'Contact'.toUpperCase()}</a></h2>
</div>

<slot />

<div id="footer">
	<h1>{'Montez.'.toUpperCase()}</h1>
	<h3>{'Engineered in Atlanta'.toUpperCase()}</h3>
</div>

<style>
	#nav {
		text-align: right;
	}
	#footer {
		position: fixed;
		bottom: 0;
	}
</style>
