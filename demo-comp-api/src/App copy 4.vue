<template>

  <h1>{{ compteur }} - {{ nombre }} </h1>
  <button @click="ajouter" >Ajouter</button>

  </template>


  <script setup> // COMPUTED
  import { computed, ref } from 'vue' // doit être importé de vue
  const compteur = ref(0)
  const ajouter = ()=>{
  compteur.value++
  }

  const nombre = computed(()=>{

  return compteur.value % 2 == 0 ? 'Nombre paire' : 'Nombre impaire'
  })
  
  </script>
<style scoped>

</style>
