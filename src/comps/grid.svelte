<script>
    import Tile from './tile.svelte';

    let tiles = [
        {"name": "square"}, {"name": "us-and-them"}, {"name": "everythingism"},
        {"name": "artbreeder_sketch"}, {"name": "the-doubt-and-the-fun-alt"}, {"name": "square"},
        {"name": "mechanical-turk"}, {"name":"artbreeder_portrait"},  {"name": "the-doubt-and-the-fun"},
        {"name": "square"}, {"name": "us-and-them-alt"}
    ]
</script>

<div class='tiles'>
    {#each tiles as tile}  
        <Tile background={tile.name} tilt="red-square"><div class='tile'></div></Tile>
    {/each}
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
    @media only screen and (max-width: 800px) {
        .tiles { grid-template-columns: 1fr; }
    }
    @media only screen and (min-width: 800px) {
        .tiles { grid-template-columns: 1fr 1fr; }
    }
    @media only screen and (min-width: 1200px) {
        .tiles { grid-template-columns: 1fr 1fr 1fr; }
    }
</style>
