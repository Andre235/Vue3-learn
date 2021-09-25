<template>
  <div @click="dicClick">
    Home组件: {{name}} - {{age}}
  </div>
</template>

<script>
  export default {
    emits: ["pageClick"],
    props: {
      name: {
        type: String,
        default: ""
      },
      age: {
        type: Number,
        default: 18
      }
    },
    methods: {
      dicClick() {
        this.$emit("pageClick", {eventType: "click"})
      }
    }
  }
</script>

<style lang="scss" scoped>

</style>