<script>
export default {
  props: {
    comics: Array,
  },

  data() {
    return {
      products: [
        {
          productImg: "buy-comics-digital-comics.png",
          label: "Digital Comics",
          link: "#",
        },

        {
          productImg: "buy-comics-merchandise.png",
          label: "DS Merchandise",
          link: "#",
        },
        {
          productImg: "buy-comics-subscriptions.png",
          label: "Subscriptions",
          link: "#",
        },

        {
          productImg: "buy-comics-shop-locator.png",
          label: "Comic Shop Locator",
          link: "#",
        },

        {
          productImg: "buy-dc-power-visa.svg",
          label: "Dc Power Visa",
          link: "#",
        },
      ],
    };
  },

  methods: {
    getImageUrl(name) {
      return new URL(`../assets/img/${name}`, import.meta.url).href;
    },
  },
};
</script>

<template>
  <main>
    <div class="container">
      <section class="section1">
        <div>
          <ul>
            <li v-for="comic in comics" :key="comic.series">
              <div class="card-img">
                <img :src="comic.thumb" alt="comic" />
              </div>
              <div class="card-desc">
                <h3>{{ comic.series }}</h3>
              </div>
            </li>
          </ul>
        </div>
        {{ title }}
      </section>

      <section class="section2">
        <div
          v-for="(product, index) in products"
          :key="product.label"
          class="main-main"
        >
          <div class="comics">
            <img :src="getImageUrl(product.productImg)" alt="Image" />
            <p>{{ product.label }}</p>
          </div>
        </div>
      </section>
    </div>
  </main>
</template>

<style lang="scss" scoped>
@use "../assets/scss/partials/mixins" as *;

main {
  background-color: black;
}
.section1 {
  padding: 60px 0;
  .card-img {
    width: 150px;
    height: 150px;

    img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      object-position: center top;
    }
  }
  ul {
    @include flex-center("horizontal");
    flex-wrap: wrap;
    gap: 1.5rem;

    li {
      max-width: 145px;
    }
  }

  .card-desc {
    font-size: 0.6rem;
    text-transform: uppercase;
    color: white;
    padding-top: 0.5rem;
  }
}

.section2 {
  background-color: hsl(209deg 100% 49%);
  width: 100%;
  @include flex-center("both");

  .main-main {
    @include flex-center("both");
    color: white;

    .comics {
      @include flex-center("both");
      padding: 20px 20px;

      img {
        max-width: 100%;
        width: 15%;
      }

      p {
        font-size: 0.9rem;
        padding-left: 15px;
      }
    }
  }
}
</style>
