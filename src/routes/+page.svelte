<script>
	import About from "$lib/pages/About.svelte";
	import Contact from "$lib/pages/Contact.svelte";
	import Gallery from "$lib/pages/Gallery.svelte";
	import Home from "$lib/pages/Home.svelte";
	import Menu from "$lib/pages/Menu.svelte";
	import Testimonials from "$lib/pages/Testimonials.svelte";
</script>

<main>
    <Home/>
    <About/>
    <Menu/>
    <Testimonials/>
    <Gallery/>
    <Contact/>
</main>

<style>
    main {
        display: flex;
        flex-direction: column;
        gap: 68px;
    }
</style>