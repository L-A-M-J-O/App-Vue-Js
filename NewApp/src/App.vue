<script setup>
import HelloWorld from './components/HelloWorld.vue'
// import TheWelcome from './components/TheWelcome.vue'
import Lista from './components/Lista.vue';
import VIf from './components/V-If.vue';
import VOf from './components/V-of.vue';
import Eventos from './components/Eventos.vue';
import Pokemons from './components/Pokemons.vue';
</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
      <HelloWorld msg="You did it!" />
    </div>
  </header>

  <main>
    <Lista/>
    <hr/>
    <VIf/>
    <hr/>
    <VOf/>
    <hr/>
    <Eventos/>
    <!-- <TheWelcome /> -->
  </main>
  <Pokemons/>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
