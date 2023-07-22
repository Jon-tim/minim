<script>
	import '../../../app.css';
	import BlackBox from '../Atoms/BlackBox.svelte';
</script>

<section class="comp-layout w-full parent">
	<section class="contain grid">
		<div class="a overflow-hidden">
			<img
				src="Images/fashion/men/long2.jpg"
				class="w-full h-full object-center object-cover"
				alt=""
			/>
		</div>
		<div class="b overflow-hidden">
			<img src="Images/fashion/hero1.jpg" alt="" class="w-full h-full object-center object-cover" />
		</div>
		<div class="c overflow-hidden">
			<img
				src="Images/fashion/women/long.jpg"
				class="w-full h-full object-center object-cover"
				alt=""
			/>
		</div>
		<div class="d flex flex-col justify-center gap-1 items-center">
			<p class=" text-6xl text-[#484848]">ultimate</p>
			<p class="text-9xl font-bold sale">sale</p>
			<p class="text-xl text-white mb-4 min-[620px]:text-black/80">new collection</p>
			<BlackBox px="px-3" py="py-2"><p class="text-white capitalize">show now</p></BlackBox>
		</div>
		<div class="e overflow-hidden">
			<img
				src="Images/fashion/men/clotheline.jpg"
				class="w-full h-full object-top object-cover"
				alt=""
			/>
		</div>
	</section>
</section>

<style lang="postcss">
	.parent {
		height: 90vh;
	}
	.contain {
		height: 100%;
		width: 100%;
		display: grid;
		gap: 1rem;
		grid-template-columns: 1fr;
		grid-template-rows: 1fr;
		grid-template-areas:
			'd'
			'a';
	}
	.contain div:not(.d) {
		background-color: #e4e4e4;
	}
	.a,
	.b,
	.c,
	.d,
	.e {
		height: 100%;
		width: 100%;
	}

	.d,
	.a {
		grid-row: 1/2;
		grid-column: 1/2;
	}
	.d p {
		text-transform: uppercase;
	}

	.sale {
		text-stroke-width: 2px;
		/* text-stroke-color: var(--headings-color); */
		text-stroke-color: white;
		text-fill-color: transparent;
		/* ------------------ */
		-webkit-text-stroke-width: 2px;
		-webkit-text-stroke-color: white;
		-webkit-text-fill-color: transparent;
	}

	.b,
	.c,
	.e {
		display: none;
	}

	@media screen and (min-width: 620px) {
		.sale {
			text-stroke-color: var(--headings-color);
			-webkit-text-stroke-color: var(--headings-color);
		}
		.b,
		.c,
		.e {
			display: unset;
		}
		.contain {
			grid-template-columns: repeat(3, 1fr);
			grid-template-rows: 1fr 3fr 1fr;
			grid-template-areas:
				'a b c'
				'a d c'
				'a e c';
		}
		.a {
			grid-area: a;
		}
		.b {
			grid-area: b;
		}
		.c {
			grid-area: c;
		}
		.d {
			grid-area: d;
		}
		.e {
			grid-area: e;
		}
	}
</style>
