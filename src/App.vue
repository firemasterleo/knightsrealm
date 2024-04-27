<template >
  <LenisScroll/>
  <div class="iphone14topspace"></div>

  <div class="mainveil" :class="{ 'is-expanded': is_expanded }" @click="ToggleMenu"></div>
  
  <!-- for headers to work well with scrolling they need to be free within the template not within a div -->
  <div class="headercontainer" :class="{ 'ishidingheader': isHidingHeader && !isScrollingUp }"> 
    <div class="header" :class="{ 'is-expanded': is_expanded }"> 
        <!-- <div class="logo">
            <img src="./assets/unikmelogo.png" alt="proselogo">
        </div> -->

        <div class="name">
          <div class="chesslogo">
<svg fill="#000000" width="26px" height="26px" viewBox="0 0 32 32" xmlns="http://www.w3.org/2000/svg"><path d="M 16 3 C 14.230469 3 13.058594 3.984375 12.59375 5 C 12.242188 5.769531 12.285156 6.304688 12.28125 6.75 C 11.535156 7.257813 10.75 7.90625 10.125 8.53125 C 8.726563 9.929688 7.960938 11.921875 8 14.03125 C 8.019531 15.003906 8.21875 15.980469 8.59375 16.96875 C 8.78125 17.464844 9.125 18.324219 9.4375 19.28125 C 9.75 20.238281 10 21.292969 10 22 L 9 22 C 8.96875 22 8.9375 22 8.90625 22 C 8.367188 22.035156 7.953125 22.492188 7.972656 23.03125 C 7.988281 23.570313 8.429688 23.996094 8.96875 24 L 7.1875 26.40625 L 7 26.65625 L 7 29 L 25 29 L 25 26.65625 L 24.8125 26.40625 L 23 24 C 23.359375 24.003906 23.695313 23.816406 23.878906 23.503906 C 24.058594 23.191406 24.058594 22.808594 23.878906 22.496094 C 23.695313 22.183594 23.359375 21.996094 23 22 L 22 22 C 22 19.738281 20.59375 17.664063 19.28125 16.0625 C 18.53125 15.144531 18.285156 14.984375 17.78125 14.5 C 17.960938 14.394531 18.183594 14.269531 18.3125 14.1875 C 18.472656 14.085938 18.558594 14.023438 18.59375 14 C 18.875 14 18.894531 14.046875 19.1875 14.28125 C 19.480469 14.515625 20.078125 15 20.90625 15 C 21.632813 15 22.164063 14.53125 22.4375 14.1875 C 22.6875 13.871094 22.824219 13.632813 22.84375 13.59375 C 22.933594 13.550781 23.128906 13.488281 23.375 13.3125 C 23.621094 13.136719 23.941406 12.746094 24 12.3125 C 24.058594 11.878906 23.921875 11.5 23.75 11.125 C 23.496094 10.570313 23.023438 9.933594 22.28125 9.15625 C 21.539063 8.378906 20.566406 7.554688 19.375 7.0625 C 19.285156 7.023438 19.359375 7.082031 19.3125 7.03125 C 19.265625 6.980469 19.125 6.769531 18.84375 6.5625 C 18.476563 6.292969 17.679688 6.261719 17 6.1875 L 17 3 Z M 15 5.21875 L 15 8 L 16 8 C 17.363281 8 17.664063 8.164063 17.65625 8.15625 C 17.652344 8.152344 17.660156 8.171875 17.8125 8.34375 C 17.964844 8.515625 18.261719 8.785156 18.625 8.9375 C 19.425781 9.269531 20.226563 9.917969 20.84375 10.5625 C 21.421875 11.164063 21.808594 11.761719 21.875 11.875 C 21.714844 11.953125 21.546875 12.007813 21.34375 12.25 C 21.070313 12.582031 20.972656 12.8125 20.875 12.9375 C 20.84375 12.976563 20.847656 12.988281 20.84375 13 C 20.757813 12.988281 20.699219 12.933594 20.4375 12.71875 C 20.109375 12.453125 19.457031 12 18.59375 12 C 17.9375 12 17.566406 12.300781 17.25 12.5 C 16.933594 12.699219 16.679688 12.84375 16.59375 12.875 L 16.5625 12.90625 L 16.53125 12.90625 C 16.347656 12.984375 16.03125 13 16.03125 13 L 15 12.96875 L 15 14.5625 L 15.34375 14.84375 C 15.34375 14.84375 16.53125 15.890625 17.71875 17.34375 C 18.90625 18.796875 20 20.667969 20 22 L 12 22 C 12 20.878906 11.6875 19.703125 11.34375 18.65625 C 11 17.609375 10.59375 16.695313 10.4375 16.28125 C 10.144531 15.507813 10.015625 14.707031 10 13.96875 C 9.96875 12.363281 10.542969 10.925781 11.53125 9.9375 C 12.183594 9.285156 13.15625 8.46875 13.6875 8.15625 L 14.1875 7.875 L 14.1875 7.3125 C 14.1875 6.941406 14.1875 6.320313 14.40625 5.84375 C 14.53125 5.574219 14.703125 5.367188 15 5.21875 Z M 11.5 24 L 20.5 24 L 22.75 27 L 9.25 27 Z"/></svg>          </div>

          <h1>KnightsRealm</h1>
        </div>
        <div class="hamburger" :class="{ 'is-active': is_expanded }" @click="ToggleMenu">
            <span class="bar"></span>
            <span class="bar"></span>
            <span class="bar"></span>
        </div>

        
    </div>

  
  </div>
  <div class="menuslide" :class="{ 'is-expanded': is_expanded }">

    <div class="topmenuslide" :class="{ 'is-expanded': is_expanded }">

      <div class="menu">
          <router-link class="menuitem" to="/" @click="ToggleMenu">
            <h3>Home</h3>
          </router-link>
       </div>

       
       
       <div class="menu">
                 <router-link class="menuitem" to="/Membership" @click="ToggleMenu">
                  <h3>Membership</h3>
                </router-link>
              </div>


       <div class="menu">
         <router-link class="menuitem" to="/" @click="ToggleMenu">
          <h3>Upcoming Events</h3>
        </router-link>
      </div>


       <div class="menu">
         <router-link class="menuitem" to="/" @click="ToggleMenu">
          <h3>Chess strategies and tactics</h3>
        </router-link>
      </div>


       <div class="menu">
         <router-link class="menuitem" to="/" @click="ToggleMenu">
          <h3>Accesories</h3>
        </router-link>
      </div>
      




      <div class="image">

        <img src="./assets/chesspic3.jpg" alt="">
      </div>
      <h3>Look and Feel your Best</h3>
      
      
            <div class="menuextra" :class="{ 'is-expanded': is_expanded }">
              <div class="engines, register">
                 <router-link class="menuitem" to="/MyEngines" @click="ToggleMenu">
                  <svg xmlns='http://www.w3.org/2000/svg'  viewBox='0 0 24 24' fill='#000000' width='24' height='24'><path d="M12 2a5 5 0 1 0 5 5 5 5 0 0 0-5-5zm0 8a3 3 0 1 1 3-3 3 3 0 0 1-3 3zm9 11v-1a7 7 0 0 0-7-7h-4a7 7 0 0 0-7 7v1h2v-1a5 5 0 0 1 5-5h4a5 5 0 0 1 5 5v1z"></path></svg>

                  <h3 class="signin">SIGN IN | REGISTER NOW</h3>
                </router-link>
              </div>
              <div class="engines">
                 <router-link class="menuitem" to="/MyEngines" @click="ToggleMenu">
                  <svg xmlns='http://www.w3.org/2000/svg'  viewBox='0 0 24 24' fill='#000000' width='24' height='24'><path d="M12 2C7.589 2 4 5.589 4 9.995 3.971 16.44 11.696 21.784 12 22c0 0 8.029-5.56 8-12 0-4.411-3.589-8-8-8zm0 12c-2.21 0-4-1.79-4-4s1.79-4 4-4 4 1.79 4 4-1.79 4-4 4z"></path></svg>
                  <h3>STORE LOCATOR</h3>
                </router-link>
              </div>
              <div class="engines">
                 <router-link class="menuitem" to="/MyEngines" @click="ToggleMenu">
                  <svg xmlns='http://www.w3.org/2000/svg'  viewBox='0 0 24 24' fill='#000000' width='24' height='24'><path d="M19 15v-3h-2v3h-3v2h3v3h2v-3h3v-2h-.937zM4 7h11v2H4zm0 4h11v2H4zm0 4h8v2H4z"></path></svg>
                  <h3>WISHLIST</h3>
                </router-link>
              </div>
              <div class="engines">
                 <router-link class="menuitem" to="/MyEngines" @click="ToggleMenu">
                  <h3>STYLING SESSION</h3>
                </router-link>
              </div>
              <div class="engines">
                 <router-link class="menuitem" to="/MyEngines" @click="ToggleMenu">
                  <h3></h3>
                </router-link>
              </div>
              <div class="engines">
                 <router-link class="menuitem" to="/MyEngines" @click="ToggleMenu">
                  <h3></h3>
                </router-link>
              </div>

      
            </div>


