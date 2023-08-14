<script setup>
import { ref, reactive, onMounted, onBeforeMount, onBeforeUnmount } from 'vue'
import { Pie } from 'vue-chartjs'

const data = reactive({
  labels: ['VueJs', 'EmberJs', 'ReactJs', 'AngularJs'],
  datasets: [
  ]
})

const options = reactive({
  responsive: true,
  maintainAspectRatio: false
})

onBeforeMount(() => {
  data.datasets = [
    {
      backgroundColor: ['#41B883', '#E46651', '#00D8FF', '#DD1B16'],
      data: [40, 20, 80, 10]
    }
  ]
})

onMounted(() => {
  options.responsive = true;
})

onBeforeUnmount(() => {
  alert('This alert from - onBeforeUnmount ')
})
</script>


<template>
  <Pie :data="data" :options="options" />
</template>