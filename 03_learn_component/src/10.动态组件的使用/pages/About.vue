<template>
  <div>
    <span>About组件</span>
    <button @click="counter++">{{counter}}</button>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        counter: 0
      }
    },
  }
</script>

<style lang="scss" scoped>

</style>