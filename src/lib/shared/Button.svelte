<script>
    export let flex = false;
    export let rad = false;
    export let full = false;
    export let ter = false;
    export let inverted = false;
    export let faded = false;
    export let type = 'button';
</script>

<button 
    class="btn capitalize"
    type={type === 'button' ? 'button' : 'submit'}
    class:full={full}
    class:flex={flex}
    class:rad={rad}
    class:faded={faded}
    class:ter={ter}
    class:inverted={inverted}
    on:click
>
    <slot></slot>
</button>

<style>
    .btn {
        background-color: var(--sec);
        border: 2px solid transparent;
        border-radius: var(--rad);
        color: var(--ter);
        padding: 5px 12px;
        cursor: pointer;
        transition: var(--trans);
    }
    .btn:hover {
        background-color: transparent;
        color: var(--pri);
        border: 2px solid var(--pri);
    }

    .btn.ter {
        background-color: var(--ter);
        color: var(--pri);
    }
    .btn.ter:hover {
        background-color: transparent;
        color: var(--ter);
        border: 2px solid var(--ter);
    }
    
    .btn.faded {
        background-color: transparent;
        color: var(--pri);
        border: 0;
    }
    .btn.faded:hover, .btn.inverted:hover {
        background-color: var(--sec);
        color: var(--ter);
    }
    
    .btn.inverted {
        background-color: transparent;
        color: var(--pri);
        border: 2px solid var(--pri);
    }
    .btn.inverted:hover {
        border: 2px solid transparent;
    }

    .full {
        width: 100% !important;
    }

    .flex {
        display: flex;
        align-items: center;
        gap: 5px;
    }

    .rad {border-radius: var(--rad2);}
</style>