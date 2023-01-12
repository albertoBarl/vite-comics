<script scoped>
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
      <div class="col-3">
        <a href="/"><img :src="logo" alt="not available" /></a>
      </div>
      <!-- NAVBAR -->
      <nav class="col-9 pt-3">
        <ul class="d-flex justify-content-between pt-4">
          <li v-for="(element, index) in nav">
            <a href="#">{{ nav[index].label }}</a>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>
<style scoped lang="scss">
@use "../styles/partials/variables" as *;
@use "../styles/partials/mixins" as *;

header {
  height: 125px;
  div {
    height: 100%;
    nav {
      height: 100%;
      ul {
        list-style: none;
        height: 80%;
        li {
          height: 100%;
          &:hover {
            color: $pointed-one;
            border-bottom: 3px solid $pointed-one;
          }
          a {
            @include a-pers;
            color: $dark-color;
            &:hover {
              color: $pointed-one;
            }
          }
        }
      }
    }
  }
}
</style>
