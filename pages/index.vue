<template>
  <div>
    <section id="landing">
      <Navbar></Navbar>
      <Content></Content>
    </section>
    <Skills></Skills>
    <Recent></Recent>
    <Client></Client>
    <Footer></Footer>
  </div>
</template>

<script>
import Footer from "../components/Footer";
import Client from "../components/Client";
import Recent from "../components/Recent";
import Skills from "../components/Skills";
import Content from "../components/Content";
import Navbar from "../components/Navbar";
export default {
  head() {
    return {
      script: [
        {
          src: "https://cdnjs.cloudflare.com/ajax/libs/gsap/3.5.1/gsap.min.js"
        },
        {
          src:
            "https://s3-us-west-2.amazonaws.com/s.cdpn.io/16327/ScrollTrigger.min.js"
        }
      ]
    };
  },
  components: {
    Footer,
    Client,
    Recent,
    Skills,
    Content,
    Navbar
  },

  mounted() {
    window.addEventListener("scroll", function() {
      var header = this.document.querySelector("nav");
      header.classList.toggle("sticked", window.scrollY > 0);
    });

    gsap.registerPlugin(ScrollTrigger);
    var tl = gsap.timeline();

    tl.from(".content", {
      y: "-30%",
      opacity: 0,
      duration: 2,
      ease: Power4.easeOut
    });
    tl.from(
      ".stagger1",
      {
        opacity: 0,
        y: -50,
        stagger: 0.3,
        ease: Power4.easeOut,
        duration: 2
      },
      "-=1.5"
    );
    tl.from(
      ".hero-design",
      {
        opacity: 0,
        y: 50,
        ease: Power4.easeOut,
        duration: 1
      },
      "-=2"
    );

    gsap.from(".square-anim", {
      stagger: 0.2,
      scale: 0.1,
      duration: 1,
      ease: Back.easeOut.config(1.7)
    });

    gsap.from(".transition2", {
      scrollTrigger: {
        trigger: ".transition2",
        start: "top bottom"
      },
      y: 50,
      opacity: 0,
      duration: 1.2,
      stagger: 0.3
    });

    gsap.from(".transition3", {
      scrollTrigger: {
        trigger: ".transition3",
        start: "top center"
      },
      y: 50,
      opacity: 0,
      duration: 1.2,
      stagger: 0.6
    });
  }
};
</script>

<style lang="scss">
@charset "utf-8";
:root {
  font-size: 20px;
}
/* CSS Document */
body {
  margin: 0px;
  padding: 0px;
  font-family: "Patrick Hand", cursive;
}
* {
  box-sizing: border-box;
  scroll-behavior: smooth;
  line-height: 1.3;
  p {
    margin-bottom: 0.5rem;
  }
}
ul {
  list-style: none;
}
a {
  text-decoration: none;
}
#landing {
  background-color: #e6f4f5;
}

nav.sticked {
  padding: 10px 50px;
  background-color: #ffffffb9;
}
nav .menu-btn,
.menu-icon {
  display: none;
}

nav ul {
  display: flex;
}
@media (max-width: 1140px) {
  .content {
    width: 100%;
  }
  .model {
    width: 400px;
    height: 400px;
  }
  .main-text,
  .model {
    margin: 10px;
  }
  .main-text h1 {
    font-size: 3rem;
  }
  .skill-img {
    width: 400px;
    height: 400px;
  }
  .client-box {
    flex-grow: 0.5;
  }
}
@media (max-width: 900px) {
  .menu-icon {
    display: block;
  }
  nav {
    justify-content: space-between;
    height: 65px;
    padding: 0px 30px;
  }
  .logo img {
    height: 35px;
  }
  .menu {
    display: none;
    position: absolute;
    top: 65px;
    left: 0px;
    background-color: #ffffff;
    border-bottom: 4px solid #1db096;
    width: 100%;
    padding: 0px;
    margin: 0px;
  }
  .menu li {
    width: 100%;
  }
  nav .menu li a {
    width: 100%;
    height: 40px;
    justify-content: center;
    align-items: center;
    margin: 0px;
    padding: 25px;
    border: 1px solid rgba(38, 38, 38, 0.03);
  }
  nav .menu-icon {
    cursor: pointer;
    float: right;
    padding: 28px 20px;
    position: relative;
    user-select: none;
  }
  nav .menu-icon .nav-icon {
    background-color: #333333;
    display: block;
    height: 2px;
    position: relative;
    transition: background 0.2s ease-out;
    width: 18px;
  }
  nav .menu-icon .nav-icon:before,
  nav .menu-icon .nav-icon:after {
    background: #333;
    content: "";
    display: block;
    height: 100%;
    position: absolute;
    transition: all ease-out 0.2s;
    width: 100%;
  }
  nav .menu-icon .nav-icon:before {
    top: 5px;
  }
  nav .menu-icon .nav-icon:after {
    top: -5px;
  }
  nav .menu-btn:checked ~ .menu-icon .nav-icon {
    background: transparent;
  }
  nav .menu-btn:checked ~ .menu-icon .nav-icon:before {
    transform: rotate(-45deg);
    top: 0;
  }
  nav .menu-btn:checked ~ .menu-icon .nav-icon:after {
    transform: rotate(45deg);
    top: 0;
  }
  nav .menu-btn {
    display: none;
  }
  nav .menu-btn:checked ~ .menu {
    display: block;
  }
  #skills {
    width: 100%;
    justify-content: space-between;
    padding-left: 40px;
  }
  .skill-text {
    width: 400px;
  }
  .skill-img {
    width: 40%;
    height: 300px;
  }
  .skill-img img {
    object-fit: cover;
    object-position: left;
  }
  .recent-heading h3,
  .client-heading h3,
  #contact h3 {
    font-size: 2.2rem;
    text-align: center;
  }
  .recent-heading {
    text-align: center;
    padding: 0px 15px;
  }
}
@media (max-width: 720px) {
  .model {
    display: none;
  }
  .main-text {
    width: 70%;
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
  }
  #contact img {
    height: 200px;
  }
  footer {
    justify-content: center;
    padding: 10px 20px;
  }
  footer p {
    text-align: center;
  }
  .recent-btn {
    margin: 0px;
  }
}
@media (max-width: 530px) {
  .contact-input {
    width: 90%;
  }
  .skill-img {
    display: none;
  }
  .skill-text {
    width: 85%;
  }
  #skills {
    margin: 0px;
  }
}
</style>
