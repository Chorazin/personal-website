<template>
  <div>
    <div v-if='this.parallax_info' class='overlay_txt'>
      <h3 v-if='this.parallax_info.heading'>{{this.parallax_info.heading}}</h3>
      <p class='spiel'>{{this.parallax_info.quote}}</p>
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
  props: ['parallax_info'],

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
  margin-bottom: 2px;
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
  margin-right: 10%;
  top: 30%;
  color: var(--main_gold_color);
}

.spiel {
  font-size: 2em;
  text-align: right;
  margin-right: 0px;
  margin-top: 0px;
  font-family: Impact, Charcoal, sans-serif;
}





@media only screen and (max-width: 700px) {
  .overlay_txt {
      margin-left: 0px;
      margin-right: 0px;
  }
  h3 {
    font-family: "roboto";
    font-size: 3em;
  }
}

@media only screen and (max-width: 1200px){
  .overlay_txt {
    margin: 30px;
    top: 0px;
  }
}
</style>
