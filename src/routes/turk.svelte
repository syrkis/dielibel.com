<script>
    import { onMount } from 'svelte';
    import axios from 'axios';
    import SvelteMarkdown from 'svelte-markdown';

    let url = "https://raw.githubusercontent.com/";
    let file = "syrkis/writings/master/the_mechanical_turk.md"
    let source = "";
    
    onMount(async () => {
        source = await axios.get(url + file);
        source = source.data;
        console.log(source);
    });
</script>


<div class='wrapper'>
    <div>
        <div>
            {#await source then source}
                <SvelteMarkdown {source} />
            {/await}
        </div>
    </div>
</div>

<style>
    .wrapper {
        line-height: 2em;
        width: 400px;
        max-width: 95%;
        font-size: 1.2em;
        text-align: justify;
        width: 90%;
        max-width: 1000px;
        margin: auto;
    }
    .header {
        text-align: center; 
    }
    #title {
        text-transform: uppercase;
    }
</style>
