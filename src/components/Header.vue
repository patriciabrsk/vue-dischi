<template>
  <nav class="navbar container-fluid justify-content-between">
    <div class="logo">
      <a href="#">
        <img
          src="../assets/spotify-logo-png-7053.png"
          alt="Spotify logo"
          class="img-fluid"
        />
      </a>
    </div>
    <Selection />
  </nav>
</template>

<script>
import Selection from "./Selection.vue";
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Header",
  components: { Selection },
};
</script>

<style scoped lang="scss">
@import "../assets/scss/style.scss";
nav {
  background-color: #2d3a46;

  img {
    width: 40px;
  }
}
</style>
