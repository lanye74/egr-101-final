<script lang="ts">
	import "@fontsource/pt-serif";
	import "@fontsource-variable/funnel-sans";



	let {children} = $props();
</script>

<style>
	:global(body) {
		margin: 0;

		padding-block: 2em;
		padding-inline: calc(calc(100vw - 42em) / 2);

		line-height: 1.6;
	}

	main {
		padding: 2em;
		border: 0.125em solid #eee;
		box-shadow: 0 0;
	}
</style>

<main>
	{@render children()}
</main>
