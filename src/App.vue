<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import { useStore } from "vuex";

const store = useStore();

</script>
<template>
  <header>
      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
        <RouterLink to="/tareas">Tareas</RouterLink>
      </nav>
      <div>
        <p>Count: {{ store.state.count }}</p>
      </div>
  </header>
  <RouterView />
</template> 