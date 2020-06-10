<template>
  <div class='pointer'>
    <div class='wrapping_element padding_bottom_100'>
      <header_navig />
      <nuxt />
    </div>
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
/*VISUAL STYLES ---------------------*/
/*Core CSS root files for use cross site */
:root {
  --main_bg_color: rgba(0, 0, 0, 1);
  --main_gold_color: #eaa000;
  --main_grey_text_color: #9e9e9e;
}

body {
  background-color: var(--main_bg_color);
  color: var(--main_grey_text_color);
  pointer-events: none;
}

@font-face {
  font-family: lobster;
  src: url(../assets/fonts/lobster 1.4.otf);
}

@font-face {
  font-family: roboto;
  src: url(../assets/fonts/Roboto-Regular.ttf);
}

/*For use with the slide out footer*/
.wrapping_element {
  pointer-events: all;
  z-index: 1;
  position: relative;
  background-color: black;
}

.date {
  font-weight: bold;
}

hr.gradient {
    border: 0;
    height: 1px;
    background-image: linear-gradient(to right, rgba(255, 255, 255, 0), rgba(255, 255, 255, 0.75), rgba(255, 255, 255, 0));
}

.underline{
  border-bottom: 1px solid rgba(234, 160, 0, 1);
  padding-bottom: 15px;
  width: 40%;
}


/*LAYOUT STYLES --------------------*/
.spacer_vertical_100 {
  margin-bottom: 100px;
  margin-top: 100px;
}
.top_margin_100 {
  margin-top: 100px;
}
.padding_bottom_100 {
  padding-bottom: 100px;
}
</style>
