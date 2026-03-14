<script>
	import Button from "$lib/shared/Button.svelte";
	import { fade, slide } from "svelte/transition";

    let open = false;

    const toggleMenu = () => {
        open == false ? open = true : open = false;
    }
</script>

<nav class="py-4">
    <section>
        <h2 class="flex items-center gap-1.5">
            <img width="30" src="./hot-beverages.png" alt="Coffee Shop Logo">
            <span class="text-3xl font-bold">Coffee</span>
        </h2>

        <!-- svelte-ignore a11y_click_events_have_key_events -->
        <!-- svelte-ignore a11y_no_static_element_interactions -->
        <span class="menu hidden cursor-pointer" onclick={() => toggleMenu()}>
            <svg data-v-15b35c9e="" xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-icon customizable lucide-text-align-justify-icon lucide-text-align-justify lucide-icon customizable" aria-hidden="true"><path d="M3 5h18"></path><path d="M3 12h18"></path><path d="M3 19h18"></path></svg>
        </span>

        <ul class="flex items-center gap-1.5">
            <li>
                <a href="#home"><Button faded={true} type='button'>home</Button></a>
            </li>
            <li>
                <a href="#about"><Button faded={true} type='button'>about</Button></a>
            </li>
            <li>
                <a href="#menu"><Button faded={true} type='button'>menu</Button></a>
            </li>
            <li>
                <a href="#testimonials"><Button faded={true} type='button'>testimonials</Button></a>
            </li>
            <li>
                <a href="#gallery"><Button faded={true} type='button'>gallery</Button></a>
            </li>
            <li>
                <a href="#contact"><Button faded={true} type='button'>contact</Button></a>
            </li>
        </ul>
    </section>
</nav>
{#if open}
    <div class="hidden">
        <!-- svelte-ignore a11y_no_noninteractive_element_interactions -->
        <ul class="links2" in:slide={{axis: 'x', delay: 350}} out:slide={{axis: 'x', duration: 300}} class:open={open}>
            <a href="#home"><li>home</li></a>
            <a href="#about"><li>about</li></a>
            <a href="#menu"><li>menu</li></a>
            <a href="#testimonials"><li>testimonials</li></a>
            <a href="#gallery"><li>gallery</li></a>
            <a href="#contact"><li>contact</li></a>
            <!-- svelte-ignore a11y_click_events_have_key_events -->
            <li class="close" onclick={() => toggleMenu()}>
                <svg data-v-15b35c9e="" xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-icon customizable lucide-x-icon lucide-x lucide-icon customizable" aria-hidden="true"><path d="M18 6 6 18"></path><path d="m6 6 12 12"></path></svg>
            </li>
        </ul>
        <span class="blurr" in:fade={{duration: 300}} out:fade={{delay: 350}} class:open={open}></span>
    </div>
{/if}

<style>
    nav {
        background-color: var(--ter);
        color: var(--pri);
        width: 100vw;
        position: sticky;
        top: 0;
        z-index: 97;
    }

    nav > section {
        width: var(--width);
        margin: 0 auto;
        display: flex;
        align-items: center;
        gap: 20px;
        flex-wrap: wrap;
        justify-content: space-between;
    }

    .blurr {
        position: fixed;
        width: 100%;
        height: 100%;
        background-color: #fff2;
        backdrop-filter: blur(2px);
        z-index: 1;
    }

    .close {
        position: absolute;
        top: 15px;
        right: 15px;
        cursor: pointer;
        padding: 0 !important;
    }

    .links2 {
        display: flex;
        flex-direction: column;
        padding: 15px ;
        text-align: center;
        position: fixed;
        justify-content: center;
        width: 50%;
        z-index: 2;
        height: 100%;
        left: 0;
        background-color: var(--text);
    }

    .links2 li {
        color: var(--pri);
        padding: 10px;
        cursor: pointer;
        transition: var(--trans);
    }
    .links2 li:hover {
        color: var(--text);
        background-color: var(--pri);
    }
</style>