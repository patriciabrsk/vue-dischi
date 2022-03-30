<template>
  <div class="container d-flex justify-content-center align-items-center m-5">
    <div class="loading m-5"></div>
  </div>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Loading",
};
</script>

<style scoped>
@import "../assets/scss/style.scss";
.loading {
  border: 16px solid #f3f3f3;
  border-top: 16px solid #2d3a46;
  border-radius: 50%;
  width: 120px;
  height: 120px;
  animation: spin 2s linear infinite;
}

@keyframes spin {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
</style>
