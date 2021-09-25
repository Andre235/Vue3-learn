<template>
  <div>
    <button v-for="item in tabs" 
            :key="item"
            @click="btnClick(item)"
            :class="{active: currentName === item, inactive: currentName !== item}">
      {{item}}
    </button>

    <!-- 动态组件实现切换组件案例 -->
    <keep-alive>
      <component 
        :is="currentName" 
        name="lucas"
        :age="18"
        @pageClick="pageClick"
      />    
    </keep-alive>
  </div>
</template>

<script>
  import Home from "./pages/Home.vue"
  import About from "./pages/About.vue"
  import Category from "./pages/Category.vue"

  export default {
    components: {
      Home, About, Category
    },
    data () {
      return {
        tabs: ["Home", "About", "Category"],
        currentName: "Home"
      }
    },
    methods: {
      btnClick(item) {
        this.currentName = item
      },
      pageClick(data) {
        console.log("Home组件内部发生了点击，参数为：", data);
      }
    }
  }
</script>

<style scoped>
  .active {
    color: red
  }
  .inactive {
    color: grey;
    font-style: italic;
  }
</style>