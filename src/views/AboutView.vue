<template>
  <section class="frontAbout" id="frontAbout">
    <div class="inner">
      <div class="frontAbout__wrap">
        <h3 class="frontAbout__heading js-fadein-ready">About Me</h3>

        <div class="frontAbout__box1">
          <h4 class="frontAbout__title js-fadein-ready">How Did it Start?</h4>
          <div class="frontAbout__flexBox1">
            <div class="frontAbout__textBox">
              <p class="frontAbout__text js-fadein-ready">
                My journey as a web developer started when I dropped out of my first university. I
                had no idea about what I would like for my job. Then, at my second university, I
                started taking online basic web development courses on HTML, CSS, Javascript,
                JQuery. I fell in love with it instantly. As a person with lots of curiosity and
                creativity, I figured that it was perfect for me.
              </p>
            </div>

            <div class="frontAbout__skills">
              <h4 class="frontAbout__skills-title js-fadein-ready">SKILLS ACQUIRED</h4>
              <ul class="frontAbout__list js-fadein-ready">
                <li class="frontAbout__listItem">HTML</li>
                <li class="frontAbout__listItem">CSS</li>
                <li class="frontAbout__listItem">Javascript</li>
                <li class="frontAbout__listItem">JQuery</li>
              </ul>
            </div>
          </div>

          <div class="frontAbout__flexBox1">
            <div class="frontAbout__textBox">
              <p class="frontAbout__text js-fadein-ready">
                After finishing the online courses, I started my internship with CLANE.inc, a web
                design company based in Japan. Struggling and also having lots of fun with the tasks
                given, I finished the internship with confidence and gained more hard skills such as
                SCSS, PHP for wordpress as well as the experience of working on a project in a team.
              </p>
            </div>

            <div class="frontAbout__skills">
              <h4 class="frontAbout__skills-title js-fadein-ready">SKILLS ACQUIRED</h4>
              <ul class="frontAbout__list js-fadein-ready">
                <li class="frontAbout__listItem">SCSS</li>
                <li class="frontAbout__listItem">WordPress</li>
                <li class="frontAbout__listItem">PHP</li>
              </ul>
            </div>
          </div>
        </div>

        <div class="frontAbout__box2">
          <h4 class="frontAbout__title js-fadein-ready">How about Soft Skills?</h4>
          <div class="frontAbout__flexBox1">
            <div class="frontAbout__textBox">
              <p class="frontAbout__text js-fadein-ready">
                I am taking part in projects with a Japanese design company where I did an intern
                for 8 months. I am improving not only my coding skills but also soft skills which
                are essential to working in a team.
              </p>
            </div>

            <div class="frontAbout__skills -soft">
              <h4 class="frontAbout__skills-title js-fadein-ready">SKILLS ACQUIRED</h4>
              <ul class="frontAbout__list js-fadein-ready">
                <li class="frontAbout__listItem">Communication skills</li>
                <li class="frontAbout__listItem">Lateral Thinking</li>
                <li class="frontAbout__listItem">Critical Thinking</li>
                <li class="frontAbout__listItem">Problem-Solving skills</li>
              </ul>
            </div>
          </div>
        </div>

        <div class="frontAbout__box2">
          <h4 class="frontAbout__title js-fadein-ready">So, what are you up to?</h4>
          <div class="frontAbout__flexBox1">
            <div class="frontAbout__textBox">
              <p class="frontAbout__text js-fadein-ready">
                I am currently looking for a job as a coder / web developer. While doing so, I am
                also constantly learning; I am learning Javascript to increse my market value as a
                developer. I am planning to start on React.js as of January 2023. I love learning,
                and I always want to be a better version of myself than yesterday.
              </p>
            </div>

            <div class="frontAbout__skills -soft">
              <h4 class="frontAbout__skills-title js-fadein-ready">SKILLS TO BE ACQUIRED</h4>
              <ul class="frontAbout__list js-fadein-ready">
                <li class="frontAbout__listItem">Advanced Javascript</li>
                <li class="frontAbout__listItem">React.js</li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.frontAbout {
  width: 100%;
  margin: 0 auto;
  background-color: #dce2ec;
  color: #394563;
  margin-top: 70px;
  padding: 6rem 0;
}
.frontAbout .frontAbout__wrap {
  background-color: #ffffff;
  padding: 8rem 4rem 4rem;
  border-radius: 10px;
}
@media only screen and (max-width: 899px) {
  .frontAbout .frontAbout__wrap {
    padding: 5rem 1.6rem 4rem;
  }
}
.frontAbout .frontAbout__heading {
  font-size: 5rem;
  font-weight: 700;
  letter-spacing: 0.1em;
  text-align: center;
  margin-bottom: 8rem;
  position: relative;
}
.frontAbout .frontAbout__heading::before {
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
.frontAbout .frontAbout__title {
  font-size: 4rem;
  font-weight: 700;
  letter-spacing: 0.1em;
  padding-left: 6rem;
}
@media only screen and (max-width: 899px) {
  .frontAbout .frontAbout__title {
    font-size: 2.4rem;
    padding-left: 0;
    max-width: 600px;
    margin: 0 auto;
  }
}
.frontAbout .frontAbout__flexBox1 {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  padding: 4rem 6rem;
}
@media only screen and (max-width: 899px) {
  .frontAbout .frontAbout__flexBox1 {
    padding: 4rem 0;
  }
}
.frontAbout .frontAbout__textBox {
  width: 45%;
}
@media only screen and (max-width: 899px) {
  .frontAbout .frontAbout__textBox {
    width: 100%;
    max-width: 600px;
    margin: 0 auto;
  }
}
.frontAbout .frontAbout__text {
  font-size: 2rem;
  font-weight: 700;
  letter-spacing: 0.1em;
}
@media only screen and (max-width: 899px) {
  .frontAbout .frontAbout__text {
    font-size: 1.6rem;
  }
}
.frontAbout .frontAbout__skills {
  width: 45%;
}
@media only screen and (max-width: 899px) {
  .frontAbout .frontAbout__skills {
    width: 100%;
    max-width: 600px;
    margin: 2rem auto;
  }
}
.frontAbout .frontAbout__skills-title {
  font-size: 2rem;
  border-bottom: 1px solid #394563;
  margin-bottom: 2rem;
}
.frontAbout .frontAbout__list {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  flex-wrap: wrap;
}
@media only screen and (max-width: 899px) {
  .frontAbout .frontAbout__list {
    padding-top: 0;
  }
}
.frontAbout .frontAbout__listItem {
  font-size: 2rem;
  font-weight: 400;
  padding: 0 1.2rem;
  letter-spacing: 0.1em;
  background-color: #394563;
  color: #ffffff;
  margin: 0 2rem 2rem 0;
  margin-right: 2rem;
  border-radius: 5px;
}
.frontAbout .frontAbout__skills.-soft .frontAbout__listItem {
  background-color: #234d4f;
}
</style>
