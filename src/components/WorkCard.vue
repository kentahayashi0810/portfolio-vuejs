<script setup>
defineProps({
  work: {
    type: Object,
    required: true
  }
})
</script>

<template>
  <li class="frontWorks__flexItem js-fadein-ready">
    <a href="">
      <h4 class="frontWorks__flexItem-title">{{ work.title }}</h4>

      <figure class="frontWorks__flexItem-image">
        <div class="frontWorks__imageWrap"></div>
        <img :src="work.image" :alt="work.imgDesc" />
      </figure>

      <dl class="frontWorks__table">
        <dt>Tools I used:</dt>
        <dd>
          <span v-for="tool in work.usedTools">{{ tool }}</span>
        </dd>
        <dt>Pages I coded:</dt>
        <dd>{{ work.pageCoded }}</dd>
        <dt>Features:</dt>
        <dd>
          <span v-for="feature in work.features">{{ feature }}</span>
        </dd>
      </dl>
    </a>
  </li>
</template>

<style scoped>
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
