<script lang="ts">
    import type {Snippet} from "svelte";

	type Props = {
		children: Snippet;
		date: string;
	};



	let {date, children}: Props = $props();
</script>


<style>
	li {
		position: relative;
		anchor-name: --li;
	}

	li::marker {
		font-size: var(--font-size-ml);

	}

	li::before {
		content: attr(data-date);
		font-size: var(--font-size-ms);
		position: absolute;

		font-style: italic;

		translate: calc(-100% - var(--spacing-m) - 2em)
			/* grrr */
			/* calc((var(--font-size-l) - var(--font-size-ms)) / 2); */
			/* the brainrot */
			0.607em;
	}

	/* vertical bar */
	li::after {
		content: "";
		position: absolute;

		translate: calc(-1 * var(--spacing-l)) -100%;
		width: var(--border-width);

		height: calc(100% + var(--spacing-m));

		background: var(--color-gray);
	}
</style>

<li data-date={date}>
	{@render children()}
</li>
