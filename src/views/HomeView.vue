<script setup>
import { ref } from 'vue'
import { RouterLink } from 'vue-router'
import { EffectCoverflow } from 'swiper'
import { Swiper, SwiperSlide } from 'swiper/vue'
import BaseFooter from '../components/BaseFooter.vue'

import 'swiper/css'
import 'swiper/css/pagination'
import 'swiper/css/effect-coverflow'
import '@/style.css'

const modules = ref([EffectCoverflow])
</script>

<template>
  <div class="center">
    <swiper
      :effect="'coverflow'"
      :grabCursor="true"
      :centeredSlides="true"
      :slidesPerView="'auto'"
      :coverflowEffect="{
        rotate: 50,
        stretch: 0,
        depth: 100,
        modifier: 1,
        slideShadows: false
      }"
      :pagination="true"
      :modules="modules"
      class="mySwiper"
    >
      <swiper-slide
        ><RouterLink to="detail/1"
          ><img src="@/assets/img/portfolio-cover-01.png" /></RouterLink></swiper-slide
      ><swiper-slide
        ><RouterLink to="detail/2"
          ><img src="@/assets/img/portfolio-cover-02.png" /></RouterLink></swiper-slide
      ><swiper-slide
        ><RouterLink to="detail/3"
          ><img src="@/assets/img/portfolio-cover-03.png" /></RouterLink></swiper-slide
      ><swiper-slide
        ><RouterLink to="detail/4"
          ><img src="@/assets/img/portfolio-cover-04.png" /></RouterLink></swiper-slide
      ><swiper-slide
        ><RouterLink to="detail/5"
          ><img src="@/assets/img/portfolio-cover-05.png" /></RouterLink></swiper-slide
      ><swiper-slide
        ><RouterLink to="detail/6"
          ><img src="@/assets/img/portfolio-cover-06.png" /></RouterLink></swiper-slide
      ><swiper-slide
        ><RouterLink to="detail/7"><img src="@/assets/img/portfolio-cover-07.png" /></RouterLink
      ></swiper-slide>
    </swiper>
  </div>
  <BaseFooter />
</template>

<style scoped>
.center {
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
</style>
