<template>
  <div id="app">
  <TheHeader />
  <TheMain />
  </div>
</template>

<script>
import TheHeader from "./components/TheHeader.vue";
import TheMain from "./components/TheMain.vue";

export default {
  name: 'App',
  components: {
    TheHeader,
    TheMain,
  }
}
</script>

<style lang="scss">
@import "~bootstrap/scss/bootstrap.scss";
@import "./assets/sass/variables.scss";
#app{
   background-color: $bodyBgColor;
}
</style>
