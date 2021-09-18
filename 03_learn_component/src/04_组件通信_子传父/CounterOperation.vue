<template>
  <div>
    <button @click="increment">+1</button>
    <button @click="decrement">-1</button>
    <br/>
    <input type="text" v-model.number="number">
    <button @click="incrementN">+n</button>
  </div>
</template>

<script>
  export default {
    // 自定义事件
    emits: ["add", 'sub', 'addN'],
    data() {
      return {
        number: 0
      }
    },
    methods: {
      increment() {
        console.log("+1");
        // 触发自定义的事件
        this.$emit("add")
      },
      decrement() {
        console.log("-1");
        this.$emit("sub")
      },
      incrementN() {
        this.$emit("addN", this.number, "lucas", 24)
      },    
    }
  }
</script>

<style lang="scss" scoped>

</style>