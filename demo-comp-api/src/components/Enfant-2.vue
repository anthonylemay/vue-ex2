<template>
  <h3>Dans le composant enfant-2</h3>
  <input v-model="nom" type="text" placeholder="entrez le nom"> <br>
  <input v-model="prenom" type="text" placeholder="entrez le prénom"> <br>
  <button @click="ajouter">Ajouter une personne</button>
  </template>
  
  
<script setup> 
 import { ref } from 'vue';


 const emit = defineEmits(['ajouter']) // permet d'avoir le tableau qui permet d'y ajouter la chaîne des événements
  
  const nom = ref('')
  const prenom = ref('')

  const ajouter = ()=>{

    emit(
      'ajouter', // on créé ici les événements,
      {nom: nom.value, prenom:prenom.value}
    )

  }



</script>


<style scoped>
  


  </style>
  