<script>
export default {
  name: "AppHeader",
  data() {
    return {
      logo: "/src/assets/img/dc-logo.png",
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
  <header class="container">
    <div class="row d-flex align-items-center my-3">
      <!-- LOGO -->
      <div class="col-3"><img :src="logo" alt="not available" /></div>
      <!-- NAVBAR -->
      <nav class="col-9 pt-3">
        <ul class="d-flex justify-content-between">
          <li v-for="(element, index) in nav">
            <a href="/">{{ nav[index].label }}</a>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>
<style lang="scss">
@use "../styles/partials/variables" as *;
ul {
  list-style: none;
  li a {
    text-transform: uppercase;
    font-size: medium;
    text-decoration: none;
    color: $dark-color;
    &:hover {
      color: $pointed-one;
    }
  }
}
</style>
