<script>
	import Navbar from '$lib/Component/UI_Components/Navbar.svelte';
	import Footer from '$lib/Component/UI_Components/Footer.svelte';
	import '../app.css';
</script>

<Navbar />
<slot />
<Footer />
