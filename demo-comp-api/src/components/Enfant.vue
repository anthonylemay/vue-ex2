<template>

<h1>Composant enfant : {{ prenom }} {{ nom }}</h1> 
  
  </template>
  
  
<script setup> // composiiton API avec le setup. On commit à un ou l'autre pour pas meler d'autres devs.
  
 const props = defineProps({ // Permet d'aller chercher les values des props transférés du niveau juste au dessus, le parent
    nom: String,
    prenom: String

 })


</script>
<style scoped>
  


  </style>
  