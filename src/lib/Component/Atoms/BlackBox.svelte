<script lang="ts">
	export let w: string;
	export let h: string;
	export let px: string;
	export let py: string;
</script>

<div
	class={`bg-black text-white cursor-pointer flex items-center justify-center gap-2 ${w} ${px} ${py} ${h}`}
>
	<slot />
</div>
