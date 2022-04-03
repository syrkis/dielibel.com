<script>
    import Tile from './tile.svelte';

    let tiles = [
        {},
        {},
        {},
        {},
        {},
        {},
        {},
        {},
        {},
        {},
        {},
        {}
    ]
</script>

<div class='tiles'>
    <Tile background="favicon" margin="75px" tilt="red-square"><div class='tile'></div></Tile>
    <a href="everythingism"><Tile background="everythingism" margin="75px" tilt="none"><div class='tile'></div></Tile></a>
    <a href="everythingism"><Tile background="everythingism" margin="75px" tilt="none"><div class='tile'></div></Tile></a>
    <a href="everythingism"><Tile background="everythingism" margin="75px" tilt="none"><div class='tile'></div></Tile></a>
    <a href="everythingism"><Tile background="everythingism" margin="75px" tilt="none"><div class='tile'></div></Tile></a>
    <a href="everythingism"><Tile background="everythingism" margin="75px" tilt="none"><div class='tile'></div></Tile></a>
    <a href="everythingism"><Tile background="everythingism" margin="75px" tilt="none"><div class='tile'></div></Tile></a>
    <a href="everythingism"><Tile background="everythingism" margin="75px" tilt="none"><div class='tile'></div></Tile></a>
    <a href="everythingism"><Tile background="everythingism" margin="75px" tilt="none"><div class='tile'></div></Tile></a>
    <a href="everythingism"><Tile background="everythingism" margin="75px" tilt="none"><div class='tile'></div></Tile></a>
    <a href="everythingism"><Tile background="everythingism" margin="75px" tilt="none"><div class='tile'></div></Tile></a>
    <a href="everythingism"><Tile background="everythingism" margin="75px" tilt="none"><div class='tile'></div></Tile></a>
</div>

<style>
    .tiles {
        display: grid;
        grid-gap: 5px;
        padding: 10px;
    }
    .tiles .tile {
        aspect-ratio: 1;
        height: 75%;
        display: flex;
        justify-content: center;
    }
    @media only screen and (max-width: 900px) {
        .tiles { grid-template-columns: 1fr; }
    }
    @media only screen and (min-width: 900px) {
        .tiles { grid-template-columns: 1fr 1fr; }
    }
    @media only screen and (min-width: 1200px) {
        .tiles { grid-template-columns: 1fr 1fr 1fr; }
    }
</style>
