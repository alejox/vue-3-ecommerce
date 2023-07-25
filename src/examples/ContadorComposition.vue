<script setup lang="ts">
import { ref, onMounted } from "vue";

const count = ref(0);

function increment() {
  count.value++;
}

function decrement() {
  count.value -= 1
}

onMounted(() => {
  console.log(`El valor inicial de contador es ${count.value}`);
});
</script>

<template>
  <h1>Hola soy la versión de Composition API</h1>
  <h1>Contador: {{ count }}</h1>
  <button @click="decrement">Decrementar contador</button>
  <button @click="increment">Incrementar contador</button>
</template>

<style scoped></style>
