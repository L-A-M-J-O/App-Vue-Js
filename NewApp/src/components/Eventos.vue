<script setup>;
import {ref} from'vue';
  const numeros = ref([]);
  const verde = 'Color: green';
  const rojo = 'Color: red'
  let cambio = ref(0);
  const increment = () => {
    cambio.value ++;
    console.log(cambio.value)
  }
  const desincrement = () => {
    cambio.value --;
    console.log(cambio.value)
  }
  const reset = () => {
    cambio.value = 0;
  }
  const agregar = () => {
    numeros.value.push(cambio.value)
  }

</script>
<template>
  <h1 v-if="cambio <= 0" :style="rojo">{{cambio}}</h1>
  <h1 v-else :style="verde">{{cambio}}</h1>
  <button @click="increment">Aumentar</button>
  <button @click="desincrement">Descrementar</button>
  <button @click="reset">Reset</button>
  <button @click="agregar">Agregar</button>
  <ul>
    <li v-for="numero in numeros">Has Agregado {{numero}}</li>
  </ul>
</template>