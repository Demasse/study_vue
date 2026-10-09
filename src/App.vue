<template>
  <!-- La structure HTML de ton composant -->
  <div>
    <h1>{{ message }}</h1>
    <button @click="incrementer">Compteur : {{ compteur }}</button>
  </div>
</template>

<script setup>
// La logique JavaScript (Vue 3 - Composition API)
import { ref } from 'vue'

const message = ref('Bienvenue dans Vue.js !')
const compteur = ref(0)

function incrementer() {
  compteur.value++
}
</script>

<style scoped>
/* Le style CSS dédié uniquement à ce composant */
h1 {
  color: #42b883;
}
</style>