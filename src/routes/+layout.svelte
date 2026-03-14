<script>
	import Footer from '$lib/components/Footer.svelte';
	import Navbar from '$lib/components/Navbar.svelte';
    import '../app.css'; // Make sure Tailwind is setup
    import { Toaster } from 'svelte-french-toast';
</script>

<Toaster />

<Navbar/>
<div>
    <slot></slot>

    <Footer/>
</div>