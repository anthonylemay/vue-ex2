<template>
  <h3>Dans le composant enfant-3: {{ personne }}</h3>

  </template>
  
  
<script setup> 
import { inject } from 'vue';
const personne = inject('personne') // permet d'aller chercher les values du provide au niveau du parent. 


</script>


<style scoped>
  


  </style>
  