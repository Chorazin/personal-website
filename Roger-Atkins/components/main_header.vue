<template>
  <div>
    <div v-if='this.parallax_info_1' class='overlay_txt'>
      <h3>{{this.parallax_info_1.heading}}</h3>
      <p class='spiel'>some cool text here</p>
    </div>
    <div v-if='this.parallax_info_2' class='overlay_txt'>
      <h3>{{this.parallax_info_2.heading}}</h3>
    </div>
    <div class='svg_container'>
      <svg viewBox='0 0 1920 150'>
        <polygon points='0,0 960,150 1920,0 1920,150 0,150' fill='black' />
      </svg>
    </div>

  </div>
</template>

<script>

export default {
  name: 'main_header',
  props: ['parallax_info_1', 'parallax_info_2', 'parallax_info_3'],

  data() {
    return {

    }
  }
}

</script>

<style scoped>

.svg_container {
  position: relative;
  line-height: 0;

}
svg {
  z-index: 2;
  position: absolute;
  min-width: 100%;
  bottom: -500px;
}

h3 {
  letter-spacing: 15px;
  font-family: "roboto";
  font-size: 5em;
  border: 1px solid;
  border-color: var(--main_gold_color);
  padding-left: 10px;
}
.overlay_txt {
  z-index: 2;
  position: absolute;
  right: 0px;
  margin-right: 300px;
  top: 30%;
  color: var(--main_gold_color);
}

.spiel {
  font-size: 2em;
  text-align: right;
  margin-right: 20px;
  font-family: Impact, Charcoal, sans-serif;
}

</style>
