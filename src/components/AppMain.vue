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
  <!-- jumbotron -->
  <div class="jumbos"></div>
  <!-- series section -->
  <div class="bg-dark">
    <div
      class="container d-flex justify-content-center flex-wrap gap-5 p-5 pb-3 position-relative"
    >
      <h5 class="mysection">CURRENT SERIES</h5>
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

.jumbos {
  height: 300px;
  background-image: url("../assets/img/jumbotron.jpg");
  background-size: cover;
}

.mysection {
  background-color: $pointed-one;
  padding: 10px;
  color: white;
  position: absolute;
  z-index: 1;
  top: -23px;
  left: 50px;
}

.mybtn {
  background-color: $pointed-one;
  border: none;
  padding: 10px 30px;
  color: white;
}
</style>
