<script setup>

const text = "vue.js 3";
const spanTag = "<span>Codigo Html</span>"

</script>

<template>
    <div> Você está aprendendo {{ text }}</div>
    <div v-html="spanTag"></div>
    <div>{{ text.split('').reverse('').join('') }}</div>
</template>