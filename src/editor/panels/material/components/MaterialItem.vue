<script setup lang="ts">
defineOptions({
  name: 'MaterialItem',
})
</script>

<template>
  <div class="material-item">
    <div class="title">柱状图</div>
    <div class="icon">
      <Icon icon="flat-color-icons:bar-chart" width="80"></Icon>
    </div>
  </div>
</template>

<style scoped lang="scss">
.material-item {
  cursor: pointer;
  height: 140px;
  padding: 10px;
  display: flex;
  flex-direction: column;
  background: bg-mix(40);
  border: 1px solid var(--border-color);
  border-radius: 4px;
  transition: all 300ms ease;
  &:hover {
    transform: translateY(-3px);
    border: 1px solid #01dbdb;
  }
  .title {
    height: 20px;
    font-size: 12px;
    font-weight: 700;
  }
  .icon {
    flex: 1;
    display: flex;
    justify-content: center;
    align-items: center;
    border: 1px solid var(--border-color);
    border-radius: 4px;
  }
}
</style>
