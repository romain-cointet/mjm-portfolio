<template>
  <div class="page--index">
    <Navbar />
    <Hero
      bgImg="hero.jpg"
      icon="crown.svg"
      title="Salam les khoya"
      text="Product Designer (UI/UX) et ancien développeur web fullstack, mon main skill est d'élaborer des maquettes web et mobiles et de les intégrer tout en supervisant une équipe de développeurs grâce à mon expérience en développement web."
    />
    <Projects />
    <Skills :skills="skills" />
  </div>
</template>

<script>
  export default {
    data() {
      return {
        skills: [
          {
            title: 'Photoshop',
            percent: 0.8,
          },
          {
            title: 'XD',
            percent: 0.5,
          },
          {
            title: 'Figma',
            percent: 0.7,
          },
          {
            title: 'Illustrator',
            percent: 0.3,
          },
        ]
      }
    }
  }
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Libre+Caslon+Text:wght@400;700&display=swap');
  img {
    width: 100%;
  }
  h1, h2, h3, p {
    color: #10262B;
  }
  .divider {
    height: 1px;
    width: 294px;
    border: 1px solid #10262B;
    margin: 64px auto;
  }
</style>
