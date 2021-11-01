<div class='wrapper'>
    <div class='box' style="--img:url(favicon.png)">
        <img class="image" src="/favicon.png">
            <div class='text' id='left'>
        <p>Lorem ipsum dolor sit amet, consectetur adipisci elit, sed eiusmod tempor incidunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrum exercitationem ullam corporis suscipit laboriosam, nisi ut aliquid ex ea commodi consequatur. Quis aute iure reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint obcaecat cupiditat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.  </p>
    </div>
    <div class='text' id='right'>
            <p>Lorem ipsum dolor sit amet, consectetur adipisci elit, sed eiusmod tempor incidunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrum exercitationem ullam corporis suscipit laboriosam, nisi ut aliquid ex ea commodi consequatur. Quis aute iure reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint obcaecat cupiditat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.  </p>
        </div>
    </div>
</div>

<style>
    .left { float: left; }
    .right { float: right; }
    .text { width: 45%; text-align: justify; display: inline-block; }

    #right:before, #left:before {
        content: ""; 
        width: 30px; 
        height: 50px;
    }

    #left:before { float: right; }
    #right:before { float: left; }

    .image {
        height: 50px;
        width: 50px;
        top: 50%;
        position: absolute;
        left: 50%;
        margin-left: -50px;
    }

    .wrapper {
        display: inline-block;
        width: 100%;
        position: absolute;
    }

</style>
