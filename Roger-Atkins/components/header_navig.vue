<template>
  <header class='header grey-text lighten-4'>
    <div class='navbar-fixed'>
      <nav>
        <div class='nav-wrapper'>

          <a href="#" data-target="mobile-demo" class="sidenav-trigger"><i class="material-icons">menu</i></a>
          <ul id="nav-mobile" class="right hide-on-med-and-down">
            <li class='center'><nuxt-link to='/'><i class="material-icons icon_grey">home</i></nuxt-link></li>
            <li class='center'><nuxt-link to='/about'><i class="material-icons  icon_grey">info</i></nuxt-link></li>
            <li class='center'><nuxt-link to='/javascript'><img src='../assets/js_v001.jpg' class='responsive-img'></nuxt-link></li>
          </ul>
        </div>
      </nav>
    </div>
    <ul class="sidenav" id="mobile-demo">
      <li><nuxt-link :to='{name: "index"}'>Home</nuxt-link></li>
      <li><nuxt-link :to='{name: "about"}'>About</nuxt-link></li>
      <li><nuxt-link :to='{name: "javascript"}'>Javascript</nuxt-link></li>
    </ul>
  </header>
</template>

<script>
export default {
  name: 'header_navig',

  mounted() {
    //set up the materialize slide in menu on component mount
    const elems = document.querySelectorAll('.sidenav');
    const instances = M.Sidenav.init(elems);
    //get the materialize instance of the side nav and set a listener to close when a link is clicked
    const link_array = document.querySelectorAll(".sidenav > li");
    link_array.forEach(link => {
      link.addEventListener('click', () => {
        const elem = document.querySelector(".sidenav");
        const instance = M.Sidenav.getInstance(elem);
        instance.close();
      })
    })





  }
}
</script>

<style scoped>
nav {
  background-color: #000000;
}
nav ul a:hover {
  background-color: rgba(255, 255, 255, 0.2);
}
.header a {
  width: 8rem;
}

.icon_grey {
  color: #9e9e9e;
}

/*.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 1rem;
  border-bottom: 1px dotted #CCCCCC;
}

.header .title {
  font-size: 3rem;
}


.header ul {
  display: flex;
}

.header a {
  display: inline-block;
  background: #000000;
  padding: 0.3rem 1rem;
  margin-right: 0.5rem;
  color: #9e9e9e;
}
*/
</style>
