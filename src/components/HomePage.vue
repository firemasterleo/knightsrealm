<template>
    <div class="body">
        <div class="herocontent">
            <h2>
                "Welcome to our chess sanctuary, <br> Where minds <br> meet in <br> harmony."
            </h2>
        </div>
        <div class="image1">

<img src="../assets/chessbackground1.jpg" alt="">
</div>
        <div class="image2">

<img src="../assets/chessbackground2.png" alt="">
</div>

    </div>
</template>

<style lang="scss" scoped>
.body {
    height: 100rem;
    overflow-x: hidden;

    .herocontent {
        position: absolute;
        z-index: 15;

        width: 20rem;
        margin-left: 1.5rem;
        top: 7rem;
        h2 {
            font-size: 36px;
        font-weight: 900;
        color: #352929;
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
}


    
</style>