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
:root {
  --main_bg_color: #000000;
  --main_gold_color: #eaa000;
  --main_grey_text_color: #9e9e9e;
}

body {
  background-color: var(--main_bg_color);
  color: var(--main_grey_text_color);
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
