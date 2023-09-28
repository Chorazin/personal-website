<template>
  <div class='home'>
    <div class='row quotes hide-on-small-only'>
      <div class='col s4'></div>
      <div class='col s4'>
        <transition name='slide_one' appear>
          <div class='lobs width_400' v-if='show'>
            {{sorted_array.quote}}
            <div class='center-align'>- {{sorted_array.author}}</div>
          </div>
        </transition>
      </div>
      <div class='col s4'></div>
    </div>
    <img class='responsive-img hide-on-small-only' src='~/assets/splash_v003.jpg' alt='picture of Roger Atkins, website author'>
    <img class='responsive-img hide-on-med-and-up' src='~/assets/logo_v001.jpg' alt='small web development RA logo'>
    <middle_links />
    <parallax_comp v-bind:parallax_info='parallax_info_3' class='hide-on-small-only'/>
  </div>
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
      title: 'Web Development Newcastle Australia',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'Web Dev-Design - Roger Atkins'
        }
      ]
    }
  },

  data() {
    return {
      sorted_array: [],
      quotations: [
        {quote:'"If you\'re already a front-end developer, well, pretend you\'re also wearing a pirate hat"', author: 'Ethan Marcotte'},
        {quote: '"Digital design is like painting, except the paint never dries"', author: 'Neville Brody'},
        {quote: '"Intuitive design is how we give the user new superpowers"', author: 'Jared Spool'},
        {quote: '"Always code as if the person who ends up maintaining your code will be a violent psychopath who knows where you live"', author: 'John Woods'},
        {quote: '"Give a man a program, frustrate him for a day. Teach a man to program, frustrate him for a lifetime."', author: 'Muhammad Waseem'},
        {quote: '"I quickly came to realise code is a superpower"', author: 'Karlie Kloss'},
        {quote: '"One man\'s crappy software is another man\'s full time job"', author: 'Jessica Gaston'},
        {quote: '"If debugging is the process of removing software bugs, then programming must be the process of putting them in"', author: 'Edsger Dijkstra'}
      ],

      show: false,

      parallax_info_3: {
        url: '/parallax_v002.jpg',
        heading: null,
        quote: null
      }
    }
  },

  mounted() {
    //generate a random number based on the length of the quotations array and grab a quote on component mount
    const generate_number = (max) => {
      return Math.floor(Math.random() * Math.floor(max));
    }
    const stored_number = generate_number(this.quotations.length);
    this.sorted_array = this.quotations[stored_number]


    //setup materialize parallex on component mount
    const elems = document.querySelectorAll('.parallax');
    const instances = M.Parallax.init(elems);

    //setup for text animation on mount, this is not default with vue animations
    this.show = true;
  }
}
</script>

<style scoped>
/*VISUAL STYLES ---------------------*/
/*note inherited core CSS from default.vue*/
.slide_one-enter-active {
  transition: opacity 0.5s ease-in-out, transform 0.5s ease;
}

.slide_one-enter-active {
  transition-delay: 0.5s;
}

.slide_one-enter {
  opacity: 0;
  transform: translateY(-100px);
}

.slide_one-to {
  opacity: 1;
  transform: translateY(0px);
}

.fade-enter-active, .fade-leave-active {
  transition-duration: 0.5s;
  transition-property: opacity;
  transition-timing-function: ease;
}

.fade-enter, .fade-leave-active {
  opacity: 0
}

.home .lobs {
  font-family: "lobster";
  font-size: 20px;
  color: white;
}


/*LAYOUT STYLES --------------------*/
.home .width_400 {
  width: 400px;
}

.home section {
  margin-top: 100px;
  margin-bottom: 100px;
}

.home .quotes {
  width: 100%;
  position: absolute;
  top: 300px;
  height: 400px;
}

.home .spacer {
  margin-top: 75px
}



/*media queries layout adjustment for mobile positioning*/
@media only screen and (max-width: 1200px) {
  .quotes {
  top: 170px;
  }
  .lobs {
  font-size: 12pt;
  width: 300px;
  }
}


@media only screen and (max-width: 700px) {
  .quotes {
  top: 90px;
  }
  .lobs {
  font-size: 10pt;
  width: 200px;
  }
}
</style>
