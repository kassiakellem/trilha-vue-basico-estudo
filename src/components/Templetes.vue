<script setup>
import { onMounted, ref } from 'vue';
const inputRefs = ref(null)

onMounted(()=> {
    inputRefs.value.focus()
})

</script>
<template>
    <div>
        <input ref="inputRefs" type="text" />
    </div>
</template>