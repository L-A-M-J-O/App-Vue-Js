<script lang="ts" setup>
  import { ref, onMounted } from 'vue'
  import axios from 'axios'

  interface users {
    gender: string
  }
  const props = defineProps<{
    users: users
  }>()

  const DataAprobada = ref([])
  const value = ref('')
  onMounted(() => {

  })

</script>
<template>
  <el-select v-model="value" class="m-2" placeholder="Select" size="large">
    <el-option
      v-for="item in props.users"
      :key="item.id"
      :label="item.gender"
      :value="item.gender"
    />
  </el-select>
  <div class="row" v-if="value === 'female'">
    <el-select v-model="value" class="m-2" placeholder="Select" size="large">
    </el-select>
  </div>
</template>
