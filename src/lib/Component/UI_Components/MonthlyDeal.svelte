<script>
	import BlackBox from '../Atoms/BlackBox.svelte';
	import CountDown from '../Atoms/CountDown.svelte';
</script>

<section class="contain">
	<section class="comp-layout">
		<div class="flex flex-col gap-2">
			<h1 class="capitalize text-2xl">deals of the month</h1>
			<p class=" text-sm mb-3">
				Discover unbeatable offers and incredible savings on a curated selection of products! Our
				offers feature hand-picked deals that are sure to delight bargain hunters and savvy shoppers
				alike.
			</p>
			<BlackBox px="px-6" py="py-2"
				><p class="text-white capitalize">buy now</p></BlackBox
			>
			<div class="mt-6">
				<p class="uppercase mb-2 text-sm text-red-500 font-semibold">Hurry before it's too late!</p>
				<CountDown />
			</div>
		</div>
	</section>
</section>

<style>
	.contain {
		background-color: var(--custom-light-grey);
	}
</style>
