<script setup lang="ts">
  import { ref, onMounted } from 'vue';
  import axios from 'axios'
  import EntitiesForwarder from '@/components/EntitiesForwarder.vue';
  import EntitiesForwarderOne from '@/components/EntitiesForwarderOne.vue';
  import VoyageMaritime from '@/components/VoyageMaritime.vue';

  const users = ref([]);
  const userAprobado = ref([])

  const getUsers = (() => {
    axios.get('https://randomuser.me/api/')
        .then(response => {
          users.value = response.data.results
          console.log(users.value )
        })
        .catch((error) => console.log(error))
  })
  onMounted(() => {
    getUsers();
  })

</script>
<template>
  <div class="container">
    <div class="row">
      <h5>Vista de Formulario</h5>
      <EntitiesForwarder v-bind:users="users"/>
      <VoyageMaritime />
    </div>
  </div>
</template>

