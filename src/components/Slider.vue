<script setup>
import { ref, onMounted, onBeforeUnmount } from 'vue'
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel'
import 'vue3-carousel/dist/carousel.css'

const images = ref(null);

onMounted(() => {
  images.value = [
    'https://source.unsplash.com/random/300x400?sig=1',
    'https://source.unsplash.com/random/300x400?sig=2',
    'https://source.unsplash.com/random/300x400?sig=3',
    'https://source.unsplash.com/random/300x400?sig=4',
    'https://source.unsplash.com/random/300x400?sig=5',
  ];
})

onBeforeUnmount(() => {
  alert('This alert from - onBeforeUnmount ')
})


</script>


<template>
  <div>
    <carousel :items-to-show="1.5" :autoplay="150000" :wrap-around="true" :pauseAutoplayOnHover="false">
      <slide v-for="image, index in images" :key="index">
        <div class="carousel__item">
          <img :src="image" :alt="image">
        </div>
      </slide>
      <template #addons>
        <navigation />
        <pagination />
      </template>
    </carousel>
  </div>
</template>

<style>
.carousel__slide--active {
  width: 85% !important;
}

.carousel__slide--prev {
  margin: -38px !important;
}
</style>