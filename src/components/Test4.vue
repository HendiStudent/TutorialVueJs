<script setup>
import { ref } from 'vue'

const titleClass = ref('title')
</script>

<template>
    <h1 :class="titleClass">Make me red</h1>
</template>

<style scoped>
.title {
    color: red;
}
</style>