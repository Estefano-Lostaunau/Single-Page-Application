<script setup>
import { ref } from "vue";


import Calendar from 'primevue/calendar';


const date = ref();
</script>

<template>
  <div class="card flex justify-content-center">
    <Calendar v-model="date" />
  </div>
</template>

<style scoped>

</style>