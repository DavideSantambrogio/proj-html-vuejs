<script>
import AppFooter from "./components/AppFooter.vue";
import AppHeader from "./components/AppHeader.vue";
import Carousel from "./components/Carousel.vue";

export default {
  components: {
    AppHeader,
    Carousel,
    AppFooter
},    
  
}

</script>

<template>
  <div class="header">
    <AppHeader />
    <div class="carousel">
      <Carousel />
    </div>
    
  </div>
  <AppFooter/>
  
</template>

<style lang="scss" >
/* Importazione di stili generali e icone FontAwesome */
  @use "./style/general.scss";
  @import "@fortawesome/fontawesome-free/css/all.css"; 

.header {
  position: relative;
}

.carousel {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: -1;
}

</style>
