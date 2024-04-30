<template>
    <div class="body">
        <div class="section1">

            <div class="herocontent">
                <h2>
                    "Welcome to KnightsRealm, <br> A sanctuary Where minds  <br> meet in <br> harmony."
                </h2>
                <button>
                    Membership
                </button>

            </div>
            <div class="image1">
    
    <img src="../assets/chessbackground1.jpg" alt="">
    </div>
            <div class="image2">
                <img src="../assets/chessbackground2.png" alt="">
    </div>
        </div>

        <!-- <div class="aboutus">
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
        </div> -->
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

<style lang="scss" >
.body {
    height: 200vh;
    overflow-x: hidden;

    .section1 {
        position: relative;
        // border: solid blue;

        .herocontent {
            position: absolute;
            z-index: 15;
    
            width: 274px;
            height: 315px;
            // border: solid;
            // margin-left: 1.5rem;
            top: 32px;
            left: 16px;
            display: flex;
            flex-direction: column;
            gap: 23px;
            h2 {
                // border: solid red;
                height: 246px;
                font-size: 34px;
            font-weight: 600;
            line-height: 2.6rem;
            word-spacing: 5px;
            letter-spacing: 1.4px;
            color: #cdc5c5;
            font-family: "Fondamento", cursive;
        }
        button {
            width: 182px;
            height: 46px;
            border: none     ;
            border-radius: 1rem;
            font-size: 24px;
            font-weight: bold;
            font-family: "Fondamento", cursive;
            letter-spacing: 1.4px;
            background-color: #352929;
            color: #cdc5c5;
        }
    }
    
        .image1 {
            position: absolute;
            width: 100vw;
            height: 100vh;
            z-index: 10;
            overflow: hidden;
            
            img {
                position: relative;
                bottom: 115px;
                right: 41px;
                width:  625px;
                height: 999px;
                // border: solid blue;
                // height: 100%;
                object-fit: cover;
                opacity: 85%;
                // transform: scale(1.05) translateX(2%); /* Increase the scale to zoom in by 20% */
    
    
            }
        }
    
        .image2 {
            // position: absolute;
            // top: 0;
            
            width: 100vw;
            height: 94vh;
            overflow: hidden;

            
            // border: solid red;
            img {
                width: 1929px;
                height: 1280px;
                bottom: 115px;
            left: -620px;
            position: relative;

                object-fit: cover;
                opacity: 30%;
                // transform: scale(1.7) translateX(4%); /* Increase the scale to zoom in by 20% */
    
    
    
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


@media (max-width: 380px) {

    .body {

        .section1 {
          position: relative;
        //   border: solid blue;
    
          .herocontent {
              position: absolute;
              z-index: 15;
              border: solid blue;

      
              width: 274px;
              height: 315px;
            //   border: solid;
              // margin-left: 1.5rem;
              top: 32px;
              left: 16px;
              display: flex;
              flex-direction: column;
              gap: 23px;
              h2 {
                //   border: solid red;
                  height: 246px;
                  font-size: 30px;
              font-weight: 600;
              line-height: 2.6rem;
              word-spacing: 5px;
              letter-spacing: 1.4px;
              color: #cdc5c5;
              font-family: "Fondamento", cursive;
          }
          button {
              width: 150px;
              height: 46px;
              border: none     ;
              border-radius: 1rem;
              font-size: 20px;
              font-weight: bold;
              font-family: "Fondamento", cursive;
              letter-spacing: 1.4px;
              background-color: #352929;
              color: #cdc5c5;
          }
      }
      
          .image1 {
              position: absolute;
              width: 100vw;
              height: 100vh;
              z-index: 10;
              overflow: hidden;
            //   border: solid;
              
              img {
                  position: relative;
                  bottom: 115px;
                  right: 41px;
                  width:  625px;
                  height: 999px;
                  // border: solid blue;
                  // height: 100%;
                  object-fit: cover;
                  opacity: 85%;
                  transform: scale(0.86) translateX(-7%); /* Increase the scale to zoom in by 20% */
      
      
              }
          }
      
          .image2 {
              // position: absolute;
              // top: 0;
              
              width: 100vw;
              height: 94vh;
              overflow: hidden;
    
              
              // border: solid red;
              img {
                  width: 1929px;
                  height: 1280px;
                  bottom: 115px;
              left: -620px;
              position: relative;
    
                  object-fit: cover;
                  opacity: 30%;
                  // transform: scale(1.7) translateX(4%); /* Increase the scale to zoom in by 20% */
      
      
      
              }
          }
      }
    
    
      .section2 {
          position: relative;
          overflow-x: auto;
          border: solid red;
      }
    
    
    }

    }    
    


    
</style>