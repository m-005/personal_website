<script>
	import Arena from '$lib/components/icons/Arena.svelte';
</script>

<div class="nav">
	<h2>
		<a href="https://paragraph.xyz/@montez" target="_blank" rel="noopener noreferrer"
			>{'Writing'.toUpperCase()}</a
		>
	</h2>
	<h2>
		<a href="https://are.na/montez" target="_blank" rel="noopener noreferrer"
			>{'Archive'.toUpperCase()}<Arena />
		</a>
	</h2>
	<h2>
		<a href="mailto:email@montez.cloud">{'Contact'.toUpperCase()}</a>
	</h2>
	<!-- <iframe
		title="Subscribe"
		src="https://paragraph.xyz/@montez/embed?minimal=true"
		width="350px"
		height="45"
		style=" background:transparent;"
		frameborder="0"
		scrolling="no"
	></iframe> -->
</div>

<style>
	.nav {
		list-style-type: none;
		text-align: right;
		align-items: center;
	}
</style>
