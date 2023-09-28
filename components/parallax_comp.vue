<template>
  <div>
    <div class="parallax-container">
      <div class="parallax">
        <img v-if="this.parallax_info" v-bind:src="this.parallax_info.url" class='responsive-img hide-on-small-only'>

        <main_header v-bind:parallax_info='parallax_info' />
      </div>
    </div>
  </div>
</template>

<script>
import main_header from './main_header.vue'

export default {
  components: {
    main_header
  },

  name: 'parallax_comp',
  props: ['parallax_info']
  
}
</script>

<style>
@media only screen and (max-width: 1200px){
  .parallax-container {
    height: 300px;
  }
}
</style>
