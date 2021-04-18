<template>
  <Navbar />
</template>

<script>
import Navbar from "@/components/Navbar.vue"
export default {
  name: 'App',
  components: {
    Navbar
  },
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin: 0;
  padding: 0;
  background-color: rgb(245, 241, 241);
  height: 100vh;
}

</style>
