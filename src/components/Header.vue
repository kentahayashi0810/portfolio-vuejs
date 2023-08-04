<script setup>
import { ref } from 'vue'
import { RouterLink } from 'vue-router'
const navOpen = ref(false)

const toggleNav = () => {
  navOpen.value = !navOpen.value
}
const closeNav = () => {
  if (navOpen.value) {
    navOpen.value = !navOpen.value
  }
}
</script>

<template>
  <header class="header" id="header">
    <div class="header__wrapper">
      <div class="header__logo"></div>
      <div class="header__bg" :class="{ active: navOpen }"></div>
      <nav class="header__globalNav" :class="{ active: navOpen }">
        <div class="header__list">
          <RouterLink class="header__listItem" to="/" @click="closeNav">Home</RouterLink>
          <RouterLink class="header__listItem" to="/about" @click="closeNav">About</RouterLink>
          <RouterLink class="header__listItem" to="/works" @click="closeNav">Works</RouterLink>
          <RouterLink class="header__listItem" to="/contact" @click="closeNav">Contact</RouterLink>

          <div class="header__language">
            <a href="">
              <figure class="header__language-icon">
                <img src="../../public/header_language_1.png" alt="English" />
              </figure>
            </a>
            <a href="">
              <figure class="header__language-icon">
                <img src="../../public/header_language_2.png" alt="日本語" />
              </figure>
            </a>
          </div>
        </div>
      </nav>
    </div>

    <button :class="{ active: navOpen }" class="header__hamburger -sp-only" @click="toggleNav">
      <span class="header__hamburger-line"></span>
      <span class="header__hamburger-line"></span>
      <span class="header__hamburger-line"></span>
    </button>
  </header>
</template>

<style scoped>
.header {
  position: fixed;
  z-index: 999;
  top: 0;
  left: 0;
  width: 100%;
  color: #ffffff;
  padding: 2rem 0;
  background-color: #394563;
  height: 70px;
}
.header .header__wrapper {
  max-width: 1440px;
  padding: 0 3rem;
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  justify-content: space-between;
  margin: 0 auto;
}
.header .header__bg {
  opacity: 0;
  visibility: hidden;
  transition: 0.5s;
  height: 100vh;
  position: absolute;
  width: 100%;
  top: 0;
  left: 0;
}
.header .header__bg.active {
  opacity: 1;
  visibility: visible;
  backdrop-filter: blur(5px);

  z-index: 50;
  transition: 0.5s;
}
@media only screen and (max-width: 899px) {
  .header .header__globalNav {
    transform: translateX(120%);
    background-color: #dce2ec;
    position: absolute;
    transition: 0.5s;
    top: 0;
    right: 0;
    height: 100vh;
    width: 80%;
  }
}
@media only screen and (max-width: 899px) {
  .header .header__globalNav.active {
    transition: 0.5s;
    transform: translateX(0%);
    z-index: 51;
  }
  .header .header__globalNav .header__listItem {
    color: #394563;
  }
}
.header .header__list {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  gap: 2rem;
}
@media only screen and (max-width: 899px) {
  .header .header__list {
    flex-direction: column;
    margin-top: 14rem;
    margin-left: 5rem;
  }
}
.header .header__listItem {
  font-size: 2rem;
  font-weight: 400;
  letter-spacing: 0.1em;
  line-height: 1.5;
}
.header .header__listItem:hover {
  border-bottom: #ffffff solid 1px;
}
@media only screen and (max-width: 899px) {
  .header .header__listItem {
    font-size: 3rem;
  }
}
.header .header__language {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
}
.header .header__language-icon {
  width: 30px;
  margin-right: 1rem;
  padding-top: 0.4rem;
}
@media only screen and (max-width: 899px) {
  .header .header__hamburger {
    position: absolute;
    width: 50px;
    height: 50px;
    z-index: 999;
    right: 20px;
    top: 10px;
  }
  .header .header__hamburger::before {
    position: absolute;
    display: inline-block;
    content: '';
    width: 90px;
    height: 70px;
    right: -20px;
    top: -10px;
  }
}
.header .header__hamburger-line {
  position: absolute;
  z-index: 10;
  display: block;
  width: 40px;
  height: 2px;
  background-color: #ffffff;
  border-radius: 2px;
  transition: 0.5s;
}
.header .header__hamburger-line:first-of-type {
  top: 8px;
}
.header .header__hamburger-line:nth-of-type(2) {
  top: 50%;
  transform: translateY(-50%);
}
.header .header__hamburger-line:last-of-type {
  bottom: 8px;
}
.header .header__hamburger.active .header__hamburger-line {
  background-color: #394563;
}
.header .header__hamburger.active .header__hamburger-line:first-of-type {
  transform: rotate(-45deg);
  top: 20px;
}
.header .header__hamburger.active .header__hamburger-line:nth-of-type(2) {
  opacity: 0;
}
.header .header__hamburger.active .header__hamburger-line:last-of-type {
  transform: rotate(45deg);
  bottom: auto;
  top: 20px;
}
</style>
