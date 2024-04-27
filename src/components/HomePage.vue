<template>
    <div class="body">
        <div class="section1">

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
        </div>

        <div class="aboutus">
            <p>
                Join us in our quest for victory and fun,
In the heart of KnightsRealm, where games are won. <br>
A haven for enthusiasts to gather and play,
In the realm of kings and queens, where rivals hold sway. <br>
Here, pawns rise as heroes, while rooks stand tall,
As knights traverse the board, answering the call.
In friendly rivalry and spirited play,
We forge bonds of camaraderie, day by day. <br>
Amidst the clatter of pieces, joy fills the air,
Celebrating the timeless art of chess, beyond compare."


            </p>
            <p>

            </p>
        </div>
<!-- 
<div class="section2">
    <div class="widget">
        <iframe
 style="width: 100%; height: 550px; overflow: hidden;"
 src="https://playpager.com/embed/chess/index.html"
 scrolling="no">
</iframe>    
  </div>
</div>
    <div class="widget">
        <iframe src="https://liveblitz.chessbase.com" width="400" height="440"></iframe>
    </div> -->

    </div>
</template>

<style lang="scss" scoped>
.body {
    height: 100rem;
    overflow-x: hidden;

    .section1 {
        position: relative;
        // border: solid blue;

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
    }


    .section2 {
        position: relative;
        overflow-x: auto;
        border: solid red;
    }


    .aboutus {
        background-color: #cdc5c5;
        height: 40rem;
        padding-inline: 1rem;
    }
}


    
</style>