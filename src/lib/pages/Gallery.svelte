<article id="gallery">
    <h3 class="title font-bold text-4xl relative mt-10 mb-20">Gallery</h3>

    <ul>
        <li class="toScrollAnimate">
            <img src="./gallery-1.jpg" alt="Pic of Gallery-1">
        </li>
        <li class="toScrollAnimate">
            <img src="./gallery-2.jpg" alt="Pic of Gallery-2">
        </li>
        <li class="toScrollAnimate">
            <img src="./gallery-3.jpg" alt="Pic of Gallery-3">
        </li>
        <li class="toScrollAnimate">
            <img src="./gallery-4.jpg" alt="Pic of Gallery-4">
        </li>
        <li class="toScrollAnimate">
            <img src="./gallery-5.jpg" alt="Pic of Gallery-5">
        </li>
        <li class="toScrollAnimate">
            <img src="./gallery-6.jpg" alt="Pic of Gallery-6">
        </li>
    </ul>
</article>

<style>
    img {
        width: 100%;
        height: 100%;
        border-radius: inherit;
        transition: var(--trans);
        object-fit: cover;
    }

    li {
        height: 280px;
        cursor: zoom-in;
        overflow: hidden;
        border-radius: 10px;
    }

    li:hover img {
        scale: 1.15;
    }
</style>