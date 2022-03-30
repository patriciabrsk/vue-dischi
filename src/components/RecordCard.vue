<template>
  <div id="card">
    <div class="col card h-100">
      <img :src="record.poster" class="m-3" :alt="record.title" />
      <div class="card-body">
        <h5 class="card-title text-white text-uppercase fw-bold">
          {{ record.title }}
        </h5>
        <h6>{{ record.author }}</h6>
        <p>{{ record.year }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "RecordCard",
  props: {
    record: Object,
  },
};
</script>

<style lang="scss" scoped>
div.card {
  background-color: #2d3a46;
  h6,
  p {
    color: #807b6f;
  }
}
</style>
