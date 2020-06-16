<template>
  <footer>
    <div class='footer_spacer_test center'>
      <div class='row'>
        <div class='col l4 m12 s12'>
          <span class='emphasis'>EXPLORE</span><br/><br/>
          <nuxt-link :to='{name: "index"}'>Home <i class="material-icons small">keyboard_arrow_right</i></nuxt-link><br/>
          <nuxt-link :to='{name: "about"}'>About <i class="material-icons small">keyboard_arrow_right</i></nuxt-link></br/>
          <nuxt-link :to='{name: "javascript"}'>Javascript <i class="material-icons small">keyboard_arrow_right</i></nuxt-link><br/>
          <nuxt-link :to='{name: "content_creation"}'>Content Creation <i class="material-icons small">keyboard_arrow_right</i></nuxt-link><br/>
          <nuxt-link :to='{name: "build"}'>Site Build <i class="material-icons small">keyboard_arrow_right</i></nuxt-link><br/>
          <nuxt-link :to='{name: "personal_projects"}'>Projects <i class="material-icons small">keyboard_arrow_right</i></nuxt-link><br/>
        </div>
        <div class='col l4 m12 s12'>
          <address>
            Roger Atkins<br/>
            PHONE: 0429232307<br/>
            EMAIL: <a href="mailto:chorazin@gmail.com">chorazin@gmail.com</a>
          </address>
        </div>
        <div class='col l4 m12 s12'>
          stuff over here
        </div>
      </div>
      <div class='row center'>
        <div class='col l12 m12 s12 emphasis'>DEV-WEB-DESIGN NEWCASTLE AUSTRALIA</div>
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
footer {
  display:inline;
  pointer-events: all;
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
  padding-top: 30px;
}
.row {
  margin-bottom: 0px;
}
.emphasis {
  font-size: 20px;
  font-weight: bold;
  border: 0px;
  border-top: 1px;
  border-style: solid;
}
.small {
  position: absolute;
  margin-top: -4px;
}
</style>
