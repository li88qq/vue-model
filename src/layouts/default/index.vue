<template>
  <div>
    <a-button type="primary" @click="test1">测试1</a-button>
  </div>
  <MyDrawer @register="register1"></MyDrawer>
</template>
<script setup lang="ts">
import {ref, reactive, defineAsyncComponent} from 'vue'
const MyDrawer = defineAsyncComponent(()=>import('./MyDrawer.vue'))

import {useDrawer} from '@/components/drawer'

const [register1,{open:open1}] = useDrawer()

const test1 = ()=>{
  open1()
}



</script>