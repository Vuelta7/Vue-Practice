<template>
  <h1>{{ num }}</h1>
  <button @click="increment">+</button>
  <button @click="decrement">-</button>
</template>

<script setup>
import { ref } from "vue";

const num = ref(0);

function increment() {
  num.value++;
}

function decrement() {
  num.value--;
}
</script>
