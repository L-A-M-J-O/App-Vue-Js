<style>
  @import '../styles/Lista.css';
</style>
<script>
export default {
  name: 'Lista',
  data () {
    return {
      subtitulo: 'Soy el componente Lista'
    }
  }
}
</script>
<template>
  <section id="lista">
    <h2><span>1.</span>{{subtitulo}}</h2>
  </section>
</template>