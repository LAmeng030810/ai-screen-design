<script setup lang="ts">
defineOptions({
  name: 'LayerPanel',
})
</script>

<template>
  <div class="h-full">
    <div class="layer-panel h-full overflow-auto">
      <div class="active" v-for="i in 80" :key="i">
        <span>柱状图</span>
        <span><Icon icon="fluent:list-bar-16-filled" width="15"></Icon></span>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
.layer-panel {
  padding: 15px 10px;
  background: bg-mix(50);
  & > div {
    cursor: pointer;
    height: 30px;
    margin-bottom: 4px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 10px;
    border: 1px solid var(--border-color);
    border-radius: 4px;
    background: bg-mix(70);
    font-size: 12px;
    &.active {
      background: #06c6c6;
    }
  }
}
</style>
