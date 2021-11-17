<template>
  <section id="main">
    <nav>
      <!--logo--------------->
      <nuxt-link to="/" class="logo">
        <img src="images/logo.png" />
      </nuxt-link>
      <!--menu-btn-------------->
      <input class="menu-btn" type="checkbox" id="menu-btn" />
      <label class="menu-icon" for="menu-btn">
        <span class="nav-icon"></span>
      </label>
      <!--menu-------------->
      <ul class="menu">
        <li><nuxt-link to="#main">Home</nuxt-link></li>
        <li><nuxt-link to="#skills">Skills</nuxt-link></li>
        <li><nuxt-link to="#recent">Recent</nuxt-link></li>
        <li><nuxt-link to="#client">Client</nuxt-link></li>
        <li><nuxt-link to="#contact">Contact</nuxt-link></li>
      </ul>
      <!--say-hey--------->
      <nuxt-link to="#" class="hey">Hi Recruiter!</nuxt-link>
    </nav>
  </section>
</template>

<script>
export default {
  mounted() {
    // $(document).ready(function() {
    //   $(window).scroll(function() {
    //     var scroll = $(window).scrollTop();
    //     //>=, not <=
    //     if (scroll >= 70) {
    //       //clearHeader, not clearheader - caps H
    //       // var navbar = document.getElementsByTagName("nav");
    //       $("nav").addClass("sticked");
    //     } else {
    //       $("nav").removeClass("sticked");
    //     }
    //   }); //missing );
    // });
  }
};
</script>

<style lang="scss" scoped>
#main {
  width: 100%;
  height: 100vh;
  position: relative;
}
nav {
  display: flex;
  justify-content: space-around;
  align-items: center;
  box-shadow: 5px 10px 30px rgba(0, 0, 0, 0.02);
  // position: fixed;
  left: 0;
  transition: 0.6s;
  padding: 20px 0;
  top: 0;
  width: 100%;
  z-index: 1;
  background-color: transparent;
}
.logo img {
  height: 45px;
}

.menu {
  margin-bottom: 0;
}
nav ul li a {
  height: 40px;
  line-height: 43px;
  margin: 3px;
  padding: 0px 22px;
  display: flex;
  font-size: 0.8rem;
  text-transform: uppercase;
  font-weight: 900;
  color: #585b5b;
  letter-spacing: 1px;
}
.hey {
  color: #39bfbd;
  font-weight: 500;
  font-size: 0.9rem;
  border-bottom: 2px solid #40c6c4;
}
nav ul li a:hover {
  background-color: #2adabc;
  color: #ffffff;
  box-shadow: 5px 10px 30px rgba(64, 198, 196, 0.3);
  transition: all ease 0.5s;
}
</style>
