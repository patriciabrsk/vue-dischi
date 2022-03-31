<template>
  <div class="container d-flex justify-content-center h-100 py-5">
    <Loading v-if="recordsList <= 0" />
    <div class="row row-cols-5 g-4 mx-5">
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
import Loading from "./Loading.vue";
import axios from "axios";

export default {
  name: "RecordsList",
  components: { RecordCard, Loading },
  data() {
    return {
      recordsList: [],
    };
    // props: {},
  },
  created() {
    setTimeout(() => {
      axios
        .get("https://flynn.boolean.careers/exercises/api/array/music")
        .then((response) => {
          this.recordsList = response.data.response;
        });
    }, 4000);
  },

  //   computed: {
  //     filteredRecordsList() {
  //       return this.recordsList.filter((record) => {
  //       });
  //     },
  //   },
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/style.scss";
div.records-container {
}
</style>
