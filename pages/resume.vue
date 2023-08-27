
<template>
    <h1 class="text-3xl font-medium mx-1 p-4">Resume :</h1>
    <div>
      <div ref="pdfSection" class="w-fmx-1 my-4">
        <img src="~assets\images\resumePic1.png" class="w-1/2 mx-1 my-4 " />   
      </div>
      <button @click="exportToPDF('my-pdf-file.pdf', pdfSection)" class="bg-gray-800 text-gray-300 p-3 rounded-3xl mx-1 my-4">
        Download as pdf
      </button>
    </div>
  </template>
  <script setup lang="ts">
  import { ref } from 'vue'
  import { exportToPDF } from '#imports'
  const pdfSection = ref<HTMLElement | null>(null)
  </script>