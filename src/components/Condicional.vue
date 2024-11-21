<script setup>
import { ref } from 'vue';
const maravilhoso = ref(false);

const letra = ref("X");
const mostra = ref(true);

</script>

<template>
<div>
    <h1 v-if="maravilhoso">maravilhoso é o vue.</h1>
    <h1 v-else>Não é vue</h1>

<div v-if="letra === 'A'">A</div>   
<div v-else-if="letra === 'B'">B</div>
<div v-else-if="letra === 'C'">C</div>
<div v-else>Não é o ABC</div>

<div v-show="mostra">V-show</div>

</div>

</template>

