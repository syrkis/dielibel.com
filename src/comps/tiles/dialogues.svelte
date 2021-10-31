<script>
    let dialogues = [
        "2021/10/05","2021/10/05","2021/10/05",
        "2021/10/05","2021/10/05","2021/10/05",
    ]
</script>


<div class='wrapper'>
    <div class='header'>
        <h2>
            DIALOGUES
        </h2>
    </div>
    <div>
     {#each dialogues as dialogue}
        <ul>
            <a href="/{dialogue}">
                <li>
                    — {dialogue} —
                </li>
            </a>
        </ul>
    {/each}
    </div>
</div>

<style>
    h2 { font-weight: bold;}
    .header {
        text-align: center;
        font-family: 'Roboto', sans-serif;
    }
    ul {
        list-style-type: none;
        padding: 0;
    }
</style>

