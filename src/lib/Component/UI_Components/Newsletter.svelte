<script>
	import BlackBox from '../Atoms/BlackBox.svelte';
</script>

<section class="comp-layout py-10 md:py-20 contain">
	<div class="hidden md:block img1">
		<img src="/Images/newsletter/newletterimg1.jpg" alt="model" />
	</div>
	<form
		class="flex flex-col items-center text-center gap-4 max-w-xl mx-auto bg-white/30 backdrop-blur-lg p-6 shadow"
	>
		<h1 class="text-2xl capitalize">subscribe to our newsletter!</h1>
		<p class="text-sm text-black/70">
			Check back every week to uncover new and exciting opportunities to save on top-quality
			products and experiences. Shop smart, save big, and make every week a rewarding shopping
			adventure with our 'Deals of the Week'!"
		</p>
		<input
			type="text"
			placeholder="example@gmail.com"
			class="w-full px-4 py-3 my-2 text-black text-sm focus:outline-none shadow-lg"
		/>
		<BlackBox px="px-8" py="py-2">
			<button class="capitalize text-white w-full h-full">subscribe now</button>
		</BlackBox>
	</form>
	<div class="img2">
		<img src="/Images/newsletter/newletterimg2.jpg" alt="model" />
	</div>
</section>

<style>
	.contain {
		display: grid;
		grid-template-columns: 1fr;
		grid-template-rows: 1fr;
		align-items: center;
	}

	form {
		order: 2;
	}

	input {
		background-color: #fff;
	}

	form,
	.img2,
	.img1 {
		grid-column: 1/2;
		grid-row: 1/2;
	}

	.img1,
	.img2 {
		height: 500px;
	}

	img {
		width: 100%;
		height: 100%;
		object-fit: contain;
	}

	@media screen and (min-width: 768px) {
		.contain {
			grid-template-columns: repeat(3, 1fr);
		}
		form {
			grid-column: 1/-1;
		}

		.img1 {
			grid-column: 1/2;
		}
		.img2 {
			grid-column: 3/-1;
		}
	}

	@media screen and (min-width: 1024px) {
		input {
			background-color: var(--custom-light-grey);
		}
	}
</style>
