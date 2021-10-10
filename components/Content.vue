<template>
    <!--content----------------->
    <div class="content mt-4">
      <!--model--------------->
      <div class="model">
        <img src="images/model.png" />
      </div>
      <!--text-------------->
      <div class="main-text">
        <h1 class="stagger1">Hello, I am Dayat</h1>
        <p class="hero-design">
          I am <b>Fullstack Developer</b> who had Website building from scratch by
          using modern <b>Frameworks</b> such as <b>Laravel, Node, CodeIgniter, YII,</b> etc as <b>Backend</b>,
          and have great <b>Frontend development skills</b> such as <b>Vue,
          Nuxt, React, Jquery, Javascript and so on</b>. I am open to learning
          new things that can help make a positive contribution to the Client I
          work for.
        </p>
        <!--btn------->
        <a href="#" class="portfolio-btn square-anim">See My Portfolio</a>
      </div>
    </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.model img {
  width: 100%;
  height: 100%;
  object-fit: contain;
}
.model {
  width: 500px;
  height: 500px;
}
.content {
  width: 90%;
  display: flex;
  justify-content: space-around;
  align-items: center;
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
}
.main-text {
  width: 500px;
}
.main-text h1 {
  font-size: 3.5rem;
  color: #1c3548;
  margin: 0px 0px 10px 0px;
  line-height: 60px;
}
.main-text p {
  color: #747474;
}
.portfolio-btn {
  width: 190px;
  height: 44px;
  display: flex;
  justify-content: center;
  align-items: center;
  color: #ffffff;
  background-color: #1db096;
  border-radius: 20px;
  box-shadow: 4px 10px 30px rgba(24, 139, 119, 0.2);
}
.portfolio-btn:hover {
  background-color: #23cdaf;
  transition: all ease 0.2s;
}
</style>
