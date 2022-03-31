<template>
  <div id="app">
    <Header />
    <Loading />
    <RecordsList />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
// import Loading from "./components/Loading.vue";
import RecordsList from "./components/RecordsList.vue";

export default {
  name: "App",
  components: {
    Header,
    // Loading,
    RecordsList,
  },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  background-color: #1e2d3b;
  height: 100%;
}
</style>
