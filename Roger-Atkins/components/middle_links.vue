<template>
  <section>
    <div class='container row icon_section center-align'>
      <div class='col m4 s12'>
        <div class="flip-card">
          <div class="flip-card-inner">
            <div class="flip-card-front">
              <i class="material-icons"><nuxt-link :to='{name: "content_creation"}'>donut_small</nuxt-link></i>
            </div>
            <div class="flip-card-back">
              <nuxt-link :to='{name: "content_creation"}'><h4>CONTENT CREATION</h4></nuxt-link>
            </div>
          </div>
        </div>
      </div>
      <div class='col m4 s12'>
        <div class="flip-card">
          <div class="flip-card-inner">
            <div class="flip-card-front">
              <i class="material-icons"><nuxt-link :to='{name: "build"}'>airplay</nuxt-link></i>
            </div>
            <div class="flip-card-back">
              <nuxt-link :to='{name: "build"}'><h4>BUILD</h4></nuxt-link>
            </div>
          </div>
        </div>
      </div>
      <div class='col m4 s12'>
        <div class="flip-card">
          <div class="flip-card-inner">
            <div class="flip-card-front">
              <i class="material-icons"><nuxt-link :to='{name: "personal_projects"}'>cloud_circle</nuxt-link></i>
            </div>
            <div class="flip-card-back">
              <nuxt-link :to='{name: "personal_projects"}'><h4>PROJECTS</h4></nuxt-link>
            </div>
          </div>
        </div>
      </div>
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


.flip-card {
  background-color: transparent;
  perspective: 1000px; /* Remove this if you don't want the 3D effect */
}

/* This container is needed to position the front and back side */
.flip-card-inner {
  position: relative;
  width: 100%;
  height: 100%;
  text-align: center;
  transition: transform 0.3s;
  transform-style: preserve-3d;

}

/* Do an horizontal flip when you move the mouse over the flip box container */
.flip-card:hover .flip-card-inner {
  transform: rotateY(180deg);
}

/* Position the front and back side */
.flip-card-front, .flip-card-back {
  position: absolute;
  width: 100%;
  height: 100%;
  -webkit-backface-visibility: hidden; /* Safari */
  backface-visibility: hidden;
}

/* Style the front side (fallback if image is missing) */
.flip-card-front {
  background-color: #000;
  color: black;
}

/* Style the back side */
.flip-card-back {
  background-color: #000;
  color: white;
  transform: rotateY(180deg);
  margin-top: -20px;
}
</style>
