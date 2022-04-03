<script>
    import VanillaTilt from 'vanilla-tilt';
    import { onMount } from 'svelte';

    let remote = "https://syrkis.ams3.digitaloceanspaces.com/dielibel/tiles"
    export let background = "none";
    export let margin = "0";
    export let border = "solid #da3527 1.5px";
    export let tilt = 'js-tilt';

    onMount(async () => {
            const element = document.querySelectorAll(".js-tilt");
            const redSquare = document.querySelector(".red-square");
            VanillaTilt.init(element, { max: 3, scale: 1.02, speed: 5000 });
            VanillaTilt.init(redSquare, { max: 10, scale: 1.07, speed: 5000, "full-page-listening": true, reverse: true });
    });
</script>

<div class='{tilt} wrapper' style="
    margin: {margin};
" >
    <div class="inner">
        <div class='wrapper' style="background: url('{remote}/{background}.png'); background-size: cover;">
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
    .wrapper{
        background-size: cover;
    }

</style>
