<script>
export default {
    data() {
        return {    
            imageUrls: [
        "src/assets/img/partner/h5-client-1.png",
        "src/assets/img/partner/h5-client-2.png",
        "src/assets/img/partner/h5-client-3.png",
        "src/assets/img/partner/h5-client-4.png",
        "src/assets/img/partner/h5-client-5.png",       
      ],
            
}
}}
</script>


<template>    
    <section class="container"> 
        <div class="image-container">
            <img v-for="(imageUrl, index) in imageUrls" :key="index" :src="imageUrl" alt="Partner Image">
        </div>
    </section>
    <hr>
</template>
  

<style scoped lang="scss">
img{
    width:calc(100%/5) ;
    margin-bottom: 7rem;
}

</style>