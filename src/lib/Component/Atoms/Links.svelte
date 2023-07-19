<script lang="ts">
	export let to: string;
	export let name: string;
</script>

<a href={to} class="transition-colors hover:underline duration-100 capitalize ease-linear">{name}</a>
