<script setup>
import { reactive, ref } from 'vue';
const mensagemEscopoPai = "vue trilha"
const items = ref([{msg:"Vue.js"}, {msg: "listas"}])
const dados = reactive({
    titulo: "Como renderizar listas no Vue.",
    autor: "Evan You",
    publicado: "2024-11-21"
})


</script>
<template>
   <ul>
    <li v-for="(item, index) in items">
        {{ mensagemEscopoPai}} - {{index}} - {{item.msg }}</li>
   </ul>
   <ul>
    <li v-for="valor in dados">
        {{ valor}}</li>
   </ul>
   <span v-for="n in 10">{{ n }}</span>
</template>