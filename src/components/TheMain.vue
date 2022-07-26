<template>
<main>
  <div class="container">
    <div class="row justify-content-between" v-show="disks.length <= 10">
    </div>
  </div>
</main>
</template>

<script>
import axios from 'axios';

export default {
  data: function () {
    return {
      disks: [],
    };
  },
  components: {
  },
  methods: {
      },
    mounted() {
      axios
        .get('https://flynn.boolean.careers/exercises/api/array/music')
        .then((result) => { this.disks = result.data.response;})
    }
}
</script>

<style lang="scss">

.col-2 {
  margin: 0 auto;
}
</style>