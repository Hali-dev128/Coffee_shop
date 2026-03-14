<article id="menu">
    <div>
        <h3 class="title font-bold text-4xl relative">OUR MENU</h3>
        
        <ul>
            <li class="toScrollAnimate">
                <img src="./hot-beverages.png" alt="hot-beverages">
                <h4 class="capitalize font-bold text-xl">hot beverages</h4>
                <p class="text-center">Wide range of Steaming hot coffee to make you fresh and light.</p>
            </li>
            <li class="toScrollAnimate">
                <img src="./cold-beverages.png" alt="cold-beverages">
                <h4 class="capitalize font-bold text-xl">cold beverages</h4>
                <p class="text-center">Creamy and frothy cold coffee to make you cool.</p>
            </li>
            <li class="toScrollAnimate">
                <img src="./refreshment.png" alt="refreshment">
                <h4 class="capitalize font-bold text-xl">refreshment</h4>
                <p class="text-center">Fruithy and icy refreshing drink to make you feel refreshed.</p>
            </li>
            <li class="toScrollAnimate">
                <img src="./special-combo.png" alt="special-combo">
                <h4 class="capitalize font-bold text-xl">special combo</h4>
                <p class="text-center">Your favourite eating and drinking combinations.</p>
            </li>
            <li class="toScrollAnimate">
                <img src="./desserts.png" alt="desserts">
                <h4 class="capitalize font-bold text-xl">desserts</h4>
                <p class="text-center">Satiate your palate and take you on a culinary treat.</p>
            </li>
            <li class="toScrollAnimate">
                <img src="./burger-frenchfries.png" alt="burger-frenchfries">
                <h4 class="capitalize font-bold text-xl">burger frenchfries</h4>
                <p class="text-center">Quick bites to satisfy your small size hunger.</p>
            </li>
        </ul>
    </div>
</article>

<style>
    #menu {
        padding: 68px 0;
        background-color: var(--text);
        color: var(--pri);
    }

    #menu > div {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        gap: calc(var(--gap) + 20px); 
    }

    p{max-width: 35ch;}

    li {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 5px;
        margin-bottom: 50px;
    }
    li img {
        height: 300px;
        max-width: 300px;
    }

    @media(max-width: 350px) {
        li img {
            height: 180px;
            max-width: 180px;
        }
    }
</style>