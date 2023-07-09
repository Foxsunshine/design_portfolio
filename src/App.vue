<script setup>
import { RouterView } from 'vue-router'

import NavigationBar from './components/NavigationBar.vue'
</script>

<template>
  <header>
    <div>
      <NavigationBar />
    </div>
  </header>
  <RouterView />
</template>

<style scoped>
.center {
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
</style>
