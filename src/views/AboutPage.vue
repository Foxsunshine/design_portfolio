<template>
  <div class="container row">
    <div class="common-box col-9">
      <div class="title-box">
        <h1 class="common-big-title">I'm Jiang Cheng,</h1>
        <h1 class="common-big-title">working as a Developer in Tokyo。</h1>
      </div>
      <div class="content-box">
        <p>
          I'm Jiang Cheng, a junior developer currently working in a Japanese financial company in
          Tokyo<span>🗼</span>. I'm dedicating myself to the learning of coding, finding immense joy
          in gaining new knowledge. Previously, I spent three years as a graphic designer after
          graduating from the China Academy of Art, which helps me a lot even though I am working in
          a total different area.
        </p>
        <p>
          Beyond coding, I have a deep fondness for exploring the breathtaking landscapes and
          culinary delights of Japan, as well as staying home for a good game or movie.Thank you so
          much for taking a moment to learn more about me!<span>🫡</span>
        </p>
      </div>
    </div>
    <div class="common-box col-3">
      <div>
        <h2 class="common-title">What I Like</h2>
        <ul class="content-box">
          <li>Chat-gpt</li>
          <li>Sleep Early</li>
          <li>Walk Around</li>
          <li>Yummy Food</li>
        </ul>
        <h2 class="common-title">What I'm learning</h2>
        <ul class="content-box">
          <li>日本語</li>
          <li>Springboot</li>
          <li>BackEnd</li>
          <li>FrontEnd</li>
        </ul>
        <h2 class="common-title">Work</h2>
        <ul class="content-box">
          <RouterLink to="detail/1"><li>Zoomily</li></RouterLink>
          <RouterLink to="detail/2"><li>Joyoung New Year Package</li></RouterLink>
          <RouterLink to="detail/3"><li>Tencent Public Welfare Gift</li></RouterLink>
          <RouterLink to="detail/4"><li>Carnivo Art Toy</li></RouterLink>
          <RouterLink to="detail/5"><li>Joyoung Recruit</li></RouterLink>
          <RouterLink to="detail/6"><li>Tencent DuanWu Festival Gift</li></RouterLink>
          <RouterLink to="detail/7"><li>Tencent Esports Gift Pack</li></RouterLink>
        </ul>
      </div>
    </div>
  </div>
</template>

<style scoped>
.container {
  align-items: start;

  margin: 5rem auto;
  gap: 9rem;
}
.common-big-title {
  letter-spacing: var(--unnamed-character-spacing-0);
  color: var(--unnamed-color-000000);
  text-align: left;
  /* font: normal normal 900 32px/29px var(--unnamed-font-family-source-han-sans-jp), sans-serif; */
  font-size: 1.8rem;
  opacity: 1;
}
.title-box {
  margin-bottom: 1.3rem;
  position: relative;
}
.content-box {
  opacity: 0.7;
  margin-bottom: 2rem;
}
.content-box p {
  margin-bottom: 1rem;
}
.content-footer {
  font-size: 10px;
}
.content-box span {
  opacity: 1;
}
.common-box {
  max-width: 520px;
}
.title-box::before {
  content: '😀'; /* 这里是你想要添加的emoji */
  position: absolute;
  top: 0px;
  left: -35px;
  font-size: 30px;
}
ul li {
  text-decoration: none;
}

ul {
  list-style: none;
  padding: 0;
}

/* 以下、スマホ用のCSS記載 */
@media screen and (max-width: 992px) {
  .container {
    flex-direction: column;
    gap: 0;
    padding-left: 50px;
    margin: 5rem auto;
  }
  .common-box {
    padding: 25px 0 0 0;
  }
}
@media screen and (max-width: 768px) {
  .container {
    padding-left: 20px;
  }
  .common-box {
    padding: 25px 0 0 0;
  }
}
</style>
