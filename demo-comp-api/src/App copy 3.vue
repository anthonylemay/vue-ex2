

<template>

  <h1>{{ compteur }} - {{ double }}</h1>
  <button @click="ajouter" >Ajouter</button>

  </template>

  <script setup> //Watchers
  import { ref, watch } from 'vue' // importation de watch

  const compteur = ref(0)
  const double = ref(0)

  const ajouter = ()=>{

  compteur.value++

  }

  watch(compteur, ()=>{ // watch permet de suivre une variable et effectuer du code en parallèle selon ce qui est observé, lorsque modifié. Prend deux params en note; la variable à observer et la fonction à executer.

  double.value = compteur.value * 2

  })
  </script>
<style scoped>

</style>
