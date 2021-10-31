<script>
    import VanillaTilt from 'vanilla-tilt';
    import { onMount } from 'svelte';

    export let background = "none";
    export let margin = "0";
    export let border = "solid #da3527 1.5px";
    export let tilt = 'js-tilt';

    onMount(async () => {
            const element = document.querySelectorAll(".js-tilt");
            const redSquare = document.querySelector(".red-square");
            VanillaTilt.init(element, { max: 2, scale: 1.01, speed: 7000 });
            VanillaTilt.init(redSquare, { max: 5, scale: 1.01, speed: 7000, "full-page-listening": true, reverse: true });
    });
</script>

<div class='{tilt}' style="
    background: {background};
    margin: {margin};
    border: {border}
" >
    <div class="inner">
        <div class='wrapper'>
            <slot />
        </div>
    </div>
</div>

<style>
    .js-tilt {
        transform-style: preserve-3d;
        transform: perspective(1000px);
    }
    .inner {
        transform: translateZ(100px);
    }
</style>
