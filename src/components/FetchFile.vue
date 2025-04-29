<template>
  <h1>Fetch Data</h1>
  <pre>{{ data["forms"][0]["name"] }}</pre>
</template>

<script setup>
import { onMounted, ref } from "vue";

const data = ref(null);

onMounted(() => {
  fetch("https://pokeapi.co/api/v2/pokemon/greninja")
    .then((res) => res.json())
    .then((json) => {
      data.value = json;
    });
});
</script>
