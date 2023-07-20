<script>
	let nums = [1, 2, 4, 3, 5];
</script>

<section class="comp-layout flex flex-wrap items-center justify-between gap-4 md:gap-8 my-8 md:my-16">
	{#each nums as num (num)}
		<div class="flex-1">
			<img src="Images/brands/brands{num}.svg" alt="brands" class="w-full" />
		</div>
	{/each}
</section>
