<template>
  <section>
    <div class='container row icon_section center-align'>
      <div class='col m4 s12'><i class="material-icons"><nuxt-link :to='{name: "content_creation"}'>donut_small</nuxt-link></i></div>
      <div class='col m4 s12'><i class="material-icons"><nuxt-link :to='{name: "build"}'>airplay</nuxt-link></i></div>
      <div class='col m4 s12'><i class="material-icons"><nuxt-link :to='{name: "personal_projects"}'>cloud_circle</nuxt-link></i></div>
    </div>
  </section>
</template>


<script>
export default {
  name: 'middle_links'

}
</script>



<style scoped>
.icon_section {
  font-family: "roboto";
}

.material-icons{
   font-size: 48px;
}


</style>
