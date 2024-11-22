<script setup>
import { ref } from 'vue';
const contador = ref(0)
const nome = ref ("vue.js")
const olaVue = ()=> {
    alert (`Olá ${nome.value}`);
}

</script>

<template>
 <button @click="contador++">contador:{{contador}}</button>   
<button @click="olaVue">Olá Vue </button>

</template>