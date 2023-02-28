<script></script>

<template>
  <div class="jumbotron">
    <div class="btn">
      <span>CURRENT SERIES</span>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.jumbotron {
  position: relative;

  min-height: 350px;
  background-image: url(../assets/img/jumbotron.jpg);
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center top;

  .btn {
    position: absolute;
    top: 330px;
    left: 15.5%;

    font-size: 1.2rem;
    font-weight: bold;
    background-color: hsl(209deg 100% 49%);
    color: white;
    padding: 8px 14px;
  }
}
</style>
