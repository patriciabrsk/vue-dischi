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
    <div class="selection d-flex justify-content-between">
      <div class="music-genre-select pe-2">
        <select
          class="form-select form-select-sm"
          aria-label=".form-select-sm example"
        >
          <option selected>Open this select menu</option>
          <option value="1">One</option>
          <option value="2">Two</option>
          <option value="3">Three</option>
        </select>
      </div>
      <div class="artist-select">
        <select
          class="form-select form-select-sm"
          aria-label=".form-select-sm example"
        >
          <option selected>Open this select menu</option>
          <option value="1">One</option>
          <option value="2">Two</option>
          <option value="3">Three</option>
        </select>
      </div>
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
nav {
  background-color: #2d3a46;

  img {
    width: 40px;
  }
}
</style>
