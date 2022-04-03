<script>
    import Tile from './tile.svelte';

    let tiles = [
        {"name": "square"}, {"name": "us-and-them"}, {"name": "everythingism"},
        {"name": "the-doubt-and-the-fun"}, {"name": "the-doubt-and-the-fun-alt"}, {"name": "square"},
        {"name": "us-and-them-alt"},{"name": "us-and-them"}, {"name": "us-and-them-alt"},
        {"name": "square"}, {"name": "us-and-them"}, {"name": "us-and-them"}
    ]
</script>

<div class='tiles'>
    {#each tiles as tile}  
        <Tile background={tile.name} tilt="none"><div class='tile'></div></Tile>
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
