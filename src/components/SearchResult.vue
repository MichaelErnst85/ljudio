<template>
  <div>
    <div v-for="(song, index) in getSearchResults" :key="index">
      <SongCard v-bind:song="song" />
    </div>
  </div>
</template>

<script>
import SongCard from "./SongCard";

export default {
  name: "searchresult",

  components: {
    SongCard,
  },

  computed: {
    getSearchResults() {
      return this.$store.state.searchresult;
    },
  },
};
</script>

<style>
body {
  background-image: radial-gradient(rgb(21, 68, 150), rgb(46, 114, 230));
}
</style>
