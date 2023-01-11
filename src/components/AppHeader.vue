<script>
export default {
  name: "AppHeader",
  data() {
    return {
      logo: "src/assets/img/dc-logo.png",
      nav: [
        {
          label: "Characters",
          status: "not-active",
        },
        {
          label: "Comics",
          status: "not-active",
        },
        {
          label: "Movies",
          status: "not-active",
        },
        {
          label: "Tv",
          status: "not-active",
        },
        {
          label: "Games",
          status: "not-active",
        },
        {
          label: "Collectibles",
          status: "not-active",
        },
        {
          label: "Videos",
          status: "not-active",
        },
        {
          label: "Fans",
          status: "not-active",
        },
        {
          label: "News",
          status: "not-active",
        },
        {
          label: "Shop",
          status: "not-active",
        },
      ],
    };
  },
};
</script>
<template lang="">
  <header>
    <div class="logo"><img :src="logo" alt="not available" /></div>
    <nav>
      <ul>
        <li v-for="(element, index) in nav">
          <a href="/">{{ nav[index].label }}</a>
        </li>
      </ul>
    </nav>
  </header>
</template>
<style lang="scss">
ul {
  list-style-type: none;
}
</style>
