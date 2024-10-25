<script setup>
import { ref, watch, watchEffect } from 'vue';

 const frase = ref("");

// Monitoramento usando `watch` (comentado): A função `watch` observa mudanças na `frase`, 
// fornecendo valores antigos e novos para execução de ações específicas.
// Se fosse utilizada, alteraria o título do documento
// cada vez que `frase` fosse modificada.
//  watch(frase,(fraseAntiga, fraseNova) => {
//    document.title = fraseNova;
//  })

// Monitoramento automático com `watchEffect`: Atualiza o título do documento. 
// sempre que o valor de `frase` muda, sem precisar de valores antigos e novos.
watchEffect(() =>{
    document.title = frase.value;
})

</script>
 
<template>
<!-- Campo de entrada que altera `frase` dinamicamente com `v-model`. 
 O título da página muda conforme o valor digitado. -->
<div><input type="text" v-model="frase" /></div>

</template>