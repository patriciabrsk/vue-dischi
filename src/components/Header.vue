<template>
  <nav class="navbar mb-5 container-fluid">
    <a href="#">
      <img
        src="../assets/spotify-logo-png-7053.png"
        alt="Spotify logo"
        class="img-fluid"
      />
    </a>
  </nav>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Header",
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
