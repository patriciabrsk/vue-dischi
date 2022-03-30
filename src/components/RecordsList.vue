<template>
  <div class="container justify-content-center m-5">
    <div class="row row-cols-5 g-4 w-80">
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
