<script setup>
import { ref } from 'vue';

// Manipulação de classes e estilos: criando classes dinâmicas. 
const ativa = ref(false);
const erro =ref(true);

const corAtiva= ref("red")
const fontSize= ref(38)

const classAtiva = "ativo";
const classError = "erro";

</script>

<template>
    <!-- <div class="estatico" :class="{ativa? classAtiva:'', classError}"></div> -->
     <div :style="{color:corAtiva, fontSize: fontSize + 'px'}">Vue</div>

</template>

<style>
.estatico {
    width: 100px;
    height: 100px;
    background-color: blue;
}
.ativo {
 background-color: green;
}
.erro {
    background-color: red
}

</style>