<template>
  <div>
    <parallax_comp v-bind:parallax_info_6='parallax_info_6'/>
    THIS IS MY CONTENT CREATION PAGE YAY!
  </div>
</template>

<script>
import parallax_comp from '../components/parallax_comp.vue'

export default {

  transition: {
    name: 'fade',
    mode: 'out-in'
  },

  components: {
    parallax_comp
  },

  head() {
    return{
      title: 'Content Creation',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'Content Creation by Roget Atkins'
        }
      ]
    }
  },

  data() {
    return {
      parallax_info_6: {
        url: '/javascript_parallax_4_v001.jpg',
        heading: '"Your mind makes it real"',
        quote: '- Morpheus'
      }
    }
  }
}
</script>

<style scoped>

.fade-enter-active,
.fade-leave-active {
  transition-duration: 0.5s;
  transition-property: opacity;
  transition-timing-function: ease;
}

.fade-enter,
.fade-leave-active {
  opacity: 0
}
</style>
