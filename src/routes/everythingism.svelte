<script>
    import { onMount } from 'svelte';
    import axios from 'axios';
    import SvelteMarkdown from 'svelte-markdown';

    let url = "https://raw.githubusercontent.com/syrkis/writings/master/everythingism.md"
    let source = "";
    
    onMount(async () => {
        source = await axios.get(url);
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
