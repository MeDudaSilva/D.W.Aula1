<script setup>
import{ ref } from `vue`
const contador = ref (10)

function incrementar() {
    contador.value++
}
function decrementar() {
    if(contador.value > 0){
        contador.value--
    }
}
function resetar(){
    contador.value = 0
}
</script>
<template>
    <button @click="incrementar">+</button>
    <button @click="decrementar">-</button>
    <button @click="resetar">C</button>
    <p>Valor do contador: {{ contador }}</p>
  </template>
  
  <style scoped>
  button {
    margin-left: 10px;
    background-color: rgb(22, 86, 214);
    color: aliceblue;
    border: none;
    border-radius: 5px;
    padding: 5px 10px;
    cursor: pointer;
  }
  </style>