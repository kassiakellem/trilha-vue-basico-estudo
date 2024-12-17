<script setup>
import { ref } from 'vue';
const contador = ref(0)
const nome = ref("vue.js")
const olaVue = () => {
    alert(`Olá ${nome.value}`);
}

const botaoDireito= () => {
    alert("clicou com botão direito")
}

const enviarMensagem= () => {
    alert("Mensagem enviada com sucesso!")
}


const textoDoInput= ref("");

const check = ref(false);

const selecionado = ref("");

</script>

<template>
    <div>
        <button @click="contador++">contador:{{ contador }}</button>
        <button @click="olaVue">Olá Vue </button>
         
        </div>
        <div>
       
        <input @keyup.enter="enviarMensagem"/>
        <button @click.right="botaoDireito">Novo</button>
        <input v-model="textoDoInput"> 
       <input type="checkbox" id="checkbox" v-model="check"/>
       <div>{{ check }}</div>
    </div>
    <div>
    <select v-model="selecionado">
        <option disabled value="">Selecione um valor</option>
        <option>A</option>
        <option>B</option>
        <option>C</option>

    </select>
        <br/>
        <div>{{ selecionado }}</div>
    </div>

</template>