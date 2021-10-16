<script>
    import VanillaTilt from 'vanilla-tilt';
    import { onMount } from 'svelte';

    export let background = "none";
    export let margin = "0";
    export let border = "solid #da3527 2px";

    onMount(async () => {
            const element = document.querySelectorAll(".js-tilt");
            VanillaTilt.init(element, { max: 7, scale: 1.05, speed: 1000 });
    });
</script>

<div class='js-tilt' style="
    background: {background};
    margin: {margin};
    border: {border}
">
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
