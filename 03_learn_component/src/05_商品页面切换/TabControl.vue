<template>
  <div class="tab-control">
    <div 
      class="tab-control-item" 
      v-for="(item,index) in title" 
      :key="index" 
      :class="{active: currentIndex === index}"
      @click="itemClick(index)">
      <span>{{item}}</span>
    </div>
  </div>
</template>

<script>
  export default { 
    emits: ["tabClick"],
    props: {
      title: {
        type: Array,
        default() {
          return []
        }
      }
    },
    data() {
      return {
        currentIndex: 0
      }
    },
    methods: {
      itemClick(index) {
        this.currentIndex = index
        this.$emit("tabClick", index)
      }
    },
  }
</script>

<style scoped>

  .tab-control {
    display: flex; /* 弹性布局 */
    
  }

  .tab-control-item {
    flex: 1;  /* 占比为1份 */
    text-align: center;
  }

  .tab-control-item.active {
    color: red;
  }

  .tab-control-item.active span {
    border-bottom: 2px solid red;
    padding: 4px;
  }
</style>