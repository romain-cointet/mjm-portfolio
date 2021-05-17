<template>
  <section class="comp--hero">
    <b-container fluid>
      <b-row class="align-items-center">
        <b-col cols="6">
          <img :src="loadImg(bgImg)" alt="" class="bg-img"/>
        </b-col>
        <b-col cols="6" class="text-wrapper">
          <img :src="loadImg(icon)" alt="" />
          <p class="title">{{ title }}</p>
          <div class="divider"></div>
          <h1>{{ text }}</h1>
        </b-col>
      </b-row>
    </b-container>
  </section>
</template>

<script>
  export default {
    props: ["bgImg", "icon", "title", "text"],

    methods: {
      loadImg(fileName) {
        return require('~/assets/' + fileName);
      }
    }
  }
</script>

<style scoped>
.text-wrapper {
  text-align: center;
  filter: blur(5px);
  animation: 2s showTexts forwards;
}
.bg-img {
  opacity: 0;
  transform: translateX(-20%);
  transform-origin: left;
  animation: 2s showImg forwards;
}
@keyframes showTexts {
  100% {
    filter: blur(0px);
  }
}
@keyframes showImg {
  100% {
    opacity: 1;
    transform: translateX(0);
  }
}
.text-wrapper img {
  width: 97px;
}
.text-wrapper .title {
  font-family: 'Libre Caslon Text', serif;
  font-weight: 700;
  font-size: 52px;
  letter-spacing: 0;
  line-height: 64px;
  text-align: center;
}
.text-wrapper h1 {
  font-family: 'Libre Caslon Text', serif;
  font-size: 18px;
  letter-spacing: 0;
  line-height: 22px;
  text-align: center;
}


</style>
