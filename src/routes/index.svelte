<script>
    import Definition from '../comps/definition.svelte';
    import Newsletter from '../comps/newsletter.svelte';
</script>

<div>
    <div class='grid'>
        <div class='grid-item'><Definition /></div>
        <div class="grid-item" id="red-square"></div>
        <div class="grid-item"><Newsletter /></div>
        <div class="grid-item">4</div>
        <div class="grid-item">5</div>
        <div class="grid-item">6</div>
    </div>
</div>

<style>
    #red-square {
        background: #da3527;
        width: 100%;
    }
    .grid {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(20rem, 1fr));
        grid-auto-rows: 1fr;
        padding: 10px;
    }
    .grid::before {
        content: '';
        width: 0;
        padding-bottom: 100%;
        grid-row: 1/1;
        grid-column: 1/1;
    }
    .grid > *:first-child {
        grid-row: 1 / 1;
        grid-column: 1 / 1;
        font-align: center;
    }
</style>
