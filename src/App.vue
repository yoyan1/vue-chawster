<script setup>
import { RouterLink, RouterView } from 'vue-router'
import headr from './components/header.vue'
import Ftr from './components/footer.vue'
</script>

<template>
  <header>
      <headr/>
  </header>
  <main>  
    <RouterView/>
  </main>
  <footer>
    <Ftr/>
  </footer>
</template>

<style scoped>
</style>
