<script>
    import Tiles from '../comps/tiles.svelte';
</script>

<div class='wrapper'>
    <div id="banner">
        <p>Die Libel | The, Bart, The | Die, Bart, Die </p>
    </div>
    <div id="tiles">
        <Tiles />
    </div>
</div>

<style>
    #tiles {
    }
    #banner {
        position: absolute;
        float: left;
        left: 0;
    }
    #banner p {
        transform: rotate(-90deg);
    }
</style>
