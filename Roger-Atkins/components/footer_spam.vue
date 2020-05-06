<template>
  <footer>
    <div class='footer_spacer_test center'>
      <div class='row spacer'>
        <div class='col l4 m12 s12'>
          <span class='emphasis'>EXPLORE</span><br/><br/>

          <nuxt-link :to='{name: "index"}'>Home</nuxt-link><br/>
          <nuxt-link :to='{name: "about"}'>About</nuxt-link></br/>
          <nuxt-link :to='{name: "javascript"}'>Javascript</nuxt-link><br/>
          Content Creation <br/>
        </div>
        <div class='col l4 m12 s12'>
          <address>
            Roger Atkins<br/>
            PHONE: 0429232307<br/>
            EMAIL: <a href="mailto:chorazin@gmail.com">chorazin@gmail.com</a>
          </address>
        </div>
        <div class='col l4 m12 s12'>


        </div>
      </div>
      <div class='row center'>
        <div class='col l12 m12 s12 emphasis'>DEV-WEB-DESIGN CRAFTED WITH <i class="material-icons">favorite</i> NEWCASTLE AUSTRALIA</div>
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
  margin-bottom: 0px;
  height: 300px;
  background-image: url('../assets/gradient_backdrop_v002.png');
  background-repeat: repeat-x;
  background-color: #000000;
  position: sticky;
  bottom: 0px;
  z-index: -5;
}
.material-icons {
  font-size: 18px;
}
.emphasis {
  font-size: 20px;
  font-weight: bold;
}

.spacer {
  padding-top: 50px;
}
</style>
