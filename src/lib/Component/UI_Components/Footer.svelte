<script>
	import Logo from '../Atoms/Logo.svelte';
</script>

<footer class="px-4 md:px-6 py-4 max-w-5xl mx-auto xl:px-0 border-t">
	<div>
		<div class="flex items-center justify-between">
			<p class="text-xs hover:underline hover:underline-offset-2 cursor-not-allowed">Support</p>
			<p class="text-xs hover:underline hover:underline-offset-2 cursor-not-allowed">FAQ</p>
			<Logo />
			<p class="text-xs hover:underline hover:underline-offset-2 cursor-not-allowed">Careers</p>
			<p class="text-xs hover:underline hover:underline-offset-2 cursor-not-allowed">Contracts</p>
		</div>
		<p class="text-xs md:text-sm text-center mt-4 opacity-80">
			Copyright {new Date().getFullYear()} Minim. All Rights Reserved
		</p>
	</div>
</footer>
