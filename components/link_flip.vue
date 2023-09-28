<template>
  <div>
    <div class="flip-card">
      <div class="flip-card-inner">
        <div class="flip-card-front">
          <i class="material-icons"><nuxt-link :to='{name: `${link_info.link}`}'>{{link_info.icon}}</nuxt-link></i>
        </div>
        <div class="flip-card-back">
          <nuxt-link :to='{name: `${link_info.link}`}'><h4>{{link_info.header}}</h4></nuxt-link>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

  export default {
    data() {
      return {

      }
    },

    name: 'link_flip',
    props: ['link_info']
  }
</script>





<style scoped>

</style>
