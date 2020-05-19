<template>
  <div>
    PERSONAL PROJECTS
  </div>
</template>

<script>
  export default {

    transition: {
      name: 'fade',
      mode: 'out-in'
    },

    components: {

    },

    head() {
      return{
        title: 'Personal Projects',
        meta: [
          {
            hid: 'description',
            name: 'description',
            content: 'Some recent personal projects'
          }
        ]
      }
    },

    data() {
      return {
        parallax_info_10: {
          url: '/javascript_parallax_3_v001.jpg',
          heading:'"WELL, THAT\'S A SWITCH"',
          quote: '- Private Hudson'
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
