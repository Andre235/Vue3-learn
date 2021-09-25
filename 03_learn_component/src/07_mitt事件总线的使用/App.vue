<template>
  <div>
    <home/>
    <about/>
  </div>
</template>

<script>
  import Home from "./Home.vue"
  import About from "./About.vue"
  

  export default {
    components: {
      Home, About
    },

    data() {
      return {
      }
    },
    methods: {

    },
  }
</script>

<style lang="scss" scoped>  

</style>