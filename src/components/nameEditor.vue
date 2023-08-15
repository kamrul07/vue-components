<script setup>
 
 defineProps( {
    name : String,
 } )
 defineEmits(['update:modelValue']);
  
</script>

<template>
<input type="text" :value="name" @input="$emit('update:name' , $event.target.value)">
</template>


<style scoped >
</style>