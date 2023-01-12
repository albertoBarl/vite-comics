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
      socials: [
        {
          name: "Facebook",
          logo: "footer-facebook.png",
        },
        {
          name: "Twitter",
          logo: "footer-twitter.png",
        },
        {
          name: "YouTube",
          logo: "footer-youtube.png",
        },
        {
          name: "Pinterest",
          logo: "footer-pinterest.png",
        },
        {
          name: "Periscope",
          logo: "footer-periscope.png",
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
            ><a href="#">{{ foothead[index].label }}</a></span
          >
        </div>
      </div>
    </div>
  </header>
  <footer class="d-flex justify-content-around">
    <div class="text-white d-flex flex-column flex-wrap">
      <div v-for="(element, index) in sections" class="my-3">
        <h4>{{ sections[index].label }}</h4>
        <ul v-for="(element, index) in sections[index].links">
          <li>
            <a href="#">{{ element }}</a>
          </li>
        </ul>
      </div>
    </div>
    <div class="dx">
      <img src="../assets/img/dc-logo-bg.png" alt="not available" />
    </div>
  </footer>
  <div class="deepbottom" style="height: 100px">
    <div class="container" style="height: 100%">
      <div class="row d-flex align-items-center" style="height: 100%">
        <div class="col-6"><button>SIGN-UP NOW</button></div>
        <div class="col-6 d-flex align-items-center py-3" style="height: 100%">
          <h4 class="me-4">FOLLOW US</h4>
          <div
            v-for="(element, index) in socials"
            :key="index"
            class="mx-2 pb-1"
          >
            <a href="#">
              <img
                :src="`src/assets/img/${socials[index].logo}`"
                alt="not available"
                style="height: 100%"
              />
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
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
footer {
  background-image: url("../assets/img/footer-bg.jpg");
  background-size: cover;
  div.text-white {
    max-width: max-content;
    max-height: 600px;
    display: flex;
    flex-direction: column;
    z-index: 1;
    h4 {
      text-transform: uppercase;
    }
    ul {
      li {
        list-style-type: none;
        transform: translateX(-2em);
        a {
          text-decoration: none;
          color: gray;
          &:hover {
            color: $pointed-one;
          }
        }
      }
    }
  }
}
div.col-6 {
  h4 {
    color: $pointed-one;
  }
}
.deepbottom {
  background-color: $dark-color;
}
</style>
