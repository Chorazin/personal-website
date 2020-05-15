<template>
  <section>
    <parallax_comp v-bind:parallax_info='parallax_info_8'/>
    <article>
      <div class='container'>
        <p>
          <h4 class='underline'>Hosting?</h4>
        </p>
        <p class='date'>
            Written by: Roger Atkins - Dev | Web | Design - 15/5/2020 <br/><br/>
        </p>
        <p>
          So for this website I decided to try out Nuxt.js, yes a framework for Vue.js which is itself a library, although it can be a framework with some other tools.
          But bear with me, it is simply another layer of abstraction, on top of several. Much like Node.js is a layer of abstraction built on top of C via the V8 engine.
          And it does package in some fairly handy and time saving features. Server side rendering, clearly having your pages able to be crawled rather than spinners
          is a good thing
        </p>
      </div>
      <parallax_comp v-bind:parallax_info='parallax_info_9'/>
      <div class='container spacer'>

      </div>
    </article>
    <br/>
    <hr class='gradient'/>
    <br/>
  </section>
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
        parallax_info_8: {
          url: '/javascript_parallax_7_v001.jpg',
          heading: 'SITE BUILD',
          quote: '- Nuxt'
        },

        parallax_info_9: {
          url: '/javascript_parallax_8_v001.jpg',
          heading: '"Where do these stairs go?"',
          quote: '- Ray Stantz'
        }
      }
    },

    mounted() {
      //setup materialize parallex on component mount
      const elems = document.querySelectorAll('.parallax');
      const instances = M.Parallax.init(elems);

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
