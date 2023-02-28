<script>
export default {
  props: {
    headerLinks: Array,
  },
};
</script>

<template>
  <header>
    <div class="container">
      <img src="../assets/img/dc-logo.png" alt="Logo" />
      <ul>
        <li v-for="(link, index) in headerLinks" :key="link.label">
          <a :href="link.url">{{ link.label }}</a>
        </li>
      </ul>
    </div>
  </header>
</template>

<style lang="scss" scoped>
@use "../assets/scss/partials/_mixins.scss" as *;

header {
  .container {
    width: 1000px;
    margin: auto;
  }

  li {
    display: inline-block;
    margin: 0 0.5rem;
  }

  a {
    text-decoration: none;
    color: #333333;
    font-size: 0.7rem;
    text-transform: uppercase;
    font-weight: bold;
  }

  img {
    width: 40px;
  }

  div {
    @include flex-between();
    padding: 10px 30px;
  }
}
</style>
