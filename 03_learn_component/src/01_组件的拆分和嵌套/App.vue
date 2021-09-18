<template>
  <div>
    <Header/>
    <Main/>
    <Footer/>
  </div>
</template>

<script>
  import Header from "./Header"
  import Main from "./Main"
  import Footer from "./Footer"

  export default {
    data() {
      return {
        
      }
    },
    components: {
      Header,
      Main,
      Footer
    }
  }
</script>

<style lang="scss" scoped>

</style>