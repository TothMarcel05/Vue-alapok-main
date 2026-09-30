<script setup>
import { ref } from 'vue'
    defineEmits(['on-change'])
    
    const name = ref('')
</script>

<template> 
    <input 
    v-model="name" 
    type="text"
    placeholder="Enter your name"
    @change="$emit('on-change', name)" >
</template>

<style scoped>

</style>