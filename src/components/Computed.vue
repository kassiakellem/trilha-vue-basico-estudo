<script setup>
import { computed, ref } from 'vue';

// Declara uma variável reativa `numeroDelivro` para armazenar o número total de livros. Valor inicial é 10.
const numeroDelivro = ref(10);

// Declara uma variável reativa `numeroDelivroLidos` para armazenar quantos livros já foram lidos. 
const numeroDelivroLidos = ref(5);

// Declara uma variável reativa `metaDeLivroLido` para armazenar a meta de leitura em percentual (0.7 significa 70%).
const metaDeLivroLido = ref(0.7);

// Cria uma propriedade computada `bateuAmeta` que calcula se a meta de leitura foi atingida.
// A expressão compara o percentual de livros lidos com a meta e retorna "Sim" ou "Não" baseado no resultado.
const bateuAmeta = computed(() => {
    return numeroDelivroLidos.value / numeroDelivro.value >= metaDeLivroLido.value
        ? "Sim"
        : "Não";
});
</script>

<template>
    <div>
        <!-- Exibe o valor da propriedade `bateuAmeta`, que pode ser "Sim" ou "Não" -->
        <p>Bateu a meta de livros?</p>
        <p>{{ bateuAmeta }}</p>
    </div>
</template>
