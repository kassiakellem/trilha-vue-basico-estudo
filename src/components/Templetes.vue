<script setup>
import { onMounted, ref } from 'vue';
const inputRefs = ref(null)

// O hook 'onMounted' 
 //é chamado quando o componente é montado no DOM.
 onMounted(()=> {
     inputRefs.value.focus()
    })
//o valor da referência 'inputRefs' e aplica o foco no campo de input.

</script>
<template>
    <div>
        <input ref="inputRefs" type="text" />
    </div>
</template>