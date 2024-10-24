<script setup>
import { ref } from 'vue';

const contador = ref(0);

</script>

<!-- tudo o que o usuario pode ver -->
<template>
<button @click="contador++">"Você clicou {{ contador }} vezes"</button>

</template>

<style>


</style>