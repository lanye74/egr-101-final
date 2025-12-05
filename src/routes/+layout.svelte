<script lang="ts">
	import "@fontsource/pt-serif";
	import "@fontsource-variable/funnel-sans";
	import type {Snippet} from "svelte";

	import Timeline from "$lib/Timeline.svelte";

	type Props = {
		children: Snippet;
	};


	let {children} = $props();


	let headerHeight: number = $state(0);
</script>

<style>
	:root {
		--spacing-l: 2em;
		--spacing-m: 1em;

		--font-size-xl: 3em;
		--font-size-l: 2em;
		--font-size-ml: 1.5em;
		--font-size-m: 1.125em;
		--font-size-ms: 0.875em;

		--border-width: 0.125em;

		--color-light: #ddd;
		--color-gray: #aaa;
	}

	:global(body) {
		margin: 0;

		padding-block: var(--spacing-l);
		padding-inline: max(var(--spacing-l), calc(calc(100vw - 42em) / 2));

		line-height: 1.6;

		font-family: "PT Serif";

		overflow-x: hidden;
	}

	:global(h1, h2, h3) {
		font-family: "Funnel Sans Variable";
	}



	main {
		padding: var(--spacing-l);

		border: var(--border-width) solid var(--color-gray);
		border-width: 0 var(--border-width);

		&::after {
			content: "";
			position: absolute;
			width: 100vw;
			height: var(--border-width);

			left: 0;

			background: var(--color-gray);
		}
	}



	header {
		text-align: center;
		padding: var(--spacing-l);

		&::before {
			content: "";
			position: absolute;
			width: 100vw;
			height: var(--border-width);

			left: 0;

			background: var(--color-gray);
		}



		& h1 {
			font-size: var(--font-size-xl);
			margin-block-start: 0;
		}

		& p {
			font-size: var(--font-size-ml);
			margin-block-end: 0;
		}



		& .flank {
			position: absolute;
			background-color: var(--color-gray);
			width: var(--border-width);

			/* not sure why it's 3.5 but idgaf*/
			height: calc(var(--h) + 3 * var(--spacing-l));
			top: 0;

			right: calc(calc(100vw - 42em) / 2);
		}

		& .flank-1 {
			translate: calc(-1 * var(--spacing-l)) 0;
			right: unset;
		}
	}
</style>



<header>
	<div class="flank flank-1" style:--h={`${headerHeight}px`}></div>
	<div class="flank flank-2" style:--h={`${headerHeight}px`}></div>

	<div bind:clientHeight={headerHeight}>
		<h1>Layne Ogden: EGR 101 Final</h1>
		<p>A road map to becoming a successful engineer</p>
	</div>
</header>

<section>
	<Timeline />
</section>

<main>
	{@render children()}
</main>

<footer>

</footer>
