<script setup>
import { RouterView } from 'vue-router'

import NavigationBar from './components/NavigationBar.vue'

/*==================== SCROLL REVEAL ANIMATION ====================*/
// const sr = ScrollReveal({
//   distance: '60px',
//   duration: 2800
//   // reset: true,
// })

// sr.reveal(
//   `.home__data, .home__social-link, .home__info,
//            .discover__container,
//            .experience__data, .experience__overlay,
//            .place__card,
//            .sponsor__content,
//            .footer__data, .footer__rights`,
//   {
//     origin: 'top',
//     interval: 100
//   }
// )
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
