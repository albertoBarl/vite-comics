<script>
export default {
  name: "AppHeader",
  data() {
    return {
      logo: "../src/assets/img/dc-logo.png",
    };
  },
};
</script>
<template lang="">
  <header>
    <div class="logo"><img :src="logo" alt="not available" /></div>
    <nav></nav>
  </header>
</template>
<style lang="sass"></style>
