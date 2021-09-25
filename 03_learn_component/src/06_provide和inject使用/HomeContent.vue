<template>
  <div>
    <span>HomeContent: {{name}} - {{age}} - {{length.value}}</span>
  </div>
</template>

<script>
  export default {
    inject: ["name", "age", "length"]
  }
</script>

<style lang="scss" scoped>

</style>