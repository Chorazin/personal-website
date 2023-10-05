<template>
  <section>
    <parallax_comp v-bind:parallax_info='parallax_info_1' />
    <article>
      <div class='container'>
        <div>
          <p>
            <h4 class='underline'>Remember the good ole' days?</h4>
          </p>
          <p class='date'>
            Written by: Roger Atkins - Dev | Web | Design - 03/10/2023 <br/><br/>
          </p>
          <p>
            I still recall when our lead Java developer, a grin on his face, dropped a massive tome on my desk that looked like it belonged to a Wizard.
            'This is some kind of mistake' I thought, 'I want to learn Javascript, not practice the arcane arts'. And thus began my long on and off again
            relationship with javascript. To be fair I kind of had an idea of what I was getting myself into. Long days I sat the next desk over from
            our lead Java developer. Often times he could be heard muttering 'why isn't that working?!' or grumbling something about 'hash tables' when
            dealing with recalcitrant Javascript problems.
          </p>
          <p>
            Back then there was no real stack overflow, the browser wars were in full swing, the joys of accessing DOM elements different for each
            browser. And alerts everywhere through your code to track down those incredibly descriptive 'null pointer' errors that the browser would
            throw your way. 'Ok I made it past alert five but crashed before alert six'. No inspect element, no console.log, tables dominated design,
            people had to get creative with frames and tables to realise their designs. And good old Dreamweaver's find replace all, what could possibly go wrong?
            Remember var's? And how amazingly strict(not) their scope was, 'Oh that is a block level scope, that var is available anywhere'.
          </p>
          <p>
            I recall after a hiatus from Javascript returning to building web apps/pages and using the inspect element functionality in google chrome's developer tools.
            This blew me away. Not only did it highlight the areas with a visual reference of what was margin, what was body etc, for the code I hovered over.
            But I could also scroll through the styles. And it provided information about where those styles were loaded from, and I could toggle them on and off
            and see their influence on the element on the page. Insert mind blown with explosions meme here.
          </p>
          <p>
            Javascript has seen some evolution over the years, let and const help with closure issues in certain instances. The older for(i=0 i<=x.length i++) has
            been mostly replaced by the higher order function foreach. Filter, map, reduce, sort are some other higher order functions that have been added to the toolset.
            I recall using the old getElementById back in the day, whereas now you are more likely to use something like querySelector or querySelectorAll to return
            a nodelist you can perform a forEach on. Spreader functions, template literals, even some paradigm changes. Callback functions due to Javascripts single
            threaded nature see a lot more use nowadays. Once you have done all the required tasks in this function, then go execute my callback function.
          </p>
          <p>
            Now let us look at an example of how much modern Javascript rocks. Granted it still has issues, and they are summed up perfectly in <a href="https://www.youtube.com/watch?v=Uo3cL4nrGOk&t=74s" target="_blank">this video.</a>
            It was built as a glue language for Netscape. Marc Andreessen, the founder of Netscape, believed that HTML needed a "glue language".
            That was easy to use by Web designers and part-time programmers to assemble components such as images and plugins, where the code could be
            written directly in the Web page markup. Based on Java syntax Brendan Eich wrote the prototype in 10 days, called Mocha internally it went
            out as livescript.
          </p>

        <br/>
        <hr class='gradient'/>
        <br/>
      </div>
      <javascript_class_desc_001 />
      <javascript_class_desc_002 />
    </div>
    <div class='spacer_vertical_100'>
      <middle_links />
    </div>
    <parallax_comp v-bind:parallax_info='parallax_info_2' />
      <div class='container'>
      <javascript_class_desc_003 />
    </div>
      <br/>
      <hr class='gradient'/>
      <br/>
    </article>
  </section>

</template>

<script>
import javascript_class_desc_001 from '../components/javascript_class_desc_001.vue'
import javascript_class_desc_002 from '../components/javascript_class_desc_002.vue'
import javascript_class_desc_003 from '../components/javascript_class_desc_003.vue'
import parallax_comp from '../components/parallax_comp.vue'
import middle_links from '../components/middle_links.vue'

export default {
  components: {
    javascript_class_desc_001,
    javascript_class_desc_002,
    javascript_class_desc_003,
    parallax_comp,
    middle_links
  },

  data() {
    return {
      parallax_info_1: {
        url: '/javascript_parallax_v002.jpg',
        heading:'JAVASCRIPT',
        quote: '- Null pointers you say?'
      },
      parallax_info_2: {
        url: '/javascript_parallax_2_v001.jpg',
        heading:'"THIS IS THE WAY"',
        quote: '- Mando'
      }
    }
  },

  transition: {
    name: 'fade',
    mode: 'out-in'
  },

  head() {
    return{
      title: 'Javascript',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'Roger Atkins relationship with javascript'
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
</style>
