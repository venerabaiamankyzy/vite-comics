<script>
export default {
  props: {
    comics: Array,
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
</style>
