<script setup>
import { ref } from 'vue'

    defineEmits(['on-change'])

    defineProps({
        modelValue: {
            type: String,
            required: false,
            default: ''
        },
        id: {
            type: String,
            required: true
        },
        type: {
            type: String,
            required: true,
            default: 'text'
        },
        placeholder: {
            type: String,
            required: true,
            default: ''
        },
        label: {
            type: String,
            required: true,
            default: 'Label'
        }
    })
    
    const name = ref('')
</script>

<template> 
<label for="name">{{ label }}</label>
    <input 
    v-model="name" 
    :value="modelValue"
    :id="id"
    :type="type"
    :placeholder="placeholder"
    @input="$emit('on-input', $event.target.value)" >
</template>

<style scoped>

</style>