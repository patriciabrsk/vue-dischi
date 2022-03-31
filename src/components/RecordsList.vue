<template>
  <div class="container d-flex justify-content-center text-center pb-5">
    <!-- <Loading v-if="recordsList <= 0" /> -->
    <div class="row row-cols-5 g-4">
      <RecordCard
        v-for="(record, index) in recordsList"
        :key="index"
        :record="record"
      />
    </div>
  </div>
</template>

<script>
import RecordCard from "./RecordCard.vue";
import axios from "axios";

export default {
  name: "RecordsList",
  components: { RecordCard },
  data() {
    return {
      recordsList: [],
    };
  },
  created() {
    // setTimeout(() => {
    axios
      .get("https://flynn.boolean.careers/exercises/api/array/music")
      .then((response) => {
        this.recordsList = response.data.response;
      });
    // }, 4000);
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/style.scss";

div.row {
  width: 70vw;
}
</style>
