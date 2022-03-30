<template>
  <div id="app">
    <Header />
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
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  background-color: #1e2d3b;
}
</style>
