<template>
  <section>
    <parallax_comp v-bind:parallax_info_5='parallax_info_5'/>
    <article>
      <div class='container spacer'>
        <p>
          <h4 class='underline'>The Ramblings of a Mad Man!</h4>
          <p>
            Written by: Roger Atkins - 12/3/2020 <br/><br/>
          </p>
          Well about myself I guess, firstly I am a long time Tottenham Hotspur supporter, although I feel sufferer is a better description. And a
          bit of a Cricket tragic. I am also a Newcastle Jets fan(go the Jets) and have been a Newcastle local for oh, 20 odd years now, although I have lived
          in Sydney before, in Artarmon and grew up in Port Macquarie.
        </p>
        <p>
          I got into web simply because I was interested in HTML initially, then CSS. And eventually when you get frustrated with the limitations using just
          HTML/CSS, Javascript is the next natural progression. From there it was a lot of the surrounding software that goes along with websites in the early
          2000's, Dreamweaver and Flash were big with Actionscript dominating any sort of animation. And of course Photoshop and Illustrator, and whatever IDE
          you felt comfortable building in. Technically I guess you could say my first job was what would now be called a Front End Developer. Although back in
          the early 2000's I was happily known as the UI guy, Graphics guy.
        </p>
        <p>
          From there I have worked mostly in the web world/media fields, wearing many and varied hats. Given I have always worked with smaller agencies, the need for people to
          be flexible was high. I havn't been just a Front End Developer, I have done some graphic design, some marketing, some traditional media such as film, some
          content creation. Even some print media.
        </p>
        <p>
          Although I would definitely cede that my main skills lie within the Front End Dev sphere, the intersection of humans and technology. But feel I can definitely
          provide some assistance, input and feedback on media, digital design, graphic design, UI/UX, and marketing.
        </p>
      </div>
        <parallax_comp v-bind:parallax_info_4='parallax_info_4'/>
        <div class='container'><div>
        <p>
          For now my tech stack I like to build with is Vue.js(CLI 3.0) and it's surrounding ecosystem, such as
        <div class='row'>
          <div class='col s12 m4'>
            <ul>
              <li><a href='https://nuxtjs.org/' target='_blank'>Nuxt.js</a></li>
              <li><a href='https://vuetifyjs.com/en/' target='_blank'>Vuetify</a></li>
              <li><a href='https://materializecss.com/' target='_blank'>Materialize</a></li>
              <li><a href='https://getbootstrap.com/' target='_blank'>Bootstrap</a></li>
              <li><a href='https://firebase.google.com/' target='_blank'>Firebase</a></li>
            </ul>
          </div>
          <div class='col s12 m4'>
            <ul>
              <li><a href='https://nodejs.org/en/' target='_blank'>Node.js</a></li>
              <li><a href='https://www.mongodb.com/' target='_blank'>MongoDb</a></li>
              <li><a href='https://mongoosejs.com/docs/' target='_blank'>Mongoose</a></li>
              <li><a href='http://expressjs.com/' target='_blank'>Express</a></li>
              <li><a href='https://www.adobe.com/au/' target='_blank'>Adobe Suite</a></li>
          </ul>
          </div>
          <div class='col s12 m4'>
            <ul>
                <li><a href='https://www.figma.com/' target='_blank'>Figma</a></li>
                <li><a href='https://github.com/' target='_blank'>Github</a></li>
                <li><a href='https://webpack.js.org/' target='_blank'>Webpack</a></li>
                <li><a href='https://www.heroku.com/' target='_blank'>Heroku</a></li>
            </ul>
          </div>
        </div>
        <p>
          My next steps are trying a more structured and OO approach to CSS without relying on SCSS. A decoupling of visual and layout design and a more component based
          approach to CSS. I recently attended a great talk by <a href='https://www.youtube.com/watch?v=ZWPMzJfJHnc' target='_blank'>Mike Riethmuller on CSS
          Architecture for Modern Web Applications</a> which takes the CSS in JS paradigm to the next level.

          And GraphQL. I have already written a simple backend for GraphQL with MongoDb but I want to expand upon that and plug in a front
          end ui to replace the Graphiql query interface. So probably building it out in something like Vue, Vue-Apollo.
        </p>
        <p>
          Those derpy moments, we all have them, we have them all the time. I had two especially great ones building this website. The first was with a parallax where
          I had forgot I set a CSS colour variable on the overlaying elements body and thus couldnt see through the background-color: black; to the parallax below.
          going over my javascript for initialising the instance of the parallax, console logging everything. Moving javascript around inside component lifecycle hooks.
        </p>
        <p>
          And perhaps my favourite where I have put a css variable for a specific colour on the top level component so I could access it anywhere. Unfortunately I
          had copy pasted the wrong hashed colour. The joys I had tracking that down before I actually decided to read over the variable declaration with more
          scrutiny. thinking maybe it was something to do with Scoping, or something to do with component mount timers.
        </p>
        <br/>
        <hr class='gradient'/>
        <br/>
      </div>
    </div>

      <div class='container'>

    </div>
      <br/>
      <hr class='gradient'/>
      <br/>
    </article>
  </section>
</template>

<script>
import parallax_comp from '../components/parallax_comp.vue'

export default {
  components: {
    parallax_comp
  },

  transition: {
    name: 'fade',
    mode: 'out-in'
  },

  data() {
    return {
      parallax_info_4: {
        url: '/javascript_parallax_3_v001.jpg',
        heading:'TECH STACK',
        quote: "'-the factor'"
      },
      parallax_info_5: {
        url: '/javascript_parallax_4_v001.jpg',
        heading: '"I SET MY MIND IN MOTION"',
        quote: '- Piter De Vries'
      }
    }
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

.spacer {
  margin-bottom: 100px;
}

</style>
