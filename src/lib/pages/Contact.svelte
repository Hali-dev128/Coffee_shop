<script>
	import Button from "$lib/shared/Button.svelte";

</script>
<article id="contact">
    <h3 class="title font-bold text-4xl relative mb-20">CONTACT US</h3>

    <section>
        <ul>
            <li>
                <svg data-v-15b35c9e="" xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-icon customizable lucide-map-pinned-icon lucide-map-pinned lucide-icon customizable" aria-hidden="true"><path d="M18 8c0 3.613-3.869 7.429-5.393 8.795a1 1 0 0 1-1.214 0C9.87 15.429 6 11.613 6 8a6 6 0 0 1 12 0"></path><circle cx="12" cy="8" r="2"></circle><path d="M8.714 14h-3.71a1 1 0 0 0-.948.683l-2.004 6A1 1 0 0 0 3 22h18a1 1 0 0 0 .948-1.316l-2-6a1 1 0 0 0-.949-.684h-3.712"></path></svg>
                <span>123 Campsite Avenue, Wilderness, CA SH765</span>
            </li>
            <li>
                <svg data-v-15b35c9e="" xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-icon customizable lucide-mail-icon lucide-mail lucide-icon customizable" aria-hidden="true"><path d="m22 7-8.991 5.727a2 2 0 0 1-2.009 0L2 7"></path><rect x="2" y="4" width="20" height="16" rx="2"></rect></svg>
                <span>info@coffeeshopwebsite.com</span>
            </li>
            <li>
                <svg data-v-15b35c9e="" xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-icon customizable lucide-phone-icon lucide-phone lucide-icon customizable" aria-hidden="true"><path d="M13.832 16.568a1 1 0 0 0 1.213-.303l.355-.465A2 2 0 0 1 17 15h3a2 2 0 0 1 2 2v3a2 2 0 0 1-2 2A18 18 0 0 1 2 4a2 2 0 0 1 2-2h3a2 2 0 0 1 2 2v3a2 2 0 0 1-.8 1.6l-.468.351a1 1 0 0 0-.292 1.233 14 14 0 0 0 6.392 6.384"></path></svg>
                <span>[123]456-78909</span>
            </li>
            <li>
                <svg data-v-15b35c9e="" xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-icon customizable lucide-clock-icon lucide-clock lucide-icon customizable" aria-hidden="true"><circle cx="12" cy="12" r="10"></circle><path d="M12 6v6l4 2"></path></svg>
                <span>Monday - Friday: 8:00AM - 5:00PM</span>
            </li>
            <li>
                <svg data-v-15b35c9e="" xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-icon customizable lucide-clock-icon lucide-clock lucide-icon customizable" aria-hidden="true"><circle cx="12" cy="12" r="10"></circle><path d="M12 6v6l4 2"></path></svg>
                <span>Saturday: 10:00AM - 8:00PM</span>
            </li>
            <li>
                <svg data-v-15b35c9e="" xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-icon customizable lucide-clock-icon lucide-clock lucide-icon customizable" aria-hidden="true"><circle cx="12" cy="12" r="10"></circle><path d="M12 6v6l4 2"></path></svg>
                <span>Sunday: Closed</span>
            </li>
            <li>
                <svg data-v-15b35c9e="" xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-icon customizable lucide-globe-icon lucide-globe lucide-icon customizable" aria-hidden="true"><circle cx="12" cy="12" r="10"></circle><path d="M12 2a14.5 14.5 0 0 0 0 20 14.5 14.5 0 0 0 0-20"></path><path d="M2 12h20"></path></svg>
                <a href="https://hali-dev-fwo9.vercel.app/" target="_blank">hali-dev-fwo9.vercel.app</a>
            </li>
        </ul>
        <form>
            <input type="text" placeholder="Your name" required>
            <input type="email" placeholder="Your email" required>
            <textarea placeholder="Your message" required></textarea>
            <Button type='submit' ter={true}>Submit</Button>
        </form>
    </section>
</article>

<style>
    #contact {justify-content: center;}

    section {
        width: var(--width);
        margin: 0 auto;
        display: grid;
        grid-gap: 20px;
        grid-template-columns: repeat(2, 1fr);
    }

    section > ul, form {
        display: flex;
        flex-direction: column;
        gap: 15px;
    }
    section > ul > li {
        display: flex;
        align-items: center;
        gap: 20px;
    }

    input, textarea {
        border-radius: 10px;
        border: 2px solid var(--ter);
        width: 100%;
        height: 50px;
    }
    textarea {height: 150px;}

    @media(max-width: 800px) {
        section {
            display: flex;
            flex-direction: column-reverse;
            align-items: center;
            gap: 25px;
            margin-bottom: var(--gap);
        }
        form {width: 100%;}
    }
</style>