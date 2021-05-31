<template>
  <div>
    {{ age }} ans
  </div>
</template>

<script>
export default {
  props: ['age'],

  watch: {
    age() {
      console.log(this.age);
    }
  }
}
</script>
