<template>
  <div class="nav-bar">
    <div class="left">
      <slot name="left"/>
    </div>
    <div class="center">
      <slot name="center"/>
    </div>
    <div class="right">
      <slot name="right"/>
    </div>
  </div>
</template>

<script>
  export default {
    
  }
</script>

<style scoped>
  .nav-bar {
    display: flex;
  }
  
  .nav-bar > div {
    height: 40px;
  }
  
  .left, .right{
    background-color: pink;
    width: 40px;
  }

  .center {
    flex: 1;
    background-color: red;
  }
</style>