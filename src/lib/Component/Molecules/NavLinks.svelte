<script lang="ts">
	import Links from '../Atoms/Links.svelte';
	let categories = [
		{ id: 1, category: 'men', slug: '/men' },
		{ id: 2, category: 'women', slug: '/women' }
	];
</script>

{#each categories as category (category.id)}
	<Links to={category.slug} name={category.category} />
{/each}
