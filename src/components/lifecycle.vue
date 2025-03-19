<script setup>
import { ref, onMounted } from 'vue'

const pElementRef = ref(null)

onMounted(() =>{
    pElementRef.value.textContent = 'hallo hendi'
})
</script>

<template>
    <p ref="pElementRef">kjbkfjdsbkjf</p>
</template>
