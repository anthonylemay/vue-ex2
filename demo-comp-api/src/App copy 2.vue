<template>

  <h1>{{ compteur }}</h1>

  <button @click="ajouter" >Ajouter</button>

  <p v-for="valeur in valeurs" :key="valeur">
  {{valeur}}
  </p>

</template>

<script setup> // REF + ARRAYS OF OBJECTS
  import { ref } from 'vue'
  
  const compteur = ref(0)
  const valeurs = ref([0])

  const ajouter = ()=>{
    
  compteur.value++
  valeurs.value.push(compteur.value)

  }
</script>

<style scoped>

</style>
