<script>
export default {
  data() {
    return {
      contador: 0
    }
  },
  methods: {
    incrementarContador() {
      this.contador++
    },
    decrementarContador() {
      this.contador--
    }
  },
  mounted() {
    console.log(`O valor inicial do contador é ${this.contador}.`)
  }
}
</script>

<template>
    <!-- Template já apresentada -->
</template>

<style scoped>
/* Estilos já apresentados */
</style>
<script setup>
import { ref, onMounted } from 'vue'

const contador = ref(0)

function incrementarContador() {
  contador.value++
}
function decrementarContador() {
  contador.value--
}

onMounted(() => {
  console.log(`O valor inicial do contador é ${contador.value}.`)
})
</script>


<template>
  <!-- Template já apresentada -->
</template>

<style scoped>
/* Estilos já apresentados */
</style>
