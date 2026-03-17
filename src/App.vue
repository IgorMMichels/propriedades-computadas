<script setup>
import { ref, computed } from 'vue'
const nome = ref('')
const sobrenome = ref('')

const nomeCompleto = computed(() => {
  console.log('Calculando nome completo...')
  return `${nome.value} ${sobrenome.value}`;
})

const nomeCompleto2 = () => {
  console.log('Calculando nome completo...')
  return `${nome.value} ${sobrenome.value}`;
}
</script>

<template>
  <div class="container">
    <input type="text" v-model="nome" />
    <input type="text" v-model="sobrenome" />
    <label>Nome completo: {{ nomeCompleto }}</label>
    <label>Nome completo 2: {{ nomeCompleto2 }}</label>
  </div>
</template>

<style scoped></style>
