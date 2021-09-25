<template>
  <div>
    <home></home>
    <button @click="pushArray">+name</button>
  </div>
</template>

<script>
  import Home from "./Home.vue"
  
  import { computed } from "vue"

  export default {
    components: {
      Home
    },
    provide() {
      // provide 定义为一个函数，方便this关键字指向当前的vue实例
      // 如果this关键字直接在对象里面定义，则this关键字指向的是当前对象
      return {
        name: "lucas",
        age: 24,
        length: computed(() => this.array.length)
      }
    },
    data() {
      return {
        array: ["abc", "b", "c"]
      }
    },
    methods: {
      pushArray() {
        console.log(this.array);
        this.array.push("lucas")
      }
    },
  }
</script>

<style lang="scss" scoped>  

</style>