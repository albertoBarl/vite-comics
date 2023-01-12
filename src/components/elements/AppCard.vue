<script>
export default {
  props: { dcSeries: Object },
};
</script>
<template lang="">
  <div class="card bg-transparent text-white border-0">
    <img :src="dcSeries.thumb" alt="not available" />
    <p class="mt-2">{{ dcSeries.series }}</p>
  </div>
</template>
<style lang="scss">
div.card {
  width: 150px;
  height: auto;
  cursor: pointer;
}
</style>
