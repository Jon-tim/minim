<script lang="ts">
	import BlackBox from '../Atoms/BlackBox.svelte';
	import MenuToggle from '../Atoms/MenuToggle.svelte';
	import NavLinks from '../Molecules/NavLinks.svelte';
</script>

<nav class="px-4 md:px-6 py-4 max-w-5xl mx-auto xl:px-0">
	<div class="flex items-center justify-between">
		<div class="hidden md:flex items-center gap-4 md:gap-10">
			<NavLinks />
		</div>
		<MenuToggle />
		<!------------------>
		<a href="/">
			<h1 class="uppercase text-black text-2xl">minim</h1>
		</a>
		<BlackBox h="h-max" w="w-max" px="px-3" py="py-2">
			<span class="capitalize text-sm">cart (0)</span>
		</BlackBox>
	</div>
</nav>
