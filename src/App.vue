<template>
  <div id="app">
    <Header @genreFilter="selectedGenre" @artistFilter="selectedArtist" />
    <RecordsList />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import RecordsList from "./components/RecordsList.vue";

export default {
  name: "App",
  components: {
    Header,
    RecordsList,
  },
  data() {
    return {};
  },
  methods: {
    selectfilter(optionSelected) {
      console.warn(optionSelected);
    },
    selectedGenre() {
      this.genre = this.filterByGenre;
    },
    selectedArtist() {
      this.artist = this.filterByArtist;
    },
  },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  background-color: #1e2d3b;
}
</style>
