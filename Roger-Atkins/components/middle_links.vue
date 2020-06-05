<template>
  <section>
    <div class='container row icon_section center-align'>
      <div class='col m4 s12'>
        <link_flip v-bind:link_info = 'link_info_one' />
      </div>
      <div class='col m4 s12'>
        <link_flip v-bind:link_info = 'link_info_two' />
      </div>
      <div class='col m4 s12'>
        <link_flip v-bind:link_info = 'link_info_three' />
      </div>
    </div>
  </section>
</template>


<script>
import link_flip from '../components/link_flip.vue'



export default {
  name: 'middle_links',

  components: {
    link_flip
  },

  data(){
    return {
      link_info_one: {
        link: 'content_creation',
        header: 'CONTENT CREATION',
        icon: 'donut_small'
      },
      link_info_two: {
        link: 'build',
        header: 'BUILD',
        icon: 'airplay'
      },
      link_info_three: {
        link: 'personal_projects',
        header: 'PROJECTS',
        icon: 'cloud_circle'
      }
    }
  }
}
</script>



<style>
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
