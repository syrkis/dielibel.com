<script>
    import Tiles from '../comps/tiles.svelte';
    import Banner from '../comps/banner.svelte';
</script>

<div class='wrapper'>
    <div id="banner-wrapper">
        <div id='banner'>
            <Banner />
        </div>
    </div>
    <div id="tiles">
        <Tiles />
    </div>
</div>

<style>
    .wrapper {
    }
    #banner {
        width: 100vh;
    }
      
</style>
