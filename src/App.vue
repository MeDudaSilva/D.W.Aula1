<script setup>
import { ref } from 'vue'
const contador = ref(10)

function incrementar() {
    contador.value++
}
function decrementar() {
    if (contador.value > 0) {
        contador.value--
    }
}
function resetar() {
    contador.value = 0
}
const ok = contador.value > 10

</script>
<template>
    <button @click="incrementar">+</button>
    <button @click="decrementar">-</button>
    <button @click="resetar">C</button>
    <p>Valor do contador: {{ contador }}</p>
    <div v-if="ok">Mostrar</div>
</template>
  
<style scoped>
button {
    margin-left: 10px;
    background-color: rgb(202, 12, 155);
    color: aliceblue;
    border: none;
    border-radius: 5px;
    padding: 5px 10px;
    cursor: pointer;
}
</style>