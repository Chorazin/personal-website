<template>
  <div>
    <div class="parallax-container">
      <div class="parallax">
        <!--make the text into components -->
        <div v-if='this.heading' class='overlay_txt'>
          <h3>{{heading}}</h3>
          <p class='spiel'>some cool text here</p>
        </div>
        <div v-if='this.heading_2' class='overlay_txt'>
          <h3>{{heading_2}}</h3>
        </div>
        <!--display only which img_src is passed to this component-->
        <img v-if='this.img_src' v-bind:src="`${this.img_src}`" class='responsive-img'>
        <img v-if='this.img_src_2' v-bind:src="`${this.img_src_2}`" class='responsive-img'>
        <div class='svg_container'>
          <svg viewBox='0 0 1920 150'>
            <polygon points='0,0 960,150 1920,0 1920,150 0,150' fill='black' />
          </svg>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
name: 'parallax_comp',
props: ['img_src', 'img_src_2', 'heading', 'heading_2'],



mounted() {
  //setup materialize parallex on component mount
  const elems = document.querySelectorAll('.parallax');
  const instances = M.Parallax.init(elems);
  console.log(this.img_src);
  }
}
</script>

<style scoped>

.start_color {
  stop-color:rgb(0,0,0);
  stop-opacity:1
}
.end_color {
  stop-color:rgb(10,10,10);
  stop-opacity:1
}

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
