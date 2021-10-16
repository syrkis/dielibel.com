<script>
    import VanillaTilt from 'vanilla-tilt';
    import { onMount } from 'svelte';

    export let background;

    onMount(async () => {
            const element = document.querySelectorAll(".js-tilt");
            VanillaTilt.init(element, { max: 3, scale: 1.1, speed: 1000 });
    });
</script>

<div class='js-tilt' style="background: {background};">
    <div class="inner">
        <div class='wrapper'>
            <slot />
        </div>
    </div>
</div>

<style>
    .js-tilt {
        border: solid #da3527 2px;
        transform-style: preserve-3d;
        transform: perspective(1000px);
    }
    .inner {
        transform: translateZ(100px);
    }
</style>
