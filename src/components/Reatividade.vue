<script setup>
import { reactive, ref } from 'vue';

const contador = ref(0);

// Função `addContador` que incrementa o valor da variável `contador` cada vez que for chamada.
const addContador = ()=> {
    contador.value++; // Incrementa o valor do contador em 1
}
// Declara um objeto reativo `contadorReactive` usando `reactive`.
// Neste caso, `contadorReactive` é um objeto com uma propriedade `contador`.
const contadorReactive = reactive({contador:0})

</script>

<!-- tudo o que o usuario pode ver -->
<template>
    <!-- Botão que exibe e incrementa o valor do `contador` (reativo simples) ao ser clicado. 
     O clique chama a função `addContador`. -->
<button @click="addContador">Contador: {{ contador }}</button>

 <!-- Botão que exibe e incrementa diretamente o valor do `contadorReactive.contador` ao ser clicado. 
  Usando a reatividade do objeto. -->
<button @click="contadorReactive.contador++">Contador reactive:{{ contadorReactive.contador }}</button>
</template>

