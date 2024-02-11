<template> <!-- EMIT -->

  <Enfant :nom="nom" :prenom="prenom"/>
  <Enfant2 @ajouter="ajouterPersonne"/> <!-- Ici on attend que la valuer soit ajoutée pour être push dans le code. Va être pratique pour push de l'info du child au parent dans le TP final.-->


  <h2>Parent - Liste des personnes</h2>
  <h3 v-for="personne in personnes" :key="personne">
    {{ personne.prenom }} {{  personne.nom }}

  </h3>

</template>


  <script setup> // composiiton API avec le setup. On commit à un ou l'autre pour pas meler d'autres devs.
  import { ref } from 'vue';
  import Enfant from './components/Enfant.vue';
  import Enfant2 from './components/Enfant-2.vue';


  const nom = ref('Doe')
  const prenom = ref('John')

  const personnes = ref([]) // tableau vide ,personne a été ajouté encore.

  const ajouterPersonne = (personne)=>{
    personnes.value.push(personne) // on poush ici le paramètre de la function. Celle ci représente la valeur de l'objet dans la fonction emit de l'enfant.
  }

  </script>
<style scoped>

</style>
