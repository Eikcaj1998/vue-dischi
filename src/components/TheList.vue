<template>
  <div class="card-wrapper">
    <div class="img">
      <img class="img-fluid" 
      :src="disk.poster" 
      :alt="disk.title" />
    </div>
    <div class="card-text text-center">
      <h5 class="title text-light fw-bold mt-3 fs-6 text-uppercase">{{ disk.title }}</h5>
      <span class="artist fw-bold">{{ disk.author }}</span>
      <span class="year d-block">{{ disk.year }}</span>
    </div>
  </div>
</template>

<script>
export default {
  props: ["disk"],
};
</script>

<style lang="scss">
@import "../assets/sass/variables.scss";
.card-wrapper {
  background-color: $cardBgColor;
  height: 21rem;
  padding: 2rem;
  margin: 10px 20px;
   width: calc(100% / 5 - 40px);
    .artist,
    .year {
        color: $cardTextColor;
    }
}
</style>