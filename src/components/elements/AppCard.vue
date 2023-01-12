<script>
export default {
  props: { dcSeries: Object },
};
</script>
<template lang="">
  <div class="card">
    <img :src="dcSeries.thumb" alt="not available" />
    <span>{{ dcSeries.series }}</span>
  </div>
</template>
<style lang="scss">
div.card {
  width: 150px;
  height: auto;
}
</style>
