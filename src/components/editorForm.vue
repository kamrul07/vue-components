<script setup>
 
 const props = defineProps( {
    name : String,
    role : String
 } )
defineEmits(['update:name','update:role']);
  
 
 
</script>

<template>
<input type="text" :value="name" @input="$emit('update:name' , $event.target.value)" >
<input type="text" :value="role"  @input="$emit('update:role' , $event.target.value)" >
<button @click="updateInfo()" >Make change</button>
</template>


<style scoped >
</style>