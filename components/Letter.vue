<template>
  <div class="comp--letter">
    <div
      v-for="(letter, i) in arrayLetters"
      :key="i"
      class="letter"
      :style="stylePosition">
      {{ letter }}
    </div>
  </div>
</template>

<script>
// https://tympanus.net/codrops/2021/03/24/distributed-letters-animation-layout/
// https://stackoverflow.com/questions/46551925/vuejs-v-bindstyle-hover
export default {
  props: ['word'],

  data() {
    return {
      arrayLetters: Array,
    }
  },

  mounted() {
    console.log('mounted');
    let letters = document.getElementByClassName('letter');
    console.log('letters', letters);
    for(let i = 0; i < letters.length; i++) {
      console.log('test');
      console.log(letter[i].getBoundingClientRect());
    }
  },

  computed: {
    stylePosition() {
      return {
        '--positionX' : 0 + 'px',
        '--positionXHover' : this.randomNumber(-100, 300) + 'px',
        '--positionY' : 0 + 'px',
        '--positionYHover' : this.randomNumber(-100, 300) + 'px',
      }
    }
  },

  mounted() {
    this.arrayLetters = this.word.split('');
    console.log(this.arrayLetters);
  },

  methods: {
    randomNumber(min, max) { // min and max included
      return Math.floor(Math.random() * (max - min + 1) + min);
    }
  }
}
</script>

<style>
  body {
    background: gray,
  }
  .comp--letter {
    width: 300px;
    height: 500px;
    background: #10262B;
    position: relative;
  }

  .letter {
    color:red;
    font-size: 42px;
    position: absolute;
    top: var(--positionX);
    left: var(--positionY);
    opacity: 0;
    transition: 0.3s all ease-out;
  }
  .comp--letter:hover .letter {
    top: var(--positionXHover) !important;
    left: var(--positionYHover) !important;
    opacity: 1;
  }
</style>
