<template>
  <footer>
    <div class='footer_spacer_test center padding_thirty'>
      <div class='row_zero_margin row'>
        <div class='col l4 m12 s12 mobile_spacer events'>
          <span class='emphasis'>EXPLORE</span><br/><br/>
          <nuxt-link :to='{name: "index"}'>Home <i class="material-icons small">keyboard_arrow_right</i></nuxt-link><br/>
          <nuxt-link :to='{name: "about"}'>About <i class="material-icons small">keyboard_arrow_right</i></nuxt-link></br/>
          <nuxt-link :to='{name: "javascript"}'>Javascript <i class="material-icons small">keyboard_arrow_right</i></nuxt-link><br/>
          <nuxt-link :to='{name: "content_creation"}'>Content Creation <i class="material-icons small">keyboard_arrow_right</i></nuxt-link><br/>
          <nuxt-link :to='{name: "build"}'>Site Build <i class="material-icons small">keyboard_arrow_right</i></nuxt-link><br/>
          <nuxt-link :to='{name: "personal_projects"}'>Projects <i class="material-icons small">keyboard_arrow_right</i></nuxt-link><br/>
        </div>
        <div class='col l4 m12 s12 mobile_spacer events'>
          <span class='emphasis'>CONTACT</span><br/><br/>
          <address>
            Roger Atkins<br/>
            PHONE: 0434593655<br/>
            EMAIL: <a href="mailto:chorazin@gmail.com">chorazin@gmail.com</a><br/>
            LOCATION: Hamilton 2303, Newcastle, Australia
          </address>
        </div>
        <div class='col l4 m12 s12 events'>
          <span class='emphasis'>FOR THE BOTS</span><br/><br/>
          <a href='sitemap.xml'>sitemap</a>
        </div>
      </div>
      <div class='row_zero_margin row center'>
        <div class='col l12 m12 s12 footer_spiel margin_top_thirty'>DEV-WEB-DESIGN NEWCASTLE AUSTRALIA</div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'footer_spam',

}
</script>

<style scoped>
/*VISUAL STYLES ---------------------*/
/*note inherited core CSS from default.vue*/
footer {
  display:inline;
}
address {
  font-style: normal;
}
.footer_spacer_test {
  height: 300px;
  background-image: url('../assets/gradient_backdrop_v002.png');
  background-repeat: repeat-x;
  background-color: #000000;
  position: sticky;
  bottom: 0px;
  z-index: -5;
}

.emphasis {
  font-size: 20px;
  font-weight: bold;
  border: 0px;
  border-top: 1px;
  border-style: solid;

}
.footer_spiel {
  font-size: 10px;
  border: 0px;
  border-top: 1px;
  border-style: solid;
}
.events {
    pointer-events: auto;
}
/*LAYOUT STYLES --------------------*/
/*see default.vue */


@media only screen and (max-width: 700px) {
  .mobile_spacer {
    margin-bottom: 100px;
  }
}

</style>
