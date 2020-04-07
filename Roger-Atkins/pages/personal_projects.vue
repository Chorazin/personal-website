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