</div>



  </div>  



  <div class="routersection" :class="{ 'is-expanded': is_expanded }">
        <router-view/>

      </div>






<div class="footer" :class="{ 'is-expanded': is_expanded }">
  <div class="logoandnav">

      <div class="logoname">

      </div>


  
      <div class="socials">
        <a href="https://www.instagram.com/_unikme_couture/" target="_blank">
          <svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24' fill='#000000' width='24' height='24'><path d="M11.999 7.377a4.623 4.623 0 1 0 0 9.248 4.623 4.623 0 0 0 0-9.248zm0 7.627a3.004 3.004 0 1 1 0-6.008 3.004 3.004 0 0 1 0 6.008z"></path><circle cx="16.806" cy="7.207" r="1.078"></circle><path d="M20.533 6.111A4.605 4.605 0 0 0 17.9 3.479a6.606 6.606 0 0 0-2.186-.42c-.963-.042-1.268-.054-3.71-.054s-2.755 0-3.71.054a6.554 6.554 0 0 0-2.184.42 4.6 4.6 0 0 0-2.633 2.632 6.585 6.585 0 0 0-.419 2.186c-.043.962-.056 1.267-.056 3.71 0 2.442 0 2.753.056 3.71.015.748.156 1.486.419 2.187a4.61 4.61 0 0 0 2.634 2.632 6.584 6.584 0 0 0 2.185.45c.963.042 1.268.055 3.71.055s2.755 0 3.71-.055a6.615 6.615 0 0 0 2.186-.419 4.613 4.613 0 0 0 2.633-2.633c.263-.7.404-1.438.419-2.186.043-.962.056-1.267.056-3.71s0-2.753-.056-3.71a6.581 6.581 0 0 0-.421-2.217zm-1.218 9.532a5.043 5.043 0 0 1-.311 1.688 2.987 2.987 0 0 1-1.712 1.711 4.985 4.985 0 0 1-1.67.311c-.95.044-1.218.055-3.654.055-2.438 0-2.687 0-3.655-.055a4.96 4.96 0 0 1-1.669-.311 2.985 2.985 0 0 1-1.719-1.711 5.08 5.08 0 0 1-.311-1.669c-.043-.95-.053-1.218-.053-3.654 0-2.437 0-2.686.053-3.655a5.038 5.038 0 0 1 .311-1.687c.305-.789.93-1.41 1.719-1.712a5.01 5.01 0 0 1 1.669-.311c.951-.043 1.218-.055 3.655-.055s2.687 0 3.654.055a4.96 4.96 0 0 1 1.67.311 2.991 2.991 0 0 1 1.712 1.712 5.08 5.08 0 0 1 .311 1.669c.043.951.054 1.218.054 3.655 0 2.436 0 2.698-.043 3.654h-.011z"></path></svg>               
        </a>
  
        <svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24' fill='#000000' width='24' height='24'><path d="M19.633 7.997c.013.175.013.349.013.523 0 5.325-4.053 11.461-11.46 11.461-2.282 0-4.402-.661-6.186-1.809.324.037.636.05.973.05a8.07 8.07 0 0 0 5.001-1.721 4.036 4.036 0 0 1-3.767-2.793c.249.037.499.062.761.062.361 0 .724-.05 1.061-.137a4.027 4.027 0 0 1-3.23-3.953v-.05c.537.299 1.16.486 1.82.511a4.022 4.022 0 0 1-1.796-3.354c0-.748.199-1.434.548-2.032a11.457 11.457 0 0 0 8.306 4.215c-.062-.3-.1-.611-.1-.923a4.026 4.026 0 0 1 4.028-4.028c1.16 0 2.207.486 2.943 1.272a7.957 7.957 0 0 0 2.556-.973 4.02 4.02 0 0 1-1.771 2.22 8.073 8.073 0 0 0 2.319-.624 8.645 8.645 0 0 1-2.019 2.083z"></path></svg>
        <svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24' fill='#000000' width='24' height='24'><path fill-rule="evenodd" clip-rule="evenodd" d="M18.403 5.633A8.919 8.919 0 0 0 12.053 3c-4.948 0-8.976 4.027-8.978 8.977 0 1.582.413 3.126 1.198 4.488L3 21.116l4.759-1.249a8.981 8.981 0 0 0 4.29 1.093h.004c4.947 0 8.975-4.027 8.977-8.977a8.926 8.926 0 0 0-2.627-6.35m-6.35 13.812h-.003a7.446 7.446 0 0 1-3.798-1.041l-.272-.162-2.824.741.753-2.753-.177-.282a7.448 7.448 0 0 1-1.141-3.971c.002-4.114 3.349-7.461 7.465-7.461a7.413 7.413 0 0 1 5.275 2.188 7.42 7.42 0 0 1 2.183 5.279c-.002 4.114-3.349 7.462-7.461 7.462m4.093-5.589c-.225-.113-1.327-.655-1.533-.73-.205-.075-.354-.112-.504.112s-.58.729-.711.879-.262.168-.486.056-.947-.349-1.804-1.113c-.667-.595-1.117-1.329-1.248-1.554s-.014-.346.099-.458c.101-.1.224-.262.336-.393.112-.131.149-.224.224-.374s.038-.281-.019-.393c-.056-.113-.505-1.217-.692-1.666-.181-.435-.366-.377-.504-.383a9.65 9.65 0 0 0-.429-.008.826.826 0 0 0-.599.28c-.206.225-.785.767-.785 1.871s.804 2.171.916 2.321c.112.15 1.582 2.415 3.832 3.387.536.231.954.369 1.279.473.537.171 1.026.146 1.413.089.431-.064 1.327-.542 1.514-1.066.187-.524.187-.973.131-1.067-.056-.094-.207-.151-.43-.263"></path></svg>
        <svg xmlns='http://www.w3.org/2000/svg'  viewBox='0 0 24 24' fill='#000000' width='24' height='24'><path d="M20 4H4a2 2 0 0 0-2 2v12a2 2 0 0 0 2 2h16a2 2 0 0 0 2-2V6a2 2 0 0 0-2-2zm0 4.7-8 5.334L4 8.7V6.297l8 5.333 8-5.333V8.7z"></path></svg>
        <svg xmlns='http://www.w3.org/2000/svg'  viewBox='0 0 24 24' fill='#000000' width='24' height='24'><path d="m20.487 17.14-4.065-3.696a1.001 1.001 0 0 0-1.391.043l-2.393 2.461c-.576-.11-1.734-.471-2.926-1.66-1.192-1.193-1.553-2.354-1.66-2.926l2.459-2.394a1 1 0 0 0 .043-1.391L6.859 3.513a1 1 0 0 0-1.391-.087l-2.17 1.861a1 1 0 0 0-.29.649c-.015.25-.301 6.172 4.291 10.766C11.305 20.707 16.323 21 17.705 21c.202 0 .326-.006.359-.008a.992.992 0 0 0 .648-.291l1.86-2.171a.997.997 0 0 0-.085-1.39z"></path></svg>
        </div>
        
      </div>



  <div class="rights">
    <p>© 2024 WARDROBEKING. All rights reserved.</p>
  </div>
