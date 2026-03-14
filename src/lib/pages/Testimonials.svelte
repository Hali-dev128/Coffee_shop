<article id="testimonials">
    <h3 class="title font-bold text-4xl relative mb-20">TESTIMONIALS</h3>

    <ul>
        <li class="text-center">
            <img src="./user-2.jpg" alt="Pic of James Wilson">
            <h4 class="capitalize font-bold text-xl">James Wilson</h4>
            <p>"Great espresso blend, smooth and bold flavour. Fast shipping."</p>
        </li>
        <li class="text-center">
            <img src="./user-3.jpg" alt="Pic of Micheal Brown">
            <h4 class="capitalize font-bold text-xl">Micheal Brown</h4>
            <p>"Fantastic mocha flavour. fresh and aromatic. Quick shipping."</p>
        </li>
        <li class="text-center">
            <img src="./user-4.jpg" alt="Pic of Emily Haris">
            <h4 class="capitalize font-bold text-xl">Emily Harris</h4>
            <p>"Excellent quality fresh beans and quick delivery. Highly recommend."</p>
        </li>
        <li class="text-center">
            <img src="./user-5.jpg" alt="Pic of Anthony Thompson">
            <h4 class="capitalize font-bold text-xl">Anthony Thompson</h4>
            <p>"Best decaf i've tried, smooth and flavourful. Arrived promptly."</p>
        </li>
        <li class="text-center">
            <img src="./user-1.jpg" alt="Pic of Sarah Johnson">
            <h4 class="capitalize font-bold text-xl">Sarah Johnson</h4>
            <p>"Loved the French toast, perfectly balanced and rich. will order again."</p>
        </li>
    </ul>
</article>

<style>
    #testimonials {justify-content: center;}

    #testimonials ul {
        width: var(--width);
        margin: 0 auto;
        display: flex;
        gap: 15px;
        scroll-snap-type: x mandatory;
        scroll-behavior: smooth;
        anchor-name: --anchor;
        overflow-x: auto;
        scroll-marker-group: after;
    }

    #testimonials ul::scroll-marker-group{
        display: flex;
        justify-content: center;
        gap: .5em;
        margin-top: 30px;
    }

    #testimonials ul::-webkit-scrollbar {display: none;}

    #testimonials ul::scroll-button(right), #testimonials ul::scroll-button(left) {
        content: '»';
        background-color: transparent;
        font-size: 40px;
        border: 0;
        position: fixed;
        position-anchor: --anchor;
        position-area: right center;
        color: var(--sec);
        cursor: pointer;
    }
    #testimonials ul::scroll-button(left) {
        content: '«';
        position-area: left center;
    }
    #testimonials ul::scroll-button(right):disabled, #testimonials ul::scroll-button(left):disabled {opacity: .5;}

    #testimonials ul li {
        height: 350px;
        scroll-snap-align: start;
        display: flex;
        flex-direction: column;
        align-items: center ;
        justify-content: center;
        gap: 10px;
        flex: 0 0 400px;
    }

    #testimonials ul li img {
        border-radius: 50%;
        width: 200px;
    }

    #testimonials ul li::scroll-marker {
        width: .8em;
        height: .8em;
        background-color: var(--text);
        border-radius: 50%;
        transition: var(--trans);
        content: 'dff';
        cursor: pointer;
        color: transparent;
    }

    #testimonials ul li::scroll-marker:hover {
        background-color: var(--sec);
    }
    #testimonials ul li::scroll-marker:target-current {
        background-color: var(--sec);
        scale: 1.25;
    }

    @media (max-width: 450px) {
        #testimonials ul li {flex: 0 0 100%;}
    }
</style>