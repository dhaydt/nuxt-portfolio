<template>
  <section id="skills">
    <!--text--------->
    <div class="skill-text">
      <!--heading-->
      <div class="skill-heading">
        <span>My Skills</span>
        <h2>My Experties</h2>
      </div>
      <!--skill-box-container----------->
      <div class="s-box-container">
        <!--skill-box-------------->
        <div class="skill-box">
          <!--icon------->
          <div class="s-box-icon">
            <font-awesome-icon :icon="['fab', 'html5']" />
          </div>
          <!--skill-box-text--------->
          <div class="s-box-text">
            <strong>Python</strong>
            <p>
              I have some experience in Augmented Intelegen with Python and i
              completed some project.
            </p>
          </div>
        </div>
        <!--skill-box-------------->
        <div class="skill-box">
          <!--icon------->
          <div class="s-box-icon">
            <font-awesome-icon :icon="['fab', 'css3-alt']" />
          </div>
          <!--skill-box-text--------->
          <div class="s-box-text">
            <strong>PHP</strong>
            <p>
              I have 1 years experience in PHP Framework such as Laravel and i
              completed some project.
            </p>
          </div>
        </div>
        <!--skill-box-------------->
        <div class="skill-box">
          <!--icon------->
          <div class="s-box-icon">
            <font-awesome-icon :icon="['fab', 'js-square']" />
          </div>
          <!--skill-box-text--------->
          <div class="s-box-text">
            <strong>JavaScript(Js)</strong>
            <p>
              I have 3 years experience in JavaScript and i completed 100+ Js
              project.
            </p>
          </div>
        </div>
      </div>
    </div>
    <!--img--------------->
    <div class="skill-img">
      <img src="images/skill2.png" />
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
#skills {
  display: flex;
  justify-content: space-around;
  align-items: center;
  width: 90%;
  margin: auto auto 50px auto;
}
.skill-text {
  width: 400px;
}
.skill-img {
  width: 600px;
  height: 600px;
}
.skill-img img {
  width: 100%;
  height: 100%;
  object-fit: contain;
}
.skill-heading span {
  color: #36b7b5;
  font-weight: 500;
  text-transform: uppercase;
  letter-spacing: 1px;
  font-size: 1rem;
}
.skill-heading h2 {
  color: #1c3548;
  font-size: 3.3rem;
  margin: 0px;
  font-weight: 400;
  letter-spacing: 1px;
}
.s-box-container {
  margin-top: 30px;
}
.skill-box {
  display: flex;
  margin: 25px 0px;
}
.s-box-icon {
  margin-right: 12px;
}
.s-box-icon svg {
  width: 40px;
  height: 40px;
  border-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #f0f0f0;
  font-size: 1.1rem;
}
.s-box-text strong {
  color: #1c3548;
  margin: 0px;
  font-size: 0.9rem;
  font-weight: 600;
}
.s-box-text p {
  color: #747474;
  font-size: 0.9rem;
}
.fa-html5 {
  color: #e06061;
}
.fa-css3-alt {
  color: #416cdf;
}
.fa-js-square {
  color: #f98231;
}
</style>