</div>




</template>

<style lang="scss" scoped>
@import './sass/main.scss';
</style>

<script setup>

import LenisScroll from './components/LenisScroll.vue';

import { ref, onMounted, onBeforeUnmount, onUnmounted } from 'vue';



import './sass/main.scss';




//togglemenu
const is_expanded = ref(false)

const ToggleMenu = () => {
  is_expanded.value = !is_expanded.value;
  

}



//headerbehaviour logic
const isAtTop = ref(true);
const isHidingHeader = ref(false);
const isScrollingUp = ref(false);

const translateThreshold = 100;
const bottomMargin = 50; // Adjust this margin as needed



let lastScrollTop = 0;

const handleScroll = () => {
const currentScrollTop = window.scrollY;
const maxScroll = document.documentElement.scrollHeight - window.innerHeight;




if (currentScrollTop > 0) {
  isAtTop.value = false;

  if (currentScrollTop > translateThreshold) {
    isScrollingUp.value = currentScrollTop < lastScrollTop;


        isHidingHeader.value = true;

    }
  else {
    isHidingHeader.value = false;
  }
} 
else {
  isAtTop.value = true;
  isHidingHeader.value = false;
}
if (is_expanded.value) {
  isScrollingUp.value = true; } //i used this code to turn off scrolling of the header when isexpanded condition is true

  if (currentScrollTop >= maxScroll - bottomMargin) {
      isHidingHeader.value = false;
      isScrollingUp.value = true;
    }   // i used this one to bring the header down when the footer shows up 



lastScrollTop = currentScrollTop; 
};

onMounted(() => {
window.addEventListener('scroll', handleScroll);
});

onUnmounted(() => {
window.removeEventListener('scroll', handleScroll);
});







</script>
