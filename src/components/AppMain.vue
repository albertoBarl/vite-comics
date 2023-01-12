<script>
import AppCard from "../components/elements/AppCard.vue";
import Cards from "../assets/datas/dataSeries.js";

export default {
  name: "AppMain",
  components: {
    AppCard,
    Cards,
  },
  data() {
    return {
      seriesCard: Cards,
    };
  },
};
</script>
<template lang="">
  <div class="bg-dark">
    <div class="container d-flex flex-wrap gap-5 p-5">
      <AppCard
        v-for="(elem, index) in seriesCard"
        :key="index"
        :dcSeries="elem"
      />
    </div>
  </div>
</template>
<style lang="scss">
@use "../styles/partials/variables" as *;
@use "../styles/partials/mixins" as *;
</style>
