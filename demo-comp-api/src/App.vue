<template> <!-- PROVIDE -->


<Enfant3/> 

<hr>

<h3>Dans le composant parent</h3>
<button @click="changerNom">Changer le nom</button>
</template>


  <script setup> // composiiton API avec le setup. On commit à un ou l'autre pour pas meler d'autres devs.
  import { ref, provide, computed } from 'vue';
  import Enfant3 from './components/Enfant-3.vue';


  const personne = ref('John Doe') // tableau vide ,personne a été ajouté encore.
  provide('personne', computed(()=>personne.value)) // personne.value permet de donner "personne" à tous les enfants qui la inject.  Mais pour réactivité, mieux vaut fournir `personne` directement, car le .value ne fournit pas la réactivité totale par vue offerte. Seulement le .value

  const changerNom = ()=>{
    personne.value = "Marie Laroche"
    console.log(personne.value)
  }


  </script>
<style scoped>

</style>
