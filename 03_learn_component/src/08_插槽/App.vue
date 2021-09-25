<template>
  <div>
    <nav-bar>
      <template #left>
        <button>左边按钮</button>
      </template>
      <template #center>
        <span>中间title</span>
      </template>      
      <template #right>
        <i>i标签</i>
      </template>      
    </nav-bar>
  </div>
</template>

<script>
  import MySlot from "./MySlot.vue"
  import NavBar from "./NavBar.vue"

  export default {
    components: {
      MySlot, NavBar
    }
  }
</script>

<style lang="scss" scoped>

</style>