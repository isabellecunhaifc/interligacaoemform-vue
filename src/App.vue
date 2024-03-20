<script setup>
import { ref } from 'vue';

const nome = ref('');
const email = ref('');
const idade = ref('');
let nomeinf = [];
let emailinf = [];
let idadeinf = [];
function enviar() {
 nomeinf.push(nome.value)
 emailinf.push(email.value)
 idadeinf.push(idade.value)
 alert(`Confirmado!\n Nome: ${nomeinf}\n Email: ${emailinf}\n Idade: ${idadeinf}`)
}
</script>

<template>
  <div class="teste">
   <p>Nome digitado é:  {{ nome }} </p>
  <input type="text" v-model="nome">
  <p>Email digitado é: {{ email }}</p>
  <input type="email" v-model="email">
  <p>Idade digitada é: {{ idade }}</p>
  <input type="number" v-model="idade">
  <br>
  <button id="enviar" @click="enviar"> Enviar</button>
</div>
</template>

<style scoped>
#enviar{
  width: 60px;
  height: 20px;
  border-radius: 5px;
  border: 2px solid black;
  background-color: rgb(245, 185, 196);
  letter-spacing: 1px;
}

.teste{
  background-color: rgb(187, 36, 61);
  color: white;
  border-radius: 5px;
  width: 250px;
  height: 180px;
  text-align: center;
  box-shadow: 10px 5px 5px rgb(73, 71, 71);
  margin-left: 450px;
  margin-bottom: 120px;
}
</style>
