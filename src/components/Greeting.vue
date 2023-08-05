<script setup>
import { RouterLink } from 'vue-router'
import { ref, onMounted } from 'vue'

const windowHeight = ref(0)

windowHeight.value = document.documentElement.clientHeight + 'px'
</script>

<template>
  <section class="frontGreeting" :style="{ height: windowHeight }">
    <div class="inner">
      <div class="frontGreeting__box">
        <p class="frontGreeting__intro">Hi, My name is</p>
        <h2 class="frontGreeting__heading1">Kenta Hayashi.</h2>

        <h3 class="frontGreeting__heading2">I work with Passion.</h3>

        <p class="frontGreeting__text">I am a Front End Developer, and an Enthusiastic Learner.</p>

        <button class="frontGreeting__button">
          <RouterLink to="/works">Check Out My Works!</RouterLink>
        </button>
      </div>
    </div>
  </section>
</template>

<style scoped>
.frontGreeting {
  width: 100%;

  margin: 0 auto;
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding-top: 70px;
}
.frontGreeting .frontGreeting__box {
  max-width: 900px;
  margin: 0 auto;
}
.frontGreeting .frontGreeting__intro {
  font-size: 3rem;
  font-weight: 700;
  letter-spacing: 0.1em;
  color: #839db3;
}
@media only screen and (max-width: 899px) {
  .frontGreeting .frontGreeting__box {
    padding-top: 20%;
  }
  .frontGreeting .frontGreeting__intro {
    font-size: 2rem;
  }
}
.frontGreeting .frontGreeting__heading1,
.frontGreeting .frontGreeting__heading2 {
  font-size: 8rem;
  font-weight: 700;
  line-height: 1.5;
  letter-spacing: 0.05em;
}
@media only screen and (max-width: 899px) {
  .frontGreeting .frontGreeting__heading1,
  .frontGreeting .frontGreeting__heading2 {
    font-size: 9.5vw;
  }
}
.frontGreeting .frontGreeting__text {
  font-size: 2rem;
  margin-top: 6rem;
  font-weight: 700;
  letter-spacing: 0.1em;
}
@media only screen and (max-width: 899px) {
  .frontGreeting .frontGreeting__text {
    font-size: 1.6rem;
  }
}
.frontGreeting .frontGreeting__button {
  background-color: #dce2ec;
  font-size: 2.4rem;
  font-weight: 700;
  letter-spacing: 0.1em;
  text-align: center;
  padding: 1.6rem 2rem;
  border-radius: 10px;
  border: 2px solid #839db3;
  color: #234d4f;
  margin: 12rem 0 6rem;
  display: block;
  transition: 0.3s;
}
@media only screen and (max-width: 899px) {
  .frontGreeting .frontGreeting__button {
    font-size: 2rem;
    margin: 10rem auto 4rem;
  }
}
.frontGreeting .frontGreeting__button:hover {
  background-color: #394563;

  color: #dce2ec;
  border: 2px solid #dce2ec;
}
</style>
