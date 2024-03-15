<script setup>
import { ref } from 'vue';

const nome = ref('');
const email = ref('');
const senha = ref('');
const confirmacaosenha = ref('');
</script>

<template>
  <input type="text" v-model="nome">
</template>

<style scoped>
</style>
