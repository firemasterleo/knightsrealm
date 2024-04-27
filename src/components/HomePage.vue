<template>
    <div class="body">
        <div class="herocontent">
            <h2>
                "Welcome to KnightsRealm, <br> A sanctuary Where minds meet in <br> harmony."
            </h2>
        </div>
        <div class="image1">

<img src="../assets/chessbackground1.jpg" alt="">
</div>
        <div class="image2">

<img src="../assets/chessbackground2.png" alt="">
</div>

<div class="section2">

</div>

<div class="section3">
    <div class="widget">
        <iframe src="https://fritz.chessbase.com" style="width:760px;height:480px"></iframe>    </div>
</div>
    </div>
</template>

<style lang="scss" scoped>
.body {
    // height: 100rem;
    overflow-x: hidden;

    .herocontent {
        position: absolute;
        z-index: 15;

        width: 22rem;
        margin-left: 1.5rem;
        top: 7rem;
        h2 {
            font-size: 34px;
        font-weight: 600;
        color: #cdc5c5;
        font-family: "Fondamento", cursive;
        }
    }

    .image1 {
        position: absolute;
        width: 100vw;
        height: 100vh;
        z-index: 10;
        overflow: hidden;
        
        img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            opacity: 85%;
            transform: scale(1.05) translateX(2%); /* Increase the scale to zoom in by 20% */


        }
    }

    .image2 {
        width: 100vw;
        height: 100vh;
        overflow: hidden;
        
        img {
            width: 100%;
            height: 100%;
            margin-left: 4rem;
            object-fit: cover;
            opacity: 30%;
            transform: scale(1.7) translateX(4%); /* Increase the scale to zoom in by 20% */



        }
    }

    .section2 {
        height: 40rem;
        background-color: #cdc5c5;
        margin-top: -4rem;
        // position: relative;
        // z-index: 15;
    }

    .section3 {
        overflow-x: auto;
    }
}


    
</style>