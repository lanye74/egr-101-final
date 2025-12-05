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
			0.6em;
	}

	/* vertical bar */
	li::after {
		content: "";
		position: absolute;

		translate: calc(-1 * var(--spacing-l)) calc(-100% + 0.5em);
		width: 0.125em;

		height: calc(100% + var(--spacing-m));

		background: linear-gradient(var(--color-light) 0%, var(--color-gray) 20%, var(--color-gray) 80%, var(--color-light) 100%);
	}
</style>

<li data-date={date}>
	{@render children()}
</li>
