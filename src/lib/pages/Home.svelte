<script>
	import Button from "$lib/shared/Button.svelte";
</script>

<article id="home">
    <div>
        <section class="first_sec">
            <h2 class="text-4xl font-bold">Best Coffee</h2>
            <h3 class="text-2xl font-bold">Make your day great with our special coffee!</h3>
            <p>Welcome to our coffee paradise, where every bean tells a story and every cup sparks joy.</p>
            <div class="flex items-center gap-5">
                <Button>Order Now</Button>
                <a href="#contact"><Button inverted={true}>Contact Us</Button></a>
            </div>
        </section>
        <section>
            <img src="./coffee-hero-section.png" alt="Header pic">
        </section>
    </div>
</article>

<style>
    #home {
        background-color: var(--ter);
        color: var(--pri);
    }
    
    #home > div {
        display: grid;
        width: var(--width);
        height: 100%;
        margin: 0 auto;
        align-items: center;
        justify-content: space-between;
        gap: var(--gap);
        grid-template-columns: repeat(2, 1fr);
    }
    
    h2 {
        font-family: Monotype Corsiva;
        color: var(--sec);
    }
    h3 {max-width: 30ch;}
    p {max-width: 55ch;}

    .first_sec {
        display: flex;
        flex-direction: column;
        gap: 15px;
        
    }

    @media(max-width: 810px) {
        #home > div {
            display: flex;
            flex-direction: column-reverse;
            justify-content: center;
        }

        section > img {
            width: 60%;
            margin: 0 auto;
        }

        h3 {width: 100%;}
        p {width: 100%;}
        .first_sec {
            align-items: center;
            text-align: center;
            gap: 10px;
        }
    }
</style>