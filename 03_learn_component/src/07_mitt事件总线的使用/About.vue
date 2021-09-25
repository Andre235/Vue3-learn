<template>
  <div>
    <button @click="click">按钮</button>
  </div>
</template>

<script>
  import emitter from "./utils/eventbus"

  export default {
    methods: {
      click() {
        console.log("click");
        // 通过事件总线发射一个事件
        emitter.emit("clicekEvent", {
          eventName: "clicekEvent",
          username: "lucas"
        })
      }
    }
  }
</script>

<style lang="scss" scoped>

</style>