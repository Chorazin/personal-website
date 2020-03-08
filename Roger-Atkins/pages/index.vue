<template>
  <div>
    <!-- nav componenet here -->
    <div>
      <div class='row quotes hide-on-small-only'>
        <div class='col s4'></div>
        <div class='col s4'>
          <div class='lobs'>
          {{sorted_array.quote}}
            <div class='center-align'>- {{sorted_array.author}}</div>
          </div>
        </div>
        <div class='col s4'></div>
      </div>
      <img class='responsive-img hide-on-small-only' src='~/assets/splash_v003.jpg'>
      <img class='responsive-img hide-on-med-and-up' src='~/assets/logo_v001.jpg'>
    </div>
    <section>
      <div class='container row icon_section grey-text lighten-4 center-align'>
        <div class='col m4 s12'><i class="material-icons">donut_small</i></div>
        <div class='col m4 s12'><i class="material-icons">airplay</i></div>
        <div class='col m4 s12'><i class="material-icons">cloud_circle</i></div>
      </div>
    </section>
    <parallax_comp v-bind:parallax_info_3='parallax_info_3'/>

    <div class='container row icon_section grey-text lighten-4 center-align'>
      <div class='col s4'><i class="material-icons expand">donut_small</i></div>
      <div class='col s4'><i class="material-icons">airplay</i></div>
      <div class='col s4'><i class="material-icons">cloud_circle</i></div>
    </div>
  </div>
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
      title: 'Web Development Newcastle Australia',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'Roger Atkins Web-Dev-Design'
        }
      ]
    }
  },

  data() {
    return {
      sorted_array: [],
      quotations: [
        {quote:'"If youre already a front-end developer, well, pretend youre also wearing a pirate hat"', author: 'Ethan Marcotte'},
        {quote: '"Digital design is like painting, except the paint never dries"', author: 'Neville Brody'},
        {quote: '"Intuitive design is how we give the user new superpowers"', author: 'Jared Spool'},
        {quote: '"Always code as if the person who ends up maintaining your code will be a violent psychopath who knows where you live"', author: 'John Woods'},
        {quote: '"Give a man a program, frustrate him for a day. Teach a man to program, frustrate him for a lifetime."', author: 'Muhammad Waseem'}
      ],

      parallax_info_3: {
        url: '/parallax_v002.jpg',
        heading_2:'AMAZING'
      }
    }
  },

  mounted() {
    //generate a randum number based on the length of the quotations array and grab a quote on component mount
    const generate_number = (max) => {
      return Math.floor(Math.random() * Math.floor(max));
    }
    const stored_number = generate_number(this.quotations.length);
    this.sorted_array = this.quotations[stored_number]


    //setup materialize parallex on component mount
    const elems = document.querySelectorAll('.parallax');
    const instances = M.Parallax.init(elems);

  }
}
</script>


<style scoped>
.material-icons{
   font-size: 48px;
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

.icon_section {
  font-family: "roboto";

}

.lobs {
  font-family: "lobster";
  width: 400px;
  font-size: 20px;
}


section {
  padding-top: 100px;
  padding-bottom: 100px;

}
.quotes {
  color: white;
  width: 100%;
  position: absolute;
  top: 300px;
  height: 400px;
}

/*media queries for mobile positioning adjustment*/
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
