<script>
import AppTestimonial from "./components/AppTestimonial.vue";
import AppEmpowering from "./components/AppEmpowering.vue";
import AppFooter from "./components/AppFooter.vue";
import AppHeader from "./components/AppHeader.vue";
import AppToutoring from "./components/AppToutoring.vue";
import CarouselHeader from "./components/CarouselHeader.vue";
import AppPossibilities from "./components/AppPossibilities.vue";
import AppCourses from "./components/AppCourses.vue";
import AppPlans from "./components/AppPlans.vue";

export default {
  components: {
    AppHeader,
    CarouselHeader,
    AppFooter,
    AppToutoring,
    AppEmpowering,
    AppTestimonial,
    AppPossibilities,
    AppCourses,
    AppPlans
},    
  
}

</script>

<template>
  <div class="header">
    <AppHeader />
    <div class="carousel">
      <CarouselHeader />
    </div>    
  </div>  
  <AppToutoring/>
  <AppEmpowering/>
  <AppTestimonial/>
  <AppPossibilities/>
  <AppCourses/>
  <AppPlans/>
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
