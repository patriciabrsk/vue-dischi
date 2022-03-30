<template>
  <nav class="navbar mb-5">
    <div class="container">
      <a class="navbar-brand" href="#">
        <img
          src="https://www.freepnglogos.com/images/spotify-logo-png-7053.html"
          alt="Spotify logo"
          width="30"
          height="24"
        />
      </a>
    </div>
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
nav,
.container {
  background-color: #2d3a46;
}
</style>
