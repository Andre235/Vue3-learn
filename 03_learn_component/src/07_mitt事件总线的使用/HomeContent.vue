<template>
  <div>
  </div>
</template>

<script>
  import emitter from "./utils/eventbus"

  export default {
    created() {
      // 监听clicekEvent事件
      emitter.on("clicekEvent", (info) => {
        console.log(info);
      })
    }
  }
</script>

<style lang="scss" scoped>

</style>