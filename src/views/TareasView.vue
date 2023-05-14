<script setup lang="ts">
import { useStore } from "vuex";
import { ref, defineProps, reactive, onMounted } from 'vue';

const store = useStore();
const props = defineProps({
  id: Number,
  descripcion: String,
  completada: Boolean
})
interface LabeledValue {
  id: Number
  file_id: string;
  type_id: string;
  forwarder_id: string;
  port_id: string;
}

const value = ref([])
const address = [
  {
    value: 'file_id',
    label: 'file_id',
  },
  {
    value: 'ForwarderJob_id',
    label: 'ForwarderJob_id',
  }
]
const file = [
  {
    value: 'addres_id',
    label: 'addres_id',
  },
  {
    value: 'type_id',
    label: 'type_id',
  }
]
const ruta = ref<LabeledValue[]>([{ 
    id: 1,
    file_id: '',
    type_id: '',
    forwarder_id: '',
    port_id: '',
}])

const agregarRuta = () => {
  console.log(`agregar`)
  ruta.value.push({
    id: ruta.value.length + 1,
    file_id: '',
    type_id: '',
    forwarder_id: '',
    port_id: '',
  })
  console.log(`agregar`, ruta.value.length + 1)
}
const eliminarRuta = (id: Number) => {  
  console.log(`eliminar`)
  ruta.value = ruta.value.filter(element => element.id !== id);
}
const handleChange = () => {
  console.log(ruta.value)
}
onMounted(() => {
  console.log(ruta.value.length)
})

</script>
<template>
  <section>
    <h1>Tareas</h1>
    <form @submit.prevent="handleChange">
        <button @click="agregarRuta">Agregar tarea</button>
      <div v-for="element in ruta">
        <button @click="eliminarRuta(element.id)">Eliminar</button>
        <el-select v-model="element.file_id" clearable filterable placeholder="Select">
          <el-option
            v-for="item in address"
            :key="item.value"
            :label="item.label"
            :value="item.value"
          />
        </el-select>
        <el-select v-show="!element.type_id" v-model="element.port_id" clearable filterable placeholder="Select">
          <el-option
            v-for="item in file"
            :key="item.value"
            :label="item.label"
            :value="item.value"
          />
        </el-select>
        <el-select v-show="!element.port_id" v-model="element.type_id" clearable filterable placeholder="Select">
          <el-option
            v-for="item in file"
            :key="item.value"
            :label="item.label"
            :value="item.value"
          />
        </el-select>
        <el-select v-model="element.forwarder_id" clearable filterable placeholder="Select">
          <el-option
            v-for="item in file"
            :key="item.value"
            :label="item.label"
            :value="item.value"
          />
        </el-select>
      </div>
      <button type="submit">Save</button>
      <div>
        <button @click="store.state.count++">Increment Count</button>
      </div>
    </form>
  </section>
</template>