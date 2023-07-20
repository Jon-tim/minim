<script lang="ts">
	import BlackBox from '../Atoms/BlackBox.svelte';
	import Logo from '../Atoms/Logo.svelte';
	import MenuToggle from '../Atoms/MenuToggle.svelte';
	import NavLinks from '../Molecules/NavLinks.svelte';
</script>

<nav class="comp-layout border-b">
	<div class="flex items-center justify-between">
		<div class="hidden md:flex items-center gap-4 md:gap-10">
			<NavLinks />
		</div>
		<MenuToggle />
		<!------------------>
		<Logo />
		<BlackBox h="h-max" w="w-max" px="px-3" py="py-2">
			<span class="capitalize text-sm">cart (0)</span>
		</BlackBox>
	</div>
</nav>
