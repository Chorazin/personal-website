<template>
  <section>
    <parallax_comp v-bind:parallax_info_6='parallax_info_6'/>
    <article>
      <div class='container'>
        <div>
          <p>
            <h4 class='underline'>Build it, and they will come.</h4>
          </p>
          <p class='date'>
              Written by: Roger Atkins - 3/4/2020 <br/><br/>
          </p>
          <p>
            Content creation, welcome fellow content creators, this section is for you. This probably is not very relevent to the Javascript folks so if that is more your thing
            I would redirect you <nuxt-link :to='{name: "javascript"}'>here</nuxt-link>. Content creation has been by far the biggest time sink building this site.
            The technical aspects are relatively light, no backend other than some SSR handled by Nuxt. No database connections, CRUD operations and authentication, no middleware
            or micro services. But writing all the content is time consuming. And proof reading, changing and editing paragraphs to be more concise, what information is relevent,
            what can be omitted, etc etc. And of course graphical content, animation and sound.
          </p>
          <p>
            For myself I have been in content creation from a marketing/advertising perspective mostly. Utilising tools such as the ubiquitous <a href='https://www.adobe.com/au/' target='blank'>Adobe Suite</a>.
            And 3d modeling tools such as
            <a href='https://pixologic.com/' target='blank'>Zbrush</a>, <a href='https://www.autodesk.com.au/products/maya/overview' target='blank'>Maya</a>,
            <a href='https://www.lightwave3d.com/' target='blank'>Lightwave</a>, video editing tools such as<a href='https://www.blackmagicdesign.com/au/products/davinciresolve/' target='blank'>
            Resolve</a> and <a href='https://www.adobe.com/au/products/aftereffects.html' target='blank'>After Effects</a>. But I feel for content creation the best way to convey
            a message is in a visual style. I put together a short clip of some stuff I have worked on from personal projects to projects for clients.
          </p>
        </div>
        <div class='row video_spacer'>
          <div class='col m12 s12 center'>
            <video controls width='818' height='460'>
              <source src='../assets/simple_cc_clip_v001.mp4' type='video/mp4'>
              <source src='movie.ogg' type='video/ogg'>
            </video>
          </div>
        </div>
      </div>
      <parallax_comp v-bind:parallax_info_7='parallax_info_7'/>
      <div class='container'>
        Looking forward from a content creation perspective I am looking to do a deep dive into Davinci Resolve. With an eventual goal of moving away from Adobe, this is more
        for the fact I like to own my software rather than rent it out.
      </div>
    </article>
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
      title: 'Content Creation',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'Content Creation by Roger Atkins'
        }
      ]
    }
  },

  data() {
    return {
      parallax_info_6: {
        url: '/javascript_parallax_5_v001.jpg',
        heading: 'CONTENT CREATION',
        quote: '- The Construct'
      },

      parallax_info_7: {
        url: '/javascript_parallax_6_v001.jpg',
        heading: '"Your mind makes it real"',
        quote: '- Morpheus'
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
video {
  max-width: 100%;
  width: 100%;
  height: auto;
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


/*LAYOUT STYLES --------------------*/
.video_spacer {
  margin-top: 80px;
  margin-bottom: 50px;
}
</style>
