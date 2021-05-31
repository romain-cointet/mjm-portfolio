<template>
  <section class="comp--projects">
    <b-container>
      <b-row class="justify-content-center">
        <Project
          v-for="(project, index) in projects"
          :key="index"
          :projectData="project"
        />
      </b-row>
    </b-container>
  </section>
</template>

<script>
  export default {
    data() {
      return {
        toto: 'salut',
        projects: [
          {
            title: 'Talking Heads',
            img: 'projet-0.jpg',
          },
          {
            title: 'Color the church',
            img: 'projet-1.jpg',
          },
          {
            title: 'Blue mymind',
            img: 'projet-2.jpg',
          },
          {
            title: 'Mirror',
            img: 'projet-3.jpg',
          },
          {
            title: 'Couvre feu',
            img: 'projet-4.jpg',
          }
        ]
      }
    },
  }
</script>

<style scoped>
  .comp--projects {
    padding: 64px 0;
  }
</style>
