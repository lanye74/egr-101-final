<script lang="ts">
	import "@fontsource/pt-serif";
	import "@fontsource-variable/funnel-sans";



	let {children} = $props();
</script>

<style>
	:root {
		--spacing-l: 2em;
		--spacing-m: 1em;

		--font-size-l: 2em;
		--font-size-m: 1em;

		--color-light: #eee;
		--color-gray: #aaa;
	}

	:global(body) {
		margin: 0;

		padding-block: var(--spacing-l);
		padding-inline: max(var(--spacing-l), calc(calc(100vw - 42em) / 2));

		line-height: 1.6;

		font-family: "PT Serif";
	}

	:global(h1, h2, h3) {
		font-family: "Funnel Sans Variable";
	}



	main {
		padding: var(--spacing-l);
		border: 0.125em solid var(--color-light);
	}
</style>

<main>
	{@render children()}
</main>
