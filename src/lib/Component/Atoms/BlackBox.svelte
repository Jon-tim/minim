<script lang="ts">
	export let px: string;
	export let py: string;
</script>

<div
	class={`bg-black text-white cursor-pointer flex items-center justify-center gap-2 w-max ${px} ${py} h-max `}
>
	<slot />
</div>
