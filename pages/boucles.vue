<template>
  <div>
    <div v-for="(fruit, index) in fruits" :key="index">
      {{ fruit }}
    </div>
    <div v-for="(identite, i) in identites" :key="i">
      {{ identite.prenom }} {{ identite.nom }}
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      fruits: [
        'poire',
        'pomme',
        'orange',
      ],
      identites: [
        {
          prenom: 'lucie',
          nom: 'dupont'
        },
        {
          prenom: 'jean',
          nom: 'machin'
        },
        {
          prenom: 'edouard',
          nom: 'lacoste'
        }
      ]
    }
  },
}
</script>
