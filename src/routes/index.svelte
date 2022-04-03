<script>
    import Grid from '../comps/grid.svelte';
    import Banner from '../comps/banner.svelte';
</script>

<div class='wrapper'>
    <div id='banner'>
        <Banner />
    </div>
    <div id="tiles">
        <Grid />
    </div>
</div>

<style>
    #tiles {
        padding-left: 3em;
    }
    /*@media only screen and (max-width: 600px) {
        #banner { display: none; }
        #tiles { padding-left: 0; }
        }*/
</style>
