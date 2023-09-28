<template>
  <section>
    <parallax_comp v-bind:parallax_info='parallax_info_10'/>
    <article>
      <div class='container'>
        <p>
          <h4 class='underline'>Projects?</h4>
        </p>
        <p class='date'>
            Written by: Roger Atkins - Dev | Web | Design - 20/5/2020 <br/><br/>
        </p>
        <ul class='custom_list'>
          <li>
            <p>
              I have been working on a bunch of personal projects and as part of a team for a proof of concept for a business idea. Guess you could call it stage one, Alpha, something along those lines. So I will start
              there with <a href='https://sample-self-insure.firebaseapp.com/' target='_blank'>Self Insure</a>. My idea here was to just get a simple prototype up and running with CRUD operations and
              authentication utilising Vue.js(cli 3.0) and Firebase. We are at a point where it needs to be more fleshed out from a business model perspective.
              What data from the user are we collecting? Custom flags and levels of administration? Use case scenarios? Have we got a backend engineer on board yet? Main content?
              I can do some backend but definitely am much more visual/front end oriented. For a full application and fleshing out the architecture I would want a backend engineer on board. Moving database actions to cloud functions
              and aggregating them all as services, etc etc.
            </p>
            <p>
              This is more an ongoing thing as
              we get in Slack and thrash it out, we are bound by work commitments and time zone constraints. People are in Bangkok, London, Sydney, me here in Newcastle.
            </p>
          </li>

          <li>
            <p>
              Graphql, I got interested in Graphql so thought I would spend some time taking a look at it's workings. I put together a simple directors, movies MongoDB database <a href='https://github.com/Chorazin/graphql_test_bed' target='_blank'>here</a> and hooked up a simple
              Graphiql query line. I may put a front end on it at a later date, most likely with Vue Apollo.
            </p>
          </li>

          <li>
            <p>
              A proof of concept for using Materialize modals for all firebase interactions, signup, login, logout, Admin flags, and CRUD operations. Apart from some hitches with onAuthStateChanged
              triggering multiple times, which was a known bug at the time, it all went smoothly and the code can be found <a href='https://github.com/Chorazin/modal_login_testing' target='_blank'>here</a>.
            </p>
          </li>

          <li>
            <p>
              I put together a <a href='https://real-time-chat-74431.firebaseapp.com/' target='_blank'>real time chat</a> using Firebase's Firestore real time database. The ability to put an observer on a collection and specify what changes to act upon is amazingly handy.
              The functionality rolled into Firebase's onSnapShot is impressive, and from a developers perspective brings some real power to the table with minimal code.
            </p>
          </li>

          <li>
            <p>
              This one makes me a little sad, I wrote an <a href='https://geo-auth-82a6d.firebaseapp.com/login' target='_blank'>app</a> using Google maps API. And around one month after I completed it they changed what functionality was accessible for free and
              what was not. But the basic gist of the app was to know your location and store those co-ords to pinpoint your location on Google maps with a tab marker. Clicking on the tab takes you to a
              chat page for that user. The co-ords are stored by user so if you shift locations your tab moves with you when you log back in. And is still accessible on Google Maps to click on and
              chat.
            </p>
          </li>

          <li>
            <p>
              And of course this Nuxt.js website, although this I cede is more of an exercise in design than my other projects. No middleware, authenticaion, database, microservices, etc to worry
              about, just setting up Nuxt.js, building with Vue.js and hosting on Heroku.
            </p>
          </li>
        </ul>
      </div>
      <div class='spacer_vertical_100'>
        <middle_links />
      </div>
      <parallax_comp v-bind:parallax_info='parallax_info_11'/>
      <div class='container'>
        <p>
          <h4 class='underline'>Future projects?</h4>
          My next project will be a Svelte and TailwindCSS project on the front end, with Node.js on the backend.
          Undecided on what I will build yet but that is 100% my tech stack unless I score a job somewhere that requires me to learn
          specific software for the role. From a content creation, design perspective a deep dive into Davince Resolve, and to spend some more time in Figma are my plans.
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
          quote: '- Go forth and build'
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
ul:not(.browser-default)>li {
  list-style-type: circle;
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
