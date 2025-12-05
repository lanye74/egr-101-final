<script lang="ts">
    import TimelineEntry from "./TimelineEntry.svelte";


</script>

<style>
	ul {
		padding-inline-start: var(--spacing-l);
		/* position: relative; */
		margin-block: 0;
	}

	ul {
		border-inline-end: var(--border-width) dashed var(--color-light);
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
		<h3>Year 1</h3>

		<p>
			UK core classes and foundational CS courses (215, 217, 218, 275). I will finish my math minor this year, try to convince myself not to start the math major yet, and well as obtain my engineering standing for future CS courses.
		</p>

		<p>Hopefully, I can also slot in a summer internship :-)</p>
	</TimelineEntry>

	<TimelineEntry date="2026–2027">
		<h3>Year 2</h3>

		<p>
			Things get busy. I need to start looking outside of UK and pushing my job skills: learning a stylesheet language, furthering my comfortability with databases, and improving my design skills.
		</p>

		<p>
			I may pick up a co-op in my spring semester, since my CS coursework is accelerated.
		</p>
	</TimelineEntry>

	<TimelineEntry date="2027–2029">
		<h3>Years 3–4</h3>

		<p>
			My end goal is to <em>never be bored</em>, to keep pushing myself and pursuing things I find interesting. My anthropology course, for example, has been super interesting, and I would love to pursue it further. In this time, I want to focus on enriching myself and getting as much out of UK as I can.
		</p>

		<p>
			I would also like to pursue some research in my target field of design and accessibility.
		</p>
	</TimelineEntry>

	<TimelineEntry date="2029–???">
		<h3>After College</h3>

		<p>
			I want a job that is both terrifying and exciting; that pushes me to grow, while not alienating me; where I feel that the <em>work I do</em> has impacts on people's lives. Something where I am never stagnating and can find a community of like-minded individuals.
		</p>

		<p>
			My dream goal—and perhaps a pipe dream it is, now, with the current housing prices—is to buy a house and settle down with my partner.
		</p>
	</TimelineEntry>
</ul>
