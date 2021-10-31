<div class='wrapper'>
    <div class="marquee">
        <p>
            Die Libel \\
            Folke Sverdrup Saenger \\
            Noah Syrkis \\
            Otto Lotz \\
            Thor Tao Hansen
            The Libel \\
        </p>
    </div>
</div>

<style>
    .wrapper {
        max-width: 100%;
        overflow: hidden;
        position: fixed;
    }

    .marquee {
        background: #da3527;
        white-space: nowrap;
        overflow: hidden;
        display: inline-block;
        animation: marquee 10s linear infinite;
    }

    .marquee p {
        display: inline-block;
        writing-mode: vertical-lr;
    }

    @keyframes marquee {
        0% {
            transform: translate3d(0, 0, 0);
        }
        100% {
            transform: translate3d(0, -50%, 0);
        }
    }

    #text span {
        overflow: hidden;
        display: inline-block;
        animation: marquee 10s linear infinite;
        margin: 10px 0;
    }
    .wrapper {
        overflow: hidden;
        color: white;
    }
    .marquee {
        white-space: nowrap;
        overflow: hidden;
        display: inline-block;
        animation: marquee 10s linear infinite;
    }

    .marquee p {
        display: inline-block;
        margin: 10px;
    }

    @keyframes text {
        0% {
            transform: translate3d(0, 0, 0);
        }
        100% {
            transform: translate3d(-50%, 0, 0);
        }
    }
</style>
