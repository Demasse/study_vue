<template>
  <div class="container">
    <h1>Mon Premier Test Vue.js 🚀</h1>

    <!-- Liaison de données avec un input -->
    <input v-model="nom" placeholder="Entre ton nom ici..." />

    <p v-if="nom">Bonjour <strong>{{ nom }}</strong> ! Bienvenue sur Vue.</p>

    <!-- Compteur avec événements -->
    <div class="card">
      <p>Compteur : {{ compteur }}</p>
      <button @click="compteur++">Incrémenter</button>
      <button @click="compteur = 0">Réinitialiser</button>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const nom = ref('')
const compteur = ref(0)
</script>

<style scoped>
.container {
  font-family: Arial, sans-serif;
  max-width: 500px;
  margin: 50px auto;
  text-align: center;
}

input {
  padding: 8px 12px;
  font-size: 16px;
  margin-bottom: 15px;
}

button {
  margin: 5px;
  padding: 8px 15px;
  cursor: pointer;
}

.card {
  margin-top: 20px;
  padding: 15px;
  border: 1px solid #ddd;
  border-radius: 8px;
}
</style>