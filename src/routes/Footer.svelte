<script>
	import Instagram from '$lib/components/icons/Instagram.svelte';
	import Tiktok from '$lib/components/icons/Tiktok.svelte';
	import X from '$lib/components/icons/X.svelte';
</script>

<div class="footer">
	<h3>
		{' Engineered in Atlanta'.toUpperCase()}
	</h3>
	<span class="icon-links">
		<a
			class="icon-link"
			href="https://instagram.com/montez.ig"
			target="_blank"
			rel="noopener noreferrer"
		>
			<Instagram /></a
		>
		<a
			class="icon-link"
			href="https://x.com/montezdotdot"
			target="_blank"
			rel="noopener noreferrer"
		>
			<X /></a
		><a
			class="icon-link"
			href="https://tiktok.com/@montez.tok"
			target="_blank"
			rel="noopener noreferrer"
		>
			<Tiktok />
		</a></span
	>
</div>

<style>
	.footer {
		justify-content: space-between;
		display: flex;
		align-items: center;
	}

	.icon-links {
		display: flex;
		gap: 0.5rem;
	}

	.icon-link {
		/* --fs-icon: clamp(1.4rem, 2vw, 2rem); */
		color: rgba(255, 255, 255, 0.5);
		width: clamp(1.4rem, 2vw, 2rem);
		height: clamp(1.4rem, 2vw, 2rem);
	}
</style>
