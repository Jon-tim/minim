<script>
	import Navbar from '$lib/Component/UI_Components/Navbar.svelte';
	import Footer from '$lib/Component/UI_Components/Footer.svelte';
	import '../app.css';
</script>

<svelte:head>
	<title>minim | home</title>
	<meta name="description" content="A Unisex fashion store" />
</svelte:head>

<Navbar />
<main>
	<slot />
</main>
<Footer />
