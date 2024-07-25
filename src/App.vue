<template>
  
  <shopHeader/>

  <RouterView />

  <shopFooter/>
  
</template>

<script setup>
import { RouterLink, RouterView } from 'vue-router'
import shopHeader from './components/header.vue'
import shopFooter from './components/shopFooter.vue';

</script>

<style scoped>

</style>
