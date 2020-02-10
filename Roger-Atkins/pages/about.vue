<template>
  <div class='container animation test'>
    <h2>ABOUT ME</h2>
    <p>This is my about page</p>
  </div>
</template>

<script>
export default {
  transition: {
    name: 'fade',
    mode: 'out-in'
  },


  head() {
    return{
      title: 'About Roger Atkins',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'About page for Roger Atkins'
        }
      ]
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
