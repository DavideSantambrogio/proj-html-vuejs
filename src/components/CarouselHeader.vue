<script>
export default {
  data() {
    return {
      images: [
        "src/assets/img/carousel/h5-slide-1-background.jpg",
        "src/assets/img/carousel/h5-slide-2-background.jpg",
        "src/assets/img/carousel/h5-slide-3-background.jpg"
        
      ],
      currentIndex: 0
    };
  },
  mounted() {
    setInterval(this.nextSlide, 3000); // Cambia immagine ogni 3 secondi
  },
  methods: {
    nextSlide() {
      this.currentIndex = (this.currentIndex + 1) % this.images.length;
    }
  }
};
</script>

<template>
  <div class="carousel">
    <div v-for="(image, index) in images" :key="index" :class="{ 'active': index === currentIndex }" class="carousel-item" :style="{ 'background-image': 'url(' + image + ')' }"></div>
  </div>
</template>
<style scoped>
.carousel {
  width: 100%;
  height: var(--header-height);
  overflow: hidden;
  position: relative;
}

.carousel-item {
  width: 100%;
  height: 100%;
  background-size: cover;
  background-position: center;
  position: absolute;
  opacity: 0;
  transition: opacity 0.5s ease;
}

.carousel-item.active {
  opacity: 1;
}
</style>