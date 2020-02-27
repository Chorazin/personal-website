<template>
  <div>
    <!-- display text based on what variables are present -->
    <!--
    <div v-if='this.heading' class='overlay_txt'>
      <h3>{{heading}}</h3>
      <p class='spiel'>some cool text here</p>
    </div>
    <div v-if='this.heading_2' class='overlay_txt'>
      <h3>{{heading_2}}</h3>
    </div>
    <div class='svg_container'>
      <svg viewBox='0 0 1920 150'>
        <polygon points='0,0 960,150 1920,0 1920,150 0,150' fill='black' />
      </svg>
    </div>
  -->
  </div>
</template>

<script>

export default {
  name: 'main_header',
  props: [],

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
  border: 1px solid #eaa000;
  padding-left: 10px;
}
.overlay_txt {
  z-index: 2;
  position: absolute;
  right: 0px;
  margin-right: 300px;
  top: 30%;
  /* color: rgba(234, 160, 0, 1); */
  color: #eaa000;
}

.spiel {
  font-size: 2em;
  text-align: right;
  margin-right: 20px;
  font-family: Impact, Charcoal, sans-serif;
}

</style>
