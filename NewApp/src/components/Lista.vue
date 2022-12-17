<style>
  @import '../styles/Lista.css';
</style>
<script setup> 
  let colorAlert = 'Color: Red'
  const styleColor = 'Color: Yellow';
  let subtitulo = 'Soy el componente Lista'
  const arrayColores = ['Blue', 'Green', 'White'];
  const activo = false;
</script>
<template>
  <section id="lista">
    <h2><span>1.</span>{{subtitulo}}</h2>
    <h4 :style="styleColor">Estilo importado</h4>
    <h4 :style="`color:${arrayColores[1]}`">Estilo importado, como un array</h4>
    <p>{{arrayColores}}</p>
    <h4 :style="colorAlert">{{ activo ? 'Estoy activo': 'Estoy desactivado'}}</h4>
  </section>
</template>