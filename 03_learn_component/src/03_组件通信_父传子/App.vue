<template>
  <div>
    <detail title="111" content="111111"></detail>
    <detail :title="appTitile" :content="appContent"></detail>
    <detail v-bind="Obj"></detail>
  </div>
</template>

<script>
  import Detail from "./Detail.vue"

  export default {
    components: {
      Detail
    },
    data() {
      return {
        appTitile: "222",
        appContent: "222222",
        Obj: {
          title: "333",
          content: "333333"
        }
      }
    },
  }
</script>

<style lang="scss" scoped>

</style>