<template>
  <div>
    <h4>计数器:{{counter}}</h4>
    <!-- 监听子组件内部自定义的事件 -->
    <counter-operation 
      @add="addOne" 
      @sub="subOne"
      @addN="addNum"/>



  </div>
</template>

<script>
  import CounterOperation from "./CounterOperation.vue"

  export default {
    components: {
      CounterOperation
    },
    data() {
      return {
        counter: 0
      }
    },
    methods: {
      addOne() {
        this.counter ++
      },
      subOne() {
        this.counter --
      },      
      addNum(number, name, age) {
        this.counter += number
        console.log(name, age);
      }
    }
  }
</script>

<style lang="scss" scoped>

</style>