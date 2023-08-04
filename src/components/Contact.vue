<template>
  <section class="frontContact" id="frontContact">
    <div class="inner">
      <h3 class="frontContact__heading">CONTACT</h3>
      <p class="frontContact__description">
        If you are interested in <span>me</span>, <br class="-sp-only" />contact <span>me</span>!
      </p>
      <table class="frontContact__table">
        <tr>
          <th>Email address:</th>
          <td>kenta0810hayashi@gmail.com</td>
        </tr>
      </table>
    </div>
  </section>
</template>

<style scoped>
.frontContact {
  padding: 10rem 0;
  margin-top: 100px;
}
.frontContact .frontContact__heading {
  color: #ffffff;
  font-size: 5rem;
  font-weight: 700;
  letter-spacing: 0.1em;
  text-align: center;
  margin-bottom: 1rem;
  position: relative;
}
.frontContact .frontContact__heading::before {
  position: absolute;
  content: '';
  left: 50%;
  top: 100px;
  transform: translateX(-50%);
  display: inline-block;
  height: 5px;
  width: 50px;
  border-radius: 5px;
  background-color: #ffffff;
}
.frontContact .frontContact__description {
  font-size: 2.8rem;
  font-weight: 400;
  letter-spacing: 0.1em;
  line-height: 1.5;
  margin: 0 auto;
  color: #ffffff;
  max-width: 800px;
  margin: 5rem auto 0;
  text-align: center;
}
.frontContact .frontContact__description span {
  color: #dce2ec;
  font-weight: 700;
}
.frontContact .frontContact__table {
  max-width: 800px;
  margin: 0 auto;
  border: none;
  font-size: 2rem;
  margin-top: 2rem;
}
@media only screen and (max-width: 899px) {
  .frontContact .frontContact__table {
    font-size: 1.4rem;
  }
}
.frontContact .frontContact__table tr {
  border: none;
}
.frontContact .frontContact__table th {
  border: none;
  padding-right: 3rem;
}
.frontContact .frontContact__table td {
  border: none;
}
</style>
