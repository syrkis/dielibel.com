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
    <a href="https://dielibel.substack.com"><Tile background="#da3527" margin="10vh" tilt="red-square"><div class='tile'></div></Tile></a>
    <a href="https://dielibel.substack.com"><Tile background="#da3527" margin="10vh" tilt="red-square"><div class='tile'></div></Tile></a>
    <a href="https://dielibel.substack.com"><Tile background="#da3527" margin="10vh" tilt="red-square"><div class='tile'></div></Tile></a>
    <a href="https://dielibel.substack.com"><Tile background="#da3527" margin="10vh" tilt="red-square"><div class='tile'></div></Tile></a>
    <a href="https://dielibel.substack.com"><Tile background="#da3527" margin="10vh" tilt="red-square"><div class='tile'></div></Tile></a>
    <a href="https://dielibel.substack.com"><Tile background="#da3527" margin="10vh" tilt="red-square"><div class='tile'></div></Tile></a>
    <a href="https://dielibel.substack.com"><Tile background="#da3527" margin="10vh" tilt="red-square"><div class='tile'></div></Tile></a>
    <a href="https://dielibel.substack.com"><Tile background="#da3527" margin="10vh" tilt="red-square"><div class='tile'></div></Tile></a>
    <a href="https://dielibel.substack.com"><Tile background="#da3527" margin="10vh" tilt="red-square"><div class='tile'></div></Tile></a>
    <a href="https://dielibel.substack.com"><Tile background="#da3527" margin="10vh" tilt="red-square"><div class='tile'></div></Tile></a>
    <a href="https://dielibel.substack.com"><Tile background="#da3527" margin="10vh" tilt="red-square"><div class='tile'></div></Tile></a>
    <a href="https://dielibel.substack.com"><Tile background="#da3527" margin="10vh" tilt="red-square"><div class='tile'></div></Tile></a>
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
    @media only screen and (max-width: 900px) {
        .tiles { grid-template-columns: 1fr; }
    }
    @media only screen and (min-width: 900px) {
        .tiles { grid-template-columns: 1fr 1fr; }
    }
    @media only screen and (min-width: 1200px) {
        .tiles { grid-template-columns: 1fr 1fr 1fr; }
    }
    @media only screen and (min-width: 1400px) {
        .tiles { grid-template-columns: 1fr 1fr 1fr 1fr; }
    }
</style>
