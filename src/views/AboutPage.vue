<script setup>
import { ref, onMounted } from 'vue'
import { Cloudinary } from '@cloudinary/url-gen'
import { AdvancedImage } from '@cloudinary/vue'

// Create a Cloudinary instance and set your cloud name.
const cld = new Cloudinary({
  cloud: {
    cloudName: 'dhk17n0ax'
  }
})
const images = ref([])

onMounted(async () => {
  for (let i = 1; i <= 5; i++) {
    images.value.push({ img: cld.image(`portfolio/3/${i}`), id: i })
  }
})
</script>
<template>
  <div class="box"></div>
  <div class="text-container">
    <p>
      Hi there! My name is Enari and I'm from China,currently living in Tokyo. I am looking for my
      first work experience in IT. I graduated at China Academy of Art, and during this period I
      learn knowledge about Art Design.After graduating from college,I worked as a graphic designer
      for 3 years in 2 companies, Joyoung and Ad.Quan.
    </p>
    <p>
      I consider myself to be honest, responsible, as well as detail-oriented, looking forward to
      continue learning new skills and web technologies for my professional growth. I'm also
      strongly committed to the projects I'm assigned to, giving my best to complete the tasks with
      the best possible outcome.
    </p>
  </div>
  <div v-for="image in images" :key="image.id">
    <AdvancedImage :cldImg="image.img" />
  </div>
</template>
<style scoped>
.box {
  width: 100vw;
  margin: auto;
  background-color: red;
  height: 400px;
}
.text-container {
  margin: 5rem 6rem;
  text-align: justify;
}
</style>
