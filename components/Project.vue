<template>
  <b-col cols="4" class="comp--project">
    <b-card
      overlay
      :img-src="loadImg(projectData.img)"
      :img-alt="projectData.title"
      text-variant="white"
      :title="projectData.title"
    ></b-card>
    {{ toto }}
  </b-col>
</template>

<script>
  export default {
    // props: ['projectData'],
    props: {
      projectData: {
        type: Object,
        default: {
          title: 'test',
          img: 'img.jpg'
        },
      },
      toto: {
        type: String,
        required: false,
      }
    },
    methods: {
      loadImg(fileName) {
        console.log(fileName);
        return require('~/assets/' + fileName);
      }
    }
  }
</script>

<style scoped>
  .comp--project {
    padding: 16px;
  }
  .card-title {
    color: #F5EDEB;
   font-family: 'Libre Caslon Text', serif;
   font-size: 52px;
   font-weight: bold;
   letter-spacing: 0;
   line-height: 64px;
   text-align: center;
   text-transform: uppercase;
  }
</style>
