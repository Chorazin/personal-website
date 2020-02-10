<template>
  <section class='container'>
    <article>
      <div>
        <h4>JAVASCRIPT</h4>
        <p>
          I still recall when our lead Java developer, a grin on his face, dropped a massive tome on my desk that looked like it belonged to a Wizard.
          'This is some kind of mistake' I thought, 'I want to learn Javascript, not read War and Peace'. And thus began my long on and off again
          relationship with javascript. To be fair I kind of had an idea of what I was getting myself into. Long days I sat the next desk over from
          our lead Java developer. Often times he could be heard muttering 'why isn't that working?!' or grumbling something about 'hash tables' when
          dealing with recalcitrant Javascript problems. They have invented fancy names for roles over the years, front end developer, full stack dev, UI/UX
          designer. Hell even Javascript itself has conjured up new names for things that were just accepted as part of the functionality of the language.
          Hoisting and event bubbling spring to mind.
        </p>

        <p>
          Back then there was no real stack overflow, the browser wars were in full swing, the joys of accessing DOM elements different for each
          browser. And alerts everywhere through your code to track down those incredibly descriptive 'null pointer' errors that the browser would
          throw your way. 'Ok I made it past alert five but crashed before alert six'. No inspect element, no console.log, tables dominated design,
          people had to get creative with frames and tables to realise their designs. And good old Dreamweaver's find replace all, what could possibly go wrong?
          Remember var's? And how amazingly strict(not) their scope was, 'Oh that is a block level scope, that var is available anywhere'.
        </p>

        <p>
          I recall after a hiatus from Javascript returning to building web apps/pages and using the inspect element functionality in google chrome.
          This blew me away. Not only did it highlight the areas with a visual reference of what was margin, what was body etc, for the code I hovered over.
          But I could also scroll through the styles. And it provided information about where those styles were loaded from, and I could toggle them on and off
          and see their infuence on the element on the page. Insert mind blown with explosions meme here.
        </p>

        <p>
          Now you have a glimpse of the past let us look at an example of how much modern Javascript rocks. Granted it still has issues, I think it always will.
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
      <javascript_class_desc_003 />
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

export default {
  components: {
    javascript_class_desc_001,
    javascript_class_desc_002,
    javascript_class_desc_003
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

hr.gradient {
    border: 0;
    height: 1px;
    background-image: linear-gradient(to right, rgba(255, 255, 255, 0), rgba(255, 255, 255, 0.75), rgba(255, 255, 255, 0));
}
</style>
