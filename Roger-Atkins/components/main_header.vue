<template>
  <div>
    <div v-if='this.parallax_info_1' class='overlay_txt'>
      <h3>{{this.parallax_info_1.heading}}</h3>
      <p class='spiel'>{{this.parallax_info_1.quote}}</p>
    </div>
    <div v-if='this.parallax_info_2' class='overlay_txt'>
      <h3>{{this.parallax_info_2.heading}}</h3>
      <p class='spiel'>{{this.parallax_info_2.quote}}</p>
    </div>
    <div v-if='this.parallax_info_3' class='overlay_txt'>
      <h3 v-if='this.parallax_info_3.heading'>{{this.parallax_info_3.heading}}</h3>
      <p class='spiel'>{{this.parallax_info_3.quote}}</p>
    </div>
    <div v-if='this.parallax_info_4' class='overlay_txt'>
      <h3>{{this.parallax_info_4.heading}}</h3>
      <p class='spiel'>{{this.parallax_info_4.quote}}</p>
    </div>
    <div v-if='this.parallax_info_5' class='overlay_txt'>
      <h3>{{this.parallax_info_5.heading}}</h3>
      <p class='spiel'>{{this.parallax_info_5.quote}}</p>
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
  props: ['parallax_info_1', 'parallax_info_2', 'parallax_info_3', 'parallax_info_4', 'parallax_info_5'],

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
      margin-right: 80px;
  }
}
</style>
