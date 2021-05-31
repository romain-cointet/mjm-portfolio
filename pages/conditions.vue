<template>
  <div>
    <p>Salut,
      <span v-if="age > 17">tu es majeure</span>
      <span v-else>tu es mineure</span>
      tu as {{ age }} ans.
    </p>
    <p>
      <span v-if="animal == 'woof'">Chien</span>
      <span v-else-if="animal == 'miaou'">Chat</span>
      <span v-else>animal incconu</span>
    </p>
    <p>
      <span v-if="somme(chiffre1, chiffre2) >= 10">OK</span>
      <span v-else>PAS OK</span>
    </p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      age: 15,
      animal: 'aa',
      chiffre1: 11,
      chiffre2: 2,
    }
  },

  methods: {
    somme(value1, value2) {
      return value1 + value2;
    }
  }
}
</script>
