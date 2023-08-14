<script setup>
import { ref, provide } from 'vue'
import Slider from './components/Slider.vue'
import Piechart from './components/Piechart.vue'
import Buttons from './components/Buttons.vue'

const slider = ref(true)
const piechart = ref(true)

provide('slider', slider)
provide('piechart', piechart)
</script>

<template>
  <div>
    <Buttons />
    <div class="flex">
      <div class="flex-1">
        <div v-if="slider">
          <Slider />
        </div>
      </div>
      <div class="flex-1">
        <div v-if="piechart">
          <Piechart />
        </div>
      </div>
    </div>
  </div>
</template>

<style></style>
