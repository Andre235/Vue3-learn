<template>
  <div>
    <show-names :names="names">
      <template v-slot="slotProps">
        <span>{{slotProps.item}}- {{slotProps.index}}</span>
      </template>
    </show-names>
  </div>
</template>

<script>
  import ShowNames from "./ShowNames.vue"

  export default {
    components: {
      ShowNames
    },
    data() {
      return {
        names: ["A", "B", "C"]
      }
    },
  }
</script>

<style lang="scss" scoped>

</style>