<template>
  <div class="selection d-flex justify-content-between">
    <div class="music-genre-select pe-2">
      <select
        v-model="filterByGenre"
        class="form-select form-select-sm"
        aria-label=".form-select-sm example"
      >
        <option value="" @click="$emit('genreFilter', filterByGenre)">
          Select music genre
        </option>
        <option
          v-for="genre in genres"
          :value="genre"
          :key="genre"
          @click="$emit('genreFilter', filterByGenre)"
        >
          {{ genre }}
        </option>
      </select>
    </div>
    <div class="artist-select">
      <select
        v-model="filterByArtist"
        class="form-select form-select-sm"
        aria-label=".form-select-sm example"
      >
        <option value="" @click="$emit('artistFilter', filterByArtist)">
          Select artist name
        </option>
        <option
          v-for="artist in artists"
          :value="artist"
          :key="artist"
          @click="$emit('artistFilter', filterByArtist)"
        >
          {{ artist }}
        </option>
      </select>
    </div>
  </div>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Selection",
  data() {
    return {
      filterByGenre: "",
      filterByArtist: "",
    };
  },
  props: {
    genres: Array,
    artists: Array,
  },
};
</script>

<style></style>
