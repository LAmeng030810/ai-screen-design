<script setup lang="ts">
defineOptions({
  name: 'toolbarRight',
})
</script>

<template>
  <div class="toolbar-right flex gap-20 justify-end">
    <span data-tooltip="预览">
      <Icon icon="codicon:open-preview"></Icon>
    </span>
    <span data-tooltip="预览">
      <Icon icon="si:json-fill"></Icon>
    </span>
    <span data-tooltip="json文本">
      <Icon icon="material-symbols:publish-rounded"></Icon>
    </span>
    <span data-tooltip="导入">
      <Icon icon="mdi:import"></Icon>
    </span>
    <span data-tooltip="导出">
      <Icon icon="mdi:export"></Icon>
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
    position: relative;
    display: inline-flex;

    &::after {
      content: attr(data-tooltip);
      position: absolute;
      bottom: -180%;
      left: 50%;
      transform: translateX(-50%);

      background-color: #333;
      color: #fff;
      padding: 4px 8px;
      border-radius: 4px;
      font-size: 12px;
      white-space: nowrap;

      opacity: 0;
      visibility: hidden;
      transition:
        opacity 0.2s ease,
        visibility 0.2s ease;
      z-index: 10;
      pointer-events: none;
    }
    &:hover::after {
      opacity: 1;
      visibility: visible;
    }
  }
}
</style>
