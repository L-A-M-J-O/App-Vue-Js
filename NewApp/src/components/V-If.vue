<style>
  @import '../styles/V-If.css';
</style>
<script setup>
  const onlineColor = 'Background-color: Green'
  const DisColor = 'Background-color: Red'
  const dontColor = 'Background-color: Yellow'
  const activo = true;
  const subtitulo = 'Soy el componente V-IF'
</script>
<template>
  <div id="v-if">
    <h2><span>2.</span>{{subtitulo}}</h2>
    <h1 v-if="activo"><i>Modo ! </i> Estoy activo</h1>
    <h1 v-if="!activo"><i>Modo ! </i> Estoy desactivado</h1>
    <h1 v-if="activo"><i>Modo else </i>Estoy activo</h1>
    <h1 v-if="!activo"><i>Modo else </i> Estoy desactivado</h1>

    <div class="container"> 
      <h2 v-if="activo === true">
        <div class="circule" :style="onlineColor"></div>
        <p>Online</p>
      </h2>
      <h2 v-else-if="activo === false">
        <div class="circule" :style="DisColor"></div>
        <p>Disconnected</p>
      </h2>
      <h2 v-else>
        <div class="circule" :style="dontColor"></div>
        <p>I don't know</p>
      </h2>
    </div>

    <h2 v-show="activo">Hola Alan Naranjo</h2>
  </div>
</template>