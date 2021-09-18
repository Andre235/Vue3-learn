<template>
  <div>
    <tab-control :title="title" @tabClick="tabClick"/>
    <h3>{{content[contentIndex]}}</h3>
  </div>
</template>

<script>
  import TabControl from "./TabControl.vue"

  export default {
    components: {
      TabControl
    },
    data() {
      return {
        title: ["衣服", "鞋子", "帽子"],
        content: ["衣服页面", "鞋子页面", "帽子页面"],
        contentIndex: 0
      }
    },
    methods: {
      tabClick(index) {
        this.contentIndex = index
      }
    }
  }
</script>

<style scoped>

</style>