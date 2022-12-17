<script setup>
 const handleClick = () => {
  this.cambio = !this.cambio;
 }
</script>
<template>
  <p v-show='handleClick'>{{cambio ? 'Autorizado' : 'No Autorizado'}}</p>
  <button v-on:click="handleClick">Click On</button>
  <button @click="handleClick">Click @</button>
</template>