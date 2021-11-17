<template>
  <section id="skills" class="mt-4">
    <!--text--------->
    <div class="skill-text">
      <!--heading-->
      <div class="skill-heading">
        <span class="transition2">My Skills</span>
        <h2 class="transition2">My Experties</h2>
      </div>
      <!--skill-box-container----------->
      <div class="s-box-container">
        <!--skill-box-------------->
        <div class="skill-box transition2">
          <!--icon------->
          <div class="s-box-icon" style="color: red">
            <font-awesome-icon :icon="['fas', 'code']" />
          </div>
          <!--skill-box-text--------->
          <div class="s-box-text">
            <strong>Web Developer</strong>
            <p>
              Frontend using modern framework such as
              <b>Vue, Nuxt, React, Bootstrap and Vuetify</b>
            </p>
            <p>
              Backend using modern framework such as
              <b>Laravel, CodeIgniter and Express</b>
            </p>
            <p>
              Third party API integration such as
              <b
                >Stripe, Paypal, Bookey, OAuth Social Media, Twilio, Pusher,
                Agora, ETC</b
              >
            </p>
          </div>
        </div>
        <!--skill-box-------------->
        <div class="skill-box transition2">
          <!--icon------->
          <div class="s-box-icon" style="color: blue">
            <font-awesome-icon :icon="['fas', 'brain']" />
          </div>
          <!--skill-box-text--------->
          <div class="s-box-text">
            <strong>Artificial Intelligence (AI)</strong>
            <p>
              Build AI using <b>Python, Anaconda</b> with
              <b>Tensorflow Object Detection or YOLO</b>
            </p>
          </div>
        </div>
        <!--skill-box-------------->
        <div class="skill-box transition2">
          <!--icon------->
          <div class="s-box-icon" style="color: green">
            <font-awesome-icon :icon="['fas', 'server']" />
          </div>
          <!--skill-box-text--------->
          <div class="s-box-text">
            <strong>Server</strong>
            <p>
              Maintenance server such as <b>VPS, Shared server</b> and shipping
              using <b>Container like Docker</b>
            </p>
          </div>
        </div>
      </div>
    </div>
    <!--img--------------->
    <div class="skill-img transition2">
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
  display: flex;
  align-items: center;
}
.skill-img img {
  width: 100%;
  object-fit: contain;
  margin-top: 114px;
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
  line-height: 1;
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
  margin: 10px 0px;
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
  line-height: 1;
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
