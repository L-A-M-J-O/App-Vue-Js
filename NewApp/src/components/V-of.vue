<script setup>
  const subtitulo = 'Soy el componente V-OF'
  const frutas = ['Manzana', 'Banano', 'Pera', 'Mora', 'Mango'];
  const animales = [ 
      {
        name: 'Perro',
        price: '20$',
        race: 'Labrador',
        stock: 3
      }, 
      {
        name: 'Gato',
        price: 'Free$',
        race: 'Español',
        stock: 12
      }, 
      {
        name: 'Leon',
        price: '10.000$',
        race: 'Salvaje',
        stock: 354
      },
      {
        name: 'Buoh',
        price: '5.000$',
        race: 'Natural',
        stock: 20
      }
    ]
  const objeto = {
    name: 'Alan',
    lastname: 'Naranjo',
    coment: 'Me gusta ser proactivo y vas hacer el mejor',
  }
</script>
<template>
  <div id="v-of">
    <h2><span>3.</span>{{subtitulo}}</h2>
    <u>
      <li v-for="(fruta, index) in frutas" :key="index"> {{fruta}}</li>
    </u>
    <ul>
      <li v-for="animal in animales" :key="animal.name">
        <h1>{{animal.name}}</h1>
        <span>{{animal.price}}</span>
        <p>{{animal.race}}</p>
      </li>
    </ul>
    <p v-for="(value, element) in objeto">{{value}} : {{element}} </p>
  </div>
</template>