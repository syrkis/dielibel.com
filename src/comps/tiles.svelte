<script>
    import Tile from './tile.svelte';
    import Template from './tiles/template.svelte';
    import Definition from './tiles/definition.svelte';
    import Newsletter from './tiles/newsletter.svelte';
</script>

<div class='tiles'>
    <Tile border="none" tilt="false"><div class='tile'><Definition /></div></Tile>
    <Tile background="#da3527" margin="10vh"><div class='tile'></div></Tile>
    <Tile><div class='tile'><Template /></div></Tile>
    <Tile><div class='tile'><Template /></div></Tile>
    <Tile><div class='tile'><Template /></div></Tile>
    <a href="https://dielibel.substack.com" target=_blank ><Tile><div class='tile'><Newsletter /></div></Tile></a>
</div>

<style>
    .tiles {
        display: grid;
        grid-gap: 5px;
    }
    .tiles .tile {
        aspect-ratio: 1;
        display: flex;
        justify-content: center;
    }
    @media only screen and (max-width: 600px) {
        .tiles {
            grid-template-columns: 1fr;
        }
    }
    @media only screen and (max-width: 1000px) and (min-width: 600px) {
        .tiles {
            grid-template-columns: 1fr 1fr;
        }
    }
    @media only screen and (min-width: 1000px) {
        .tiles {
            grid-template-columns: 1fr 1fr 1fr;
        }
    }
</style>
