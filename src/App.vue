<script>
import AppHeader from "./components/AppHeader.vue";
import AppFooter from "./components/AppFooter.vue";
import AppMain from "./components/AppMain.vue";

export default {
  name: "",
  components: { AppHeader, AppFooter, AppMain },

  data() {
    return {
      title: "Hello World",
    };
  },
};
</script>

<template>
  <AppHeader />
  <main>
    <AppMain />
  </main>
  <AppFooter />
</template>

<style lang="scss" scoped>
@use "./assets/scss/general.scss" as *;

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  margin: 0;
}
</style>
