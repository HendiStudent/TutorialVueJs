<script setup>
import { reactive, ref } from 'vue'

const counter = reactive({count: 0})
const message = ref('Hari ini sangat cerah')
</script>

<template>
  <div>
    <h1>{{ message }}</h1>
    <p>Count is: {{ counter.count }}</p>
  </div>
</template>