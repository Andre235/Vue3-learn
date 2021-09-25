<template>
  <div>
    <template v-for="(item, index) in names" :key="index">
      <!-- 自定义插槽的属性 -->
      <slot :item="item" :index="index"></slot>
    </template>
  </div>
</template>

<script>
  export default {
    props: {
      names: {
        type: Array,
        default: () => []
      }
    }
  }
</script>

<style lang="scss" scoped>

</style>