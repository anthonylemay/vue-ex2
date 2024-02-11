<script setup>
import { RouterLink, RouterView } from 'vue-router'
import { reactive, ref } from 'vue'

// REF AND REACTIVE

let nom = ref('Marie Laroche') // on y va avec un ref quand c'est une seule variable facile.
console.log(nom)

let personne = reactive({ // on y va avec un reactive quand c'est plusieurs variables ensemble.
  nom:'Laroche',
  prenom: 'Marie'
})



function changer(){ // variable statique. ne met pas a jour le dom automatiquement.
  nom.value =  "nouveau nom" //.value permet de changer le nom de la variable de façon réactive.
  console.log(nom) 
}

const modifier=()=>{ // arrow method of calling a function
  personne.prenom = 'Catherine'
}


</script>

<template>
 <h1 @click="changer()">{{ nom }} </h1> <!--Ref-->
  
 <h2 @click="modifier()">{{ personne.prenom }} {{ personne.nom }}</h2> <!--Reactive-->
  <RouterView />
</template>

<style scoped>

</style>
