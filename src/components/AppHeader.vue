<script>
export default {
  data() {
    return {
      title: "Header",
    };
  },
};
</script>

<template>
  <header>
    <div class="container">
      <img src="../assets/img/dc-logo.png" alt="Logo" />
      <ul>
        <li><a href="#">CHARACTERS</a></li>
        <li><a href="#">COMICS</a></li>
        <li><a href="#">MOVIES</a></li>
        <li><a href="#">TV</a></li>
        <li><a href="#">GAMES</a></li>
        <li><a href="#">COLLECTIBLES</a></li>
        <li><a href="#">VIDEOS</a></li>
        <li><a href="#">FANS</a></li>
        <li><a href="#">NEWS</a></li>
        <li><a href="#">SHOP</a></li>
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
  }

  img {
    width: 40px;
  }

  background-color: white;
  div {
    @include flex-between();

    padding: 10px 30px;

    background-color: red;
  }
}
</style>
