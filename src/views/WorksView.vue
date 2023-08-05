<script setup>
import { ref, onMounted } from 'vue'
import axios from 'axios'
import WorkCard from '../components/WorkCard.vue'

const works = ref(null)

onMounted(() => {
  axios
    .get('https://my-json-server.typicode.com/kentahayashi0810/my-works-api/works')
    .then((response) => {
      works.value = response.data
    })
    .catch((errro) => console.log(error))
})
</script>

<template>
  <section class="frontWorks" id="frontWorks">
    <div class="inner">
      <h3 class="frontWorks__heading js-fadein-ready">WORKS</h3>
      <p class="frontWorks__description js-fadein-ready">
        Here is a collection of websites / projects I have worked on.
      </p>

      <ul v-if="works" class="frontWorks__flexbox">
        <WorkCard v-for="work in works" :work="work"></WorkCard>
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
</style>
