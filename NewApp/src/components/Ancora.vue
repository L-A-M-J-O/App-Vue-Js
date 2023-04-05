<script setup lang="ts">
  import {ref} from 'vue';
  import axiso from 'axios';

</script>
<template>
  <div class="container">
    <div class="row">
      <div class="col-2">
        <label for="name">Entities</label>
      </div>
      <select name="select">
        <option>Valencia</option>
        <option>Madrid</option>
        <option>Sevilla</option>
      </select>
      <div class="col-2">
        <label for="name">Address</label>
      </div>
      <select name="select">
        <option>V1111</option>
        <option>M2222</option>
        <option>S3333</option>
      </select>
    </div>
  </div>
</template>