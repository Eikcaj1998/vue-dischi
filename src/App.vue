<template>
  <div id="app">
  <TheHeader />
  </div>
</template>

<script>
import TheHeader from "./components/TheHeader.vue";

export default {
  name: 'App',
  components: {
    TheHeader,
  }
}
</script>

<style lang="scss">
@import "~bootstrap/scss/bootstrap.scss";
@import "./assets/sass/variables.scss";
</style>
