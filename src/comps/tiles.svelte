<script>
    import Tile from './tile.svelte';
    import Images from './tiles/images.svelte';
    import Definition from './tiles/definition.svelte';
    import Newsletter from './tiles/newsletter.svelte';
    import Everythingism from './tiles/everythingism.svelte';
    import Turk from './tiles/turk.svelte';
    import Drawing from './tiles/drawing.svelte';
</script>

<div class='tiles'>
    <a href="https://dielibel.substack.com"><Tile background="#da3527" margin="10vh" tilt="red-square"><div class='tile'></div></Tile></a>
    <!--<Tile border="None"  margin="10vh"><div class='tile'></div></Tile>-->
</div>

<style>
    #interviewer {
        background: url('https://syrkis.ams3.cdn.digitaloceanspaces.com/noah/bciioi/1.jpg');

    }
    .tiles {
        display: grid;
        grid-gap: 5px;
        padding: 10px;
    }
    .tiles .tile {
        aspect-ratio: 1;
        height: 100%;
        display: flex;
        justify-content: center;
    }
    @media only screen and (max-width: 600px) {
        .tiles { grid-template-columns: 1fr; }
    }
    /*@media only screen and (max-width: 1200px) and (min-width: 600px) {
        .tiles { grid-template-columns: 1fr 1fr; }
    }
    @media only screen and (min-width: 1200px) {
        .tiles { grid-template-columns: 1fr 1fr 1fr; }
    }*/
</style>
