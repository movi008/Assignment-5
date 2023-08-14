<script setup>
import { inject } from 'vue'
const slider = inject('slider')
const piechart = inject('piechart')
</script>

<template>
    <div class="grid place-items-center">
        <div class="my-2">
            <label class="relative inline-flex items-center cursor-pointer">
                <input type="checkbox" v-model="slider" class="sr-only peer">
                <div
                    class="w-14 h-7 bg-gray-200 peer-focus:outline-none peer-focus:ring-4 peer-focus:ring-blue-300 dark:peer-focus:ring-blue-800 rounded-full peer dark:bg-gray-700 peer-checked:after:translate-x-full peer-checked:after:border-white after:content-[''] after:absolute after:top-0.5 after:left-[4px] after:bg-white after:border-gray-300 after:border after:rounded-full after:h-6 after:w-6 after:transition-all dark:border-gray-600 peer-checked:bg-blue-600">
                </div>
                <span class="ml-3 text-sm font-medium dark:text-gray-900">Mount / UnMount Slider</span>
            </label>
        </div>
        <div class="my-2" style="margin-left: 13px">
            <label class="relative inline-flex items-center cursor-pointer">
                <input type="checkbox" v-model="piechart" class="sr-only peer">
                <div
                    class="w-14 h-7 bg-gray-200 peer-focus:outline-none peer-focus:ring-4 peer-focus:ring-blue-300 dark:peer-focus:ring-blue-800 rounded-full peer dark:bg-gray-700 peer-checked:after:translate-x-full peer-checked:after:border-white after:content-[''] after:absolute after:top-0.5 after:left-[4px] after:bg-white after:border-gray-300 after:border after:rounded-full after:h-6 after:w-6 after:transition-all dark:border-gray-600 peer-checked:bg-blue-600">
                </div>
                <span class="ml-3 text-sm font-medium text-gray-900 dark:text-gray-900">Mount / UnMount Piechart</span>
            </label>
        </div>
    </div>
</template>

<style lang="scss" scoped></style>