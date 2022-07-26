<template>
<main>
  <div class="container">
    <div class="row" v-show="disks.length <= 10">
    <div class="d-flex flex-wrap">
    <TheList
        v-for="(disk, index) in disks"
        :key="index"
        :disk="disk"/>
    </div>
    </div>
  </div>
</main>
</template>

<script>
import axios from 'axios';
import TheList from './TheList';


export default {
  data: function () {
    return {
      disks: [],
    };
  },
  components: {
    TheList,
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
main{
    padding:70px 0;
}
</style>