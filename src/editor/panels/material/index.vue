<script setup lang="ts">
import MaterialItem from '@/editor/panels/material/components/MaterialItem.vue'

defineOptions({
  name: 'MaterialPanel',
})
</script>

<template>
  <div class="material-panel flex">
    <div class="nav w-50">
      <div>
        <span><Icon icon="solar:chart-bold" width="18"></Icon></span>
        <span>图表</span>
      </div>
      <div>
        <span><Icon icon="mdi:form-outline" width="18"></Icon></span>
        <span>表单</span>
      </div>
    </div>
    <div class="flex-1 py-15 px-10 overflow-auto">
      <MaterialItem class="mb-15" v-for="i in 20" :key="i"></MaterialItem>
    </div>
  </div>
</template>

<style scoped lang="scss">
.material-panel {
  background: bg-mix(20);
  .nav {
    border-right: 1px solid var(--border-color);
    div {
      cursor: pointer;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      height: 50px;
      font-size: 12px;
      &.active {
        background: bg-mix(60);
      }
    }
  }
}
</style>
