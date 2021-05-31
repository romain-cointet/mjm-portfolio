<template>
  <div>
    <input type="text" v-model="email" />
    {{ email }}
  </div>
</template>

<script>
export default {
  data() {
    return {
      email: '',
    }
  }
}
</script>
