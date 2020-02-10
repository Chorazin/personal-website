<template>
  <div>
    <header_navig />
    <nuxt />
    <footer_spam />
  </div>
</template>

<script>
import header_navig from "../components/header_navig.vue";
import footer_spam from "../components/footer_spam.vue";

export default {
  components: {
    header_navig,
    footer_spam
  }
}
</script>


<style>
body {
  background-color: #000000;
  color: #9e9e9e;
}

@font-face {
  font-family: lobster;
  src: url(../assets/fonts/lobster 1.4.otf);
}

@font-face {
  font-family: roboto;
  src: url(../assets/fonts/Roboto-Regular.ttf);
}

</style>
