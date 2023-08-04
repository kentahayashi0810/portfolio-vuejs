<script setup></script>

<template>
  <section class="frontWorks" id="frontWorks">
    <div class="inner">
      <h3 class="frontWorks__heading js-fadein-ready">WORKS</h3>
      <p class="frontWorks__description js-fadein-ready">
        Here is a collection of websites / projects I have worked on.
      </p>

      <ul class="frontWorks__flexbox">
        <li class="frontWorks__flexItem js-fadein-ready">
          <a href="">
            <h4 class="frontWorks__flexItem-title"></h4>

            <figure class="frontWorks__flexItem-image">
              <div class="frontWorks__imageWrap"></div>
              <img src="" alt="" />
            </figure>

            <dl class="frontWorks__table">
              <dt>Tools I used:</dt>
              <dd></dd>
              <dt>Pages I coded:</dt>
              <dd></dd>
              <dt>Features:</dt>
              <dd></dd>
            </dl>
          </a>
        </li>
      </ul>
    </div>
  </section>
</template>

<style scoped>
.frontWorks {
  background-color: #f7f6f4;
  padding: 10rem 0 6rem;
}
.frontWorks .frontWorks__heading {
  color: #394563;
  font-size: 5rem;
  font-weight: 700;
  letter-spacing: 0.1em;
  text-align: center;
  margin-bottom: 1rem;
  position: relative;
}
.frontWorks .frontWorks__heading::before {
  position: absolute;
  content: '';
  left: 50%;
  top: 100px;
  transform: translateX(-50%);
  display: inline-block;
  height: 5px;
  width: 50px;
  border-radius: 5px;
  background-color: #394563;
}
.frontWorks .frontWorks__description {
  font-size: 2.8rem;
  font-weight: 400;
  letter-spacing: 0.1em;
  line-height: 1.5;
  margin: 0 auto;
  color: #333;
  max-width: 800px;
  margin-top: 5rem;
}
@media only screen and (max-width: 899px) {
  .frontWorks .frontWorks__description {
    font-size: 1.8rem;
  }
}
.frontWorks .frontWorks__flexbox {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  flex-wrap: wrap;
}
.frontWorks .frontWorks__flexItem {
  padding: 8rem 10rem;
  width: 100%;
  max-width: 800px;
  margin: 6rem auto 0;
  background-color: #ffffff;
  border-radius: 10px;
  box-shadow: 5px 5px 10px rgba(51, 51, 51, 0.4);
}
@media only screen and (max-width: 899px) {
  .frontWorks .frontWorks__flexItem {
    padding: 4rem 1.6rem;
  }
}
.frontWorks .frontWorks__flexItem-title {
  color: #394563;
  font-size: 4rem;
  font-weight: 700;
  margin: 2rem 0;
}
@media only screen and (max-width: 899px) {
  .frontWorks .frontWorks__flexItem-title {
    max-width: 600px;
    margin: 2rem auto;
    font-size: 2.8rem;
  }
}
.frontWorks .frontWorks__flexItem-image {
  position: relative;
  max-width: 800px;
  margin: 0 auto 3rem;
}
.frontWorks .frontWorks__flexItem-image img {
  width: 100%;
  object-fit: cover;
  object-position: top;
}
@media only screen and (max-width: 899px) {
  .frontWorks .frontWorks__flexItem-image {
    max-width: 600px;
  }
}
.frontWorks .frontWorks__imageWrap {
  position: absolute;
  z-index: 100;
  height: 100%;
  width: 100%;
  top: 0;
  left: 0;
  transition: 0.3s;
}
.frontWorks .frontWorks__imageWrap:hover {
  background-color: rgba(255, 255, 255, 0.4);
}
.frontWorks .frontWorks__table {
  color: #333;
  font-size: 2rem;
  max-width: 800px;
  margin: 0 auto;
}
.frontWorks .frontWorks__table dt {
  margin-top: 2rem;
}
@media only screen and (max-width: 899px) {
  .frontWorks .frontWorks__table {
    max-width: 600px;
    font-size: 1.6rem;
  }
}
</style>
