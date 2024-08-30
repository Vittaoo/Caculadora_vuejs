<script setup>

import { reactive } from "vue";


import Operacao from "./components/Operacao.vue";
import Resultado from './components/Result.vue';
import Cabecalho from "./components/Cabecalho.vue";

const estado = reactive({
  operacao: '+',
  numero_1: 0,
  numero_2: 0,

})

const resultado = () => {
  const { operacao } = estado
  let resultado

  switch (operacao) {
    case '*':
      return  parseFloat(estado.numero_1) * parseFloat(estado.numero_2)
    case '-':
      return  parseFloat(estado.numero_1) - parseFloat(estado.numero_2)
    case '/':
      return  parseFloat(estado.numero_1) / parseFloat(estado.numero_2)
    default:
      return  parseFloat(estado.numero_1) + parseFloat(estado.numero_2)
  }
    

}



</script>

<template>

  
    <div class="container">
      <Cabecalho/>
      <Operacao :operacao="e => estado.operacao = e.target.value" :num_1="e => estado.numero_1 = e.target.value" :num_2="e => estado.numero_2 = e.target.value" />
      <Resultado :resultado="resultado()" :num1="estado.numero_1"  :num2="estado.numero_2"/>
  
    </div>
  



</template>

<style scoped></style>
