<template>
  <section>
    <parallax_comp v-bind:parallax_info='parallax_info_10'/>
    <article>
      <div class='container spacer'>
        <p>
          <h4 class='underline'>Projects?</h4>
        </p>
        <p class='date'>
            Written by: Roger Atkins - Dev | Web | Design - 20/5/2020 <br/><br/>
        </p>
        <p>
          I have been working on a bunch of personal projects and one proof of concept for a business idea. Guess you could call it stage one, Alpha, something along those lines. So I will start
          there with <a href='https://sample-self-insure.firebaseapp.com/' target='_blank'>Self Insure</a>. My idea here was to just get a simple prototype up and running with CRUD operations and
          authentication utilising Vue.js(cli 3.0) and Firebase. We are at a point where it needs to be more fleshed out from a business model perspective.
          What data from the user are we collecting? Custom flags and levels of administration? Use case scenarios? Have we got a backend engineer on board yet?
          I can do some backend but definitely am much more visual/front end oriented. For a full application and fleshing out the architecture I would want a backend engineer on board. Moving database actions to cloud functions
          and aggregating them all as a service, etc etc<br/><br/> This is more an ongoing thing as
          we get in Slack and thrash it out and bound by work and time zone constraints. People are in Bangkok, London, Sydney, me here in Newcastle.
        </p>
        <p>
          Graphql, I got interested in Graphql so thought I would spend some time taking a look at it's workings. I put together a simple directors, movies MongoDB database <a href='https://github.com/Chorazin/graphql_test_bed' target='_blank'>here</a> and hooked up a simple
          Graphiql query line. I may put a front end on it at a later date, most likely with Vue Apollo.
        </p>
        <p>
          A proof of concept for using Materialize modals for all firebase interactions, signup, login, logout, Admin flags, and CRUD operations. Apart from some hitches with onAuthStateChanged
          triggering multiple times, which was a known bug at the time, it all went smoothly and the code can be found <a href='https://github.com/Chorazin/modal_login_testing' target='_blank'>here</a>.
        </p>
        <p>
          I put together a <a href='https://real-time-chat-74431.firebaseapp.com/' target='_blank'>real time chat</a> using Firebase's Firestore real time database. The ability to put an observer on a collection and specify what changes to act upon is amazingly handy.
          The functionality rolled into Firebase's onSnapShot is impressive, and from a developers perspective brings some real power to the table with minimal code.
        </p>
        <p>
          This last one makes me a little sad, I wrote an app using Google maps API. And around one month after I completed it they changed what functionality was accessible for free and
          what was not. So you have to allow the app to know your location and it stores those co-ords and pinpoints your location on the map with a tab. Clicking on the tab takes you to a
          chat page for that user. The co-ords are stored by user so if you shift locations your tab moves with you when you log back in. And is still accessible on Google Maps to click on and
          chat.
        </p>
      </div>
      <div class='mid_link_spacer'>
        <middle_links />
      </div>
      <parallax_comp v-bind:parallax_info='parallax_info_11'/>
      <div class='container spacer'>
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
          url: '/javascript_parallax_9_v001.jpg',
          heading:'PROJECTS',
          quote: '- Go build something'
        },
        parallax_info_11: {
          url: '/javascript_parallax_10_v001.jpg',
          heading:'"WELL, THAT\'S A SWITCH"',
          quote: '- Private Hudson'
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
.spacer {
  margin-bottom: 100px;
  margin-top: 100px;
}

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
