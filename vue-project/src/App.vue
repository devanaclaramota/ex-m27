<script setup >
 import { reactive } from 'vue';
    const estado = reactive({
      n1: 0,
      n2: 0,
      soma: true,
      sub: false,
      mult: false,
      div: false
      
    })
</script>
<template>
  
  <div>

<form>
  <input v-model="n1" placeholder="n1" type="number" >
  <input v-model="n2" placeholder="n2" type="number" >

  <select name="operacao">
    <option value="---">---</option>
    <option value="+">soma</option>
    <option value="-">Subtração</option>
    <option value="*">Multiplicação</option>
    <option value="/">Divisão</option>
  </select>
  
</form>
 
 <p v-if="soma" >{{ (n1) + (n2)}} </p>
 <p v-else-if="sub">{{ (n1) - (n2)}}</p>
 <p v-else-if="mult"> {{ (n1) * (n2)}}</p>
 <p v-else-if= "div">{{ (n1) / (n2)}}</p>
 <p v-else>Selecione uma operação</p>


</div>

</template>