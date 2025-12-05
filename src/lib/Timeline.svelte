<script lang="ts">
    import TimelineEntry from "./TimelineEntry.svelte";


</script>

<style>
	ul {
		padding-inline-start: var(--spacing-l);
		/* position: relative; */
		margin-block: 0;
	}

	ul::before {
		content: "";
		position: absolute;
		/* janked this by just setting overflow-x hidden */
		width: 100vw;
		height: var(--border-width);

		left: 0;

		background: var(--color-gray);
	}

	ul::after {
		content: "";
		position: absolute;
		width: 100vw;
		height: var(--border-width);

		left: 0;

		background: var(--color-gray);
	}



	h3 {
		font-size: var(--font-size-ml);

		margin-block-start: 0;
	}
</style>

<ul>
	<TimelineEntry date="2025–2026">
		<h3>
			Year 1
		</h3>

		<p>
			Lorem ipsum dolor sit amet consectetur adipisicing elit. Obcaecati, rem quis totam accusantium perspiciatis minima, nostrum tempora quo, beatae omnis maxime nisi culpa sapiente iste. Omnis deleniti eum ex repudiandae.
			Lorem ipsum dolor sit amet consectetur adipisicing elit. Obcaecati, rem quis totam accusantium perspiciatis minima, nostrum tempora quo, beatae omnis maxime nisi culpa sapiente iste. Omnis deleniti eum ex repudiandae.
			Lorem ipsum dolor sit amet consectetur adipisicing elit. Obcaecati, rem quis totam accusantium perspiciatis minima, nostrum tempora quo, beatae omnis maxime nisi culpa sapiente iste. Omnis deleniti eum ex repudiandae.
			Lorem ipsum dolor sit amet consectetur adipisicing elit. Obcaecati, rem quis totam accusantium perspiciatis minima, nostrum tempora quo, beatae omnis maxime nisi culpa sapiente iste. Omnis deleniti eum ex repudiandae.
			Lorem ipsum dolor sit amet consectetur adipisicing elit. Obcaecati, rem quis totam accusantium perspiciatis minima, nostrum tempora quo, beatae omnis maxime nisi culpa sapiente iste. Omnis deleniti eum ex repudiandae.
		</p>

	</TimelineEntry>

	<TimelineEntry date="2025–2026">
		<h3>
			H3 content
		</h3>

		<p>
			Lorem ipsum dolor sit amet consectetur adipisicing elit. Obcaecati, rem quis totam accusantium perspiciatis minima, nostrum tempora quo, beatae omnis maxime nisi culpa sapiente iste. Omnis deleniti eum ex repudiandae.
			Lorem ipsum dolor sit amet consectetur adipisicing elit. Obcaecati, rem quis totam accusantium perspiciatis minima, nostrum tempora quo, beatae omnis maxime nisi culpa sapiente iste. Omnis deleniti eum ex repudiandae.
			Lorem ipsum dolor sit amet consectetur adipisicing elit. Obcaecati, rem quis totam accusantium perspiciatis minima, nostrum tempora quo, beatae omnis maxime nisi culpa sapiente iste. Omnis deleniti eum ex repudiandae.
			Lorem ipsum dolor sit amet consectetur adipisicing elit. Obcaecati, rem quis totam accusantium perspiciatis minima, nostrum tempora quo, beatae omnis maxime nisi culpa sapiente iste. Omnis deleniti eum ex repudiandae.
			Lorem ipsum dolor sit amet consectetur adipisicing elit. Obcaecati, rem quis totam accusantium perspiciatis minima, nostrum tempora quo, beatae omnis maxime nisi culpa sapiente iste. Omnis deleniti eum ex repudiandae.
		</p>

	</TimelineEntry>
</ul>
