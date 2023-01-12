<script>
import AppCard from "../components/elements/AppCard.vue";
import series from "../assets/datas/dataSeries.js";

export default {
  name: "AppMain",
  components: {
    AppCard,
    series,
  },
  data() {
    return {
      seriesCard: series,
    };
  },
};
</script>
<template lang="">
  <div class="bg-dark">
    <div
      class="container d-flex justify-content-center flex-wrap gap-5 pt-5 pb-3"
    >
      <AppCard
        v-for="(elem, index) in seriesCard"
        :key="index"
        :dcSeries="elem"
      />
      <button class="mybtn">LOAD MORE</button>
    </div>
  </div>
</template>
<style lang="scss">
@use "../styles/partials/variables" as *;
@use "../styles/partials/mixins" as *;

.mybtn {
  background-color: $pointed-one;
  border: none;
  padding: 10px 30px;
  color: white;
}
</style>
