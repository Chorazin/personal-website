<template>
  <div>
    <div class="parallax-container">
      <div class="parallax">
        <img v-if="this.parallax_info_1" v-bind:src="this.parallax_info_1.url" class='responsive-img'>
        <img v-if='this.parallax_info_2' v-bind:src="this.parallax_info_2.url" class='responsive-img'>
        <img v-if='this.parallax_info_3' v-bind:src="this.parallax_info_3.url" class='responsive-img'>
        <main_header v-bind:parallax_info_1='parallax_info_1, parallax_info_2, parallax_info_3' />
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
  props: ['parallax_info_1', 'parallax_info_2', 'parallax_info_3'],

  }
</script>

<style scoped>



</style>
