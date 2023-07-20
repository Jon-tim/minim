<script>
	import '../../../app.css';
</script>

<section class="comp-layout w-full parent">
	<section class="contain grid">
		<div class="a">aaaa</div>
		<div class="b">bbbb</div>
		<div class="c">cccc</div>
		<div class="d">text</div>
		<div class="e">eeee</div>
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
		grid-template-rows: 60% 40%;
		grid-template-areas:
			'd'
			'a';
	}
	.contain div {
		background-color: #e4e4e4;
		background-color: var(--red-alert-color);
	}
	.a,
	.b,
	.c,
	.d,
	.e {
		height: 100%;
		width: 100%;
	}

	.d {
		grid-row: 1/2;
	}

	.b,
	.c,
	.e {
		display: none;
	}

	@media screen and (min-width: 620px) {
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
