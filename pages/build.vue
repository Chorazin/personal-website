<template>
  <section>
    <parallax_comp v-bind:parallax_info='parallax_info_8'/>
    <article>
      <div class='container'>
        <p>
          <h4 class='underline'>Hosting?</h4>
        </p>
        <p class='date'>
            Written by: Roger Atkins - Dev | Web | Design - 30/09/2023 <br/><br/>
        </p>
        <p>
          So for this website I decided to try out Nuxt.js, a framework for Vue.js, yes I know, a framework for a library.
          But bear with me, it is simply another layer of abstraction, on top of several. Much like Node.js is a layer of abstraction built on top of C++ via the V8 engine.
          And Nuxt does package in some fairly handy and time saving features. Server side rendering, clearly having your pages able to be crawled rather than spinners
          is a good thing. The other big advantage is routing, Nuxt handles routing much as it would be in say a PHP application. Create a Vue.js file and drop it in
          the pages directory and you are good to go. Nuxt builds out your router file for you, it also has in built functionality to handle dynamic links like user sign
          up home page, posts etc. Although to add an extra layer of security to your router file will still have to be done manually. Say if you are checking authentication
          before allowing a user to navigate to a certain page.
        </p>
        <p>
          The site build itself is pretty straight forward from a technical standpoint. No database operations to worry about, no middleware, no pulling of content from microservices. No authentication,
          not even really enough data being passed around to warrant a Vuex store which comes pre packaged with Nuxt if you need it. I created a few components to make my life easier,
          such as the parallax areas i can just pass an object to containing the information about which image to use and which quote.
        </p>
        <p>
          So why Nuxt over say Gridsome? It simply was a flip of the coin to tell the truth, I could of gone with either framework. Next time around I will probably give
          Gridsome a try. For my CSS I opted for Materialize CSS framework, based on Google's material design. I'd used Vuetify in a recent project and wanted to go back to bashing away at
          Materialize. Although in hindsight I think I should have done a dive into TailwindCSS as it seems to be gaining a lot of traction.
        </p>
        <p>
          I did the rough wireframing for the site in Figma and am quite pleased with how it runs and is set up. Figma is a collaboration tool for designers with a lot
          of nifty features for teams. Anyone on the team can post sticky notes on works commenting, 'need more pop here!', 'this is great!' etc and structurally it is
          based around design components, built out of smaller building blocks.
        </p>
        <p>
          For hosting I went with Heroku initiall back in 2020, I don't think my job application traffic will ever push my free Dyno to cap so seemed a good option. But recently
          Heroku went to a paid only format, no free Dyno's for small personal projects so I have shifted my hosting to Vercel.
          Vercel even has it's own CLI for projects and for deployment from Git.
        </p>
      </div>
      <div class='spacer_vertical_100'>
        <middle_links />
      </div>
      <parallax_comp v-bind:parallax_info='parallax_info_9'/>
      <div class='container'>
        <p>
          <h4 class='underline'>Cross browser, cross platform?</h4>
          For myself I am just sticking with modern browsers, I figure the majority of my target audience(job applications) will be on modern tech. It is not like I have to support
          redundancy software. I may get around to testing for Mac Safari, but all my main testing has been done in the latest version of Chrome(Version 83.0.4103.61) and Firefox(76.0.1). As for
          anyone that has disbaled Javascript in the browser, that is a lot harder to cater for given this is built with Vue.js within a Nuxt.js framework.
        </p>
        <p>
          I will probably add to the site at a later date, I certainly wanted to use photos of Newcastle but realised my library for such was rather lacking. Might dedicate a day
          to taking some swell shots of my home town.
        </p>
        <p>
          I might also go through the process for something like say 3d modeling. From
          conception and initial illustrations to modeling the wireframe mesh in say Zbrush. Then exporting the model into Lightwave, applying textures, lights and
          setting up a scene to rendering and compiling in Resolve.
        </p>
      </div>
    </article>
    <br/>
    <hr class='gradient'/>
    <br/>
  </section>
</template>

<script>
import parallax_comp from '../components/parallax_comp.vue'
import middle_links from '../components/middle_links.vue'

export default {

  transition: {
    name: 'fade',
    mode: 'out-in'
  },

  components: {
      parallax_comp,
      middle_links
  },

  head() {
    return{
      title: 'Site Build',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'The tech stack used to build this website'
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
