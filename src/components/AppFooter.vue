<script scoped>
export default {
  name: "AppFooter",
  data() {
    return {
      foothead: [
        {
          logo: "/src/assets/img/buy-comics-digital-comics.png",
          label: "digital comics",
        },
        {
          logo: "/src/assets/img/buy-comics-merchandise.png",
          label: "dc merchandise",
        },
        {
          logo: "/src/assets/img/buy-comics-subscriptions.png",
          label: "subscription",
        },
        {
          logo: "/src/assets/img/buy-comics-shop-locator.png",
          label: "comic shop locator",
        },
        {
          logo: "/src/assets/img/buy-dc-power-visa.svg",
          label: "dc power visa",
        },
      ],
      sections: [
        {
          label: "dc comics",
          links: [
            "Characters",
            "Comics",
            "Movies",
            "TV",
            "Games",
            "Videos",
            "News",
          ],
        },
        {
          label: "shop",
          links: ["Shop DC", "Shop DC Collectibles"],
        },
        {
          label: "dc",
          links: [
            "Terms Of Use",
            "Privacy policy (New)",
            "Ad Choices",
            "Advertising",
            "Jobs",
            "Subscriptions",
            "Talent Workshops",
            "CPSC Certificates",
            "Ratings",
            "Shop Help",
            "Contact Us",
          ],
        },
        {
          label: "sites",
          links: [
            "DC",
            "MAD Magazine",
            "DC Kids",
            "DC Universe",
            "DC Power Visa",
          ],
        },
      ],
    };
  },
};
</script>
<template lang="">
  <header>
    <div class="container">
      <div
        class="d-flex justify-content-between pt-3"
        style="width: 100%; height: 100%"
      >
        <div
          v-for="(element, index) in foothead"
          class="d-flex align-items-center"
        >
          <img :src="foothead[index].logo" alt="not available" />
          <span class="ms-2"
            ><a href="/">{{ foothead[index].label }}</a></span
          >
        </div>
      </div>
    </div>
  </header>
  <footer>
    <div class="container text-white">
      <div v-for="(element, index) in sections">
        <h4>{{ sections[index].label }}</h4>
        <ul v-for="(element, index) in sections[index].links">
          <li>{{ element }}</li>
        </ul>
      </div>
    </div>
  </footer>
</template>
<style scoped lang="scss">
@use "../styles/partials/variables" as *;
@use "../styles/partials/mixins" as *;
header {
  background-color: $pointed-one;
  height: 100px;
  img {
    height: 66px;
  }
  span {
    text-transform: uppercase;
    a {
      color: $clear-color;

      @include a-pers;
    }
  }
}
</style>
