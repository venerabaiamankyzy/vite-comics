<script>
export default {
  props: {
    products: Array,
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
    <section class="section">
      <div class="container main-main">
        <div v-for="product in products" :key="product.label">
          <div class="comics">
            <img :src="getImageUrl(product.productImg)" alt="Image" />
            <p>{{ product.label }}</p>
          </div>
        </div>
      </div>
    </section>
  </main>
</template>

<style lang="scss" scoped>
@use "../assets/scss/partials/mixins" as *;

.section {
  background-color: hsl(209deg 100% 49%);
  color: rgb(230, 230, 230);

  .main-main {
    @include flex-center("both");

    .comics {
      @include flex-center("both");
      margin: 40px 20px;
      // width: 160px;
      // height: 55px;

      img {
        max-width: 100%;
        width: 40px;
        color: rgb(230, 230, 230);
      }

      p {
        font-size: 0.7rem;
        padding-left: 8px;
        text-transform: uppercase;
      }
    }
  }
}
</style>
