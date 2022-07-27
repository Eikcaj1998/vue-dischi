<template>
  <header>
  <div class="d-flex justify-content-between mx-1">
    <img src="../assets/img/spotify-logo.png" alt="spotify-logo">
      <SearchGenre  @choosedGenre="filteredSearch"/>
    </div>
  </header>
</template>

<script>
import SearchGenre from './SearchGenre.vue';
export default {
    components:{
        SearchGenre,
    },
}
</script>

<style lang="scss">
@import "../assets/sass/variables.scss";
    header{
        background-color: $headerBgColor ;

        img{
          height: 5.5rem;
          padding: 0.8rem;
        }
    }

</style>