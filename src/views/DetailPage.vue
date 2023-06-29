<script setup>
import { ref, onMounted } from 'vue'
import { useRoute } from 'vue-router'
import { Cloudinary } from '@cloudinary/url-gen'
import { AdvancedImage } from '@cloudinary/vue'

const route = useRoute()
const id = ref(route.params.id)
const images = ref([])
// Create a Cloudinary instance and set your cloud name.
const cld = new Cloudinary({
  cloud: {
    cloudName: 'dhk17n0ax'
  }
})

onMounted(async () => {
  for (let i = 1; i <= 5; i++) {
    images.value.push({ img: cld.image(`portfolio/${id.value}/${i}`), id: i })
  }
})
</script>

<template>
  <section>
    <div class="text-contanier" v-if="id == 1">
      <div><h1 class="title">ZOOMILY Branding Design</h1></div>
      <p>
        Zoomily is a pet brand for which a visual identity (VI) system has been created. The color
        scheme is inspired by the refined colors prevalent in popular Chinese court dramas from
        2018. The brand primarily targets female customers and incorporates elements from brands
        favored by women. A black cat character has been introduced as well to enhance the brand's
        recognition. The design project also includes some packaging applications.
      </p>
    </div>
    <div class="text-contanier" v-if="id == 2">
      <div><h1 class="title">Joyoung New Year Package Design</h1></div>
      <p>
        Joyoung, as a well-known brand in the small home appliances industry, distributes New Year
        gift packs to employees and major customers to enhance brand recognition. The inspiration
        for this design came from three of Joyoung's main products of 2020 - a water dispenser, a
        rice cooker, and a cooking machine. The visuals prominently feature Joyoung's brand symbol,
        the Joyoung circle, its brand color orange, classic elements like soymilk, along with some
        classic Chinese New Year elements.
      </p>
    </div>
    <div class="text-contanier" v-if="id == 3">
      <div><h1 class="title">Tencent Public Welfare Gift</h1></div>
      <p>
        In Tencent's public welfare fundraising campaign, many enterprises have participated in
        creating social public welfare activities. Tencent public welfare recorded their deeds and
        awarded them, and summarized them in this 100-day plan as a gift for all participants and
        participating youth. The overall packaging is made of PVC shell and special public welfare
        paper, and the 100-day plan includes a to-do list and special stickers.
      </p>
    </div>
    <div class="text-contanier" v-if="id == 4">
      <div><h1 class="title">Carnivo Art Toy Design</h1></div>
      <p>
        For the special holiday of Children's Day, Carnival Advertising Company hopes to give each
        of its major clients a gift that brings back childhood innocence. By co-branding with the IP
        image of "little white" from ThinkBig, various gaming elements are used to represent the
        diverse creativity that bursts forth from play among advertisers. The gift is packaged in a
        transparent PVC box containing a skateboard and a roly-poly toy figure of "little white".
      </p>
    </div>
    <div class="text-contanier" v-if="id == 5">
      <div><h1 class="title">Joyoung Recruit</h1></div>
      <p>
        Campus recruitment is a crucial initiative for major companies to recruit new talent.
        Despite being a renowned brand in the small home appliances industry, Joyoung is perceived
        by young people as a traditional, outdated brand known for soymilk machines. The challenge
        of this project is to visually alter the brand image of Joyoung in the minds of young
        people, while keeping the brand's DNA intact, and attract more young people to work at
        Joyoung. The final visual output chose to use large areas of orange, the brand symbol and
        font of Joyoung in a glass texture, and fun typography.
      </p>
    </div>
    <div class="text-contanier" v-if="id == 6">
      <div><h1 class="title">Tencent DuanWu Festival Gift</h1></div>
      <p>
        The greatest challenge for Dragon Boat Festival gift packs in the advertising industry is
        how to make them both creative and practical. Skateboarding is a popular sport among young
        people, and transforming a skateboard into a chair is both decorative and practical. Using
        the concept of "tide player", illustrations combining the Tencent penguin, Dragon Boat
        Festival elements, etc., are applied to the skateboard chair. Additionally, a carpet and
        triangle-shaped dumpling packaging are included, allowing the whole set to be taken out for
        camping or picnicking.
      </p>
    </div>
    <div class="text-contanier" v-if="id == 7">
      <div><h1 class="title">Tencent Esports Gift Pack</h1></div>
      <p>
        The Tencent Esports New Year gift pack, styled in the form of a chip bag, contains creative
        items like a calendar, stickers, and more. The centerpiece of the gift pack is the creative
        calendar that features 365 different esports highlights, esports jokes, and industry jargon.
        This allows the employees who receive the gift pack to resonate with the content every day
        for 365 days.
      </p>
    </div>
  </section>
  <section>
    <div v-for="image in images" :key="image.id">
      <AdvancedImage :cldImg="image.img" class="img-container" />
    </div>
  </section>
</template>

<style scoped>
.img-container {
  max-width: 80vw;
}
.text-contanier {
  margin-top: 6rem;
  margin-bottom: 6rem;
  display: flex;
  gap: 4rem;
}
.title {
  font-size: 60px;
  line-height: 1.2;
  white-space: pre-wrap;
}
.text-contanier p {
  text-align: justify;
  margin-top: 1rem;
}
</style>
