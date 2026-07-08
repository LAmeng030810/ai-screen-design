<script setup lang="ts">
import { Icon } from '@iconify/vue'
import { useEditorStore } from '@/stores/editor.ts'

defineOptions({
  name: 'toolbarLeft',
})

const { panelVisible } = useEditorStore()
</script>

<template>
  <div class="toolbar-right flex gap-20">
    <span
      :class="{ active: panelVisible.material }"
      @click="panelVisible.material = !panelVisible.material"
      title="物料面板"
    >
      <Icon icon="fluent:panel-left-28-filled"></Icon>
    </span>
    <span
      :class="{ active: panelVisible.property }"
      @click="panelVisible.property = !panelVisible.property"
      title="属性面板"
    >
      <Icon icon="fluent:panel-right-28-filled"></Icon>
    </span>
    <span
      :class="{ active: panelVisible.layer }"
      @click="panelVisible.layer = !panelVisible.layer"
      title="图层面板"
    >
      <Icon icon="fluent:layer-20-filled"></Icon>
    </span>
    <span title="后退">
      <Icon icon="material-symbols:undo-rounded"></Icon>
    </span>
    <span title="前进">
      <Icon icon="material-symbols:redo-rounded"></Icon>
    </span>
  </div>
</template>

<style scoped lang="scss">
.toolbar-right {
  span {
    padding: 4px;
    border: 1px solid #495b79;
    border-radius: 4px;
    cursor: pointer;

    &.active {
      background-color: #3e60a9;
    }
  }
}
</style>
