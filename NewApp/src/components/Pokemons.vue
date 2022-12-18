<style>
.container {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  align-items: center;
}
.image {
  margin: 2px;
}
</style>
<script>
import axios from 'axios'

export default {
  name: 'Pokemons',
  data() {
    return {
      characterData: null
    }
  },
  created() {
    this.getPeticion()
  },
  methods: {
    getPeticion () {
      axios.get('https://rickandmortyapi.com/api/character')
        .then((response) => {
          this.characterData = response.data.results;
        })
        .catch((err) => {
          console.log(err)
        })
    }
  },
}
</script>
<template>
  <div>
    <h1>Characters Rick And Morty</h1>
    <div class="container">
      <div v-for="element in characterData" :key='element.id'>
        <h3>{{element.name}}</h3>
        <p>{{element.species, element.gender, element.status}}</p>
        <img class="image" :src='element.image' alt="Imagen de Character"/>
      </div>
    </div>
  </div>
</template>