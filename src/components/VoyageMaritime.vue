<template>
  <div>
    <label @click="opcion1 = !opcion1">
      <img
        v-if="opcion1"
        src="..//../public/assets/img/crucero (1).png"
        alt="Checkbox Seleccionado"
      />
      <img
        v-else
        src="..//../public/assets/img/crucero.png"
        alt="Checkbox Deseleccionado"
      />
    </label>
    <label @click="opcion2 = !opcion2">
      <img
        v-if="opcion2"
        src="..//../public/assets/img/crucero (1).png"
        alt="Checkbox Seleccionado"
      />
      <img
        v-else
        src="..//../public/assets/img/crucero.png"
        alt="Checkbox Deseleccionado"
      />
    </label>
    <label @click="opcion3 = !opcion3">
      <img
        v-if="opcion3"
        src="..//../public/assets/img/crucero (1).png"
        alt="Checkbox Seleccionado"
      />
      <img
        v-else
        src="..//../public/assets/img/crucero.png"
        alt="Checkbox Deseleccionado"
      />
    </label>
    <div v-if="opcion1">
      <h1>1</h1>
      <el-select v-model="select1" clearable filterable placeholder="Select">
        <el-option
          v-for="item in selectVoyage.options"
          :key="item.base"
          :label="item.updated"
          :value="item.base"
        />
      </el-select>
    </div>

    <div v-if="opcion2">
      <h1>2</h1>
      <el-select v-model="select2" clearable filterable placeholder="Select">
        <el-option
          v-for="item in selectVoyage.options"
          :key="item.base"
          :label="item.updated"
          :value="item.base"
        />
      </el-select>
    </div>

    <div v-if="opcion3">
      <h1>3</h1>
      <el-select v-model="select3" clearable filterable placeholder="Select">
        <el-option
          v-for="item in selectVoyage.options"
          :key="item.base"
          :label="item.updated"
          :value="item.base"
        />
      </el-select>
    </div>
    <!-- <button @click="simulacionDeEntrada">Simulacion</button> -->
  </div>
</template>

<script setup lang="ts">
import { onMounted, ref } from "vue";
const opcion1 = ref(true);
const opcion2 = ref(false);
const opcion3 = ref(false);
const select1 = ref();
const select2 = ref();
const select3 = ref();
onMounted(() => {
  if (datosVoyaga.value) {
    selectVoyage.value.options.push(datosVoyaga.value);
    select1.value = selectVoyage.value.options[0];
  }
});
const datosVoyaga = ref({
  base: "USD",
  result: {
    EUR: 0.93354,
  },
  updated: "202:58",
  ms: 2,
});
const value = ref();
const selectVoyage = ref({
  list: [],
  options: [
    {
      base: "USD",
      result: {
        EUR: 0.93354,
      },
      updated: "2023-05-29 22:29:58",
      ms: 2,
    },
    {
      base: "USD",
      result: {
        EUR: 0.93354,
      },
      updated: "2023-05-29 22:29:58",
      ms: 2,
    },
    {
      base: "USD",
      result: {
        EUR: 0.93354,
      },
      updated: "2023-05-29 22:29:58",
      ms: 2,
    },
    {
      base: "USD",
      result: {
        EUR: 0.93354,
      },
      updated: "2023-05-29 22:29:58",
      ms: 2,
    },
    {
      base: "USD",
      result: {
        EUR: 0.93354,
      },
      updated: "2023-05-29 22:29:58",
      ms: 2,
    },
    {
      base: "USD",
      result: {
        EUR: 0.93354,
      },
      updated: "2023-05-29 22:29:58",
      ms: 2,
    },
    {
      base: "USD",
      result: {
        EUR: 0.93354,
      },
      updated: "2023-05-29 22:29:58",
      ms: 2,
    },
    {
      base: "USD",
      result: {
        EUR: 0.93354,
      },
      updated: "2023-05-29 22:29:58",
      ms: 2,
    },
    {
      base: "USD",
      result: {
        EUR: 0.93354,
      },
      updated: "2023-05-29 22:29:58",
      ms: 2,
    },
    {
      base: "USD",
      result: {
        EUR: 0.93354,
      },
      updated: "2023-05-29 22:29:58",
      ms: 2,
    },
  ],
});
</script>
<style>
img {
  width: 40px;
  height: 40px;
}
</style>
