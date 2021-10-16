<div class='wrapper'>

    <!--    <aside class="rotate">Die Libel | The Libel | The, Bart, The | Noah Syrkis | Folke Sverdrup Saenger</aside>-->
    <slot />
</div>

<style>
    .wrapper {
        position: relative;
    }
    aside {
        transform: rotate(-90deg);
        transform-origin: 0 0;
    }
    .rotate {
        display: flex;
        align-items: bottom;
        justify-content: bottom ;
    }
</style>
