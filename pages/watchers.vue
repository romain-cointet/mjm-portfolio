<template>
  <div>
    <Age :age="age" />
    <button @click="addAge">Clic</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      age: 17,
    }
  },
  //
  // mounted() {
  //   this.age = 18;
  // },

  methods: {
    addAge() {
      return this.age++;
    }
  }
}
</script>
