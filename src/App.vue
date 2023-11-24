<template>
  <HeaderNew />
  <MainNew />
  <FooterNew />
</template>

<script>
import HeaderNew from "./components/HeaderNew.vue";
import FooterNew from "./components/FooterNew.vue";
import MainNew from "./components/MainNew.vue";

export default {
  name: "App",
  components: {
    HeaderNew,
    FooterNew,
    MainNew,
  },
};
</script>

<style>
html {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
*,
*::after,
*::before {
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}
</style>
