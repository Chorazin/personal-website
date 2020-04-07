<template>
  <div>
    HOW I BUILT THIS SITE
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
        title: 'Site Build',
        meta: [
          {
            hid: 'description',
            name: 'description',
            content: 'The tech stack used to build the website'
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
