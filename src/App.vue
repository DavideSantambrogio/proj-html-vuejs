<script>
import AppHeader from './components/AppHeader.vue';

export default {
  components: {
      AppHeader,
      
    },    
  
}

</script>

<template>
  <AppHeader />
 
</template>

<style lang="scss" >
/* Importazione di stili generali e icone FontAwesome */
  @use "./style/general.scss";
  @import "@fortawesome/fontawesome-free/css/all.css"; 

</style>
