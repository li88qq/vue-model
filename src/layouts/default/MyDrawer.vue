<template>
  <BasicDrawer @register="register" v-bind="drawerRt">
    <template #extra>
      <a-space>
        <a-button type="primary">保存</a-button>
        <a-button @click="close">取消</a-button>
      </a-space>
    </template>
  </BasicDrawer>
</template>
<script setup lang="ts">
import {ref,reactive} from 'vue'
import {BasicDrawer,useDrawer,DrawerProps} from '@/components/drawer'

const [register,{close}] = useDrawer()

const drawerRt = reactive<DrawerProps>({
  title:'测试',
  closable:false,
})
</script>