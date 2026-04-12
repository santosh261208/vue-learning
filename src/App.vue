<!-- Comment
<script setup>
const begruessung = "Hallo ÜK!"
const fach = "Frontend Modul 294"
</script>

<template>
  <h1>{{ begruessung }}</h1>
  <p>Willkommen im {{ fach }}</p>
</template>

<style scoped>
h1 {
  color: green;
}
</style>
-->

<script setup>
import { ref } from 'vue'

const age = ref(0)
const result = ref("")

function decrement() {
  age.value++
}

function check() {
  if (age.value >= 18) {
    result.value = "Volljährig"
  } else {
    result.value = "Minderjährig"
  }
}
</script>

<template>
  <h1>Alter: {{ age }}</h1>
  <button @click="decrement">Inkrementieren</button>

  <button @click="check">Check</button>
  <h1>{{result}}</h1>
</template>
