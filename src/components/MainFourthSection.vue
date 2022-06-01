<template>
  <section class="section">
    <div class="container">
      <div class="intro">
        <small>Monthly plans</small>
        <h1> Table</h1>
        <p>
          We can help you deliver and execute your future, whetever you compete,
          using the latest <br />
          technologies, from strategy development to implementation.
        </p>
      </div>
      <ul class="main-ul">
        <li class="main-li" v-for="(item, index) in cards" :key="index">
          <div class="info-start">
            <p class="most-popular">
              Most <br />
              Popular
            </p>
            <i :class="item.icon"></i>
            <h2>{{ item.title }}</h2>
            <h4>
              $
              <h3>{{ item.price }}</h3>
              / mo
            </h4>
          </div>
          <!-- divisore -->
          <ul class="info-list">
            <li>
              <span>Standard Accounting</span>
              <i :class="item - option1"></i>
            </li>
            <li class="li">
              <span>Platform Access</span>
              <i :class="item - option2"></i>
            </li>
            <li class="li">
              <span>Business Orientation</span>
              <i :class="item - option3"></i>
            </li>
            <li class="li">
              <span>Dedicated Consultant</span>
              <i :class="item - option4"></i>
            </li>
            <li class="li">
              <span>Personal Assistance</span>
              <i :class="item - option5"></i>
            </li>
          </ul>
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
export default {
  name: "MainFourthSection",
  props: {
    cards: Array,
  },
};
</script>

<style scoped lang="scss">
@import "../style/variables.scss";
@import "~@fortawesome/fontawesome-free/css/all.min.css"; //Font Awesome

.section {
  display: flex;
  justify-content: center;
  width: 100%;
  background-color: $bg-light-green;
  padding: 8rem 0 10rem 0;
}

.intro {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;

  h1 {
    margin: 2rem 0;

    &::before {
      content: "Pricing";
      color: $text-light;
      padding: 0 1rem;
      background-color: $bg-dark-green;
      border-radius: 5px;
    }
  }

  p {
    color: rgba(33, 62, 55, 0.7);
    font-size: 1.15rem;
  }
}

.main-ul {
  display: flex;
  justify-content: space-between;
  margin-top: 4rem;
}

.main-li {
  background-color: white;
  width: calc(100% / 3 - 1.5rem);
  min-height: 500px;
  padding: 2rem;
  transition: 0.5s;

  &:hover {
    transform: scale(1.08);
  }

  &:nth-child(2) .most-popular {
    display: inline;
  }
}

.info-start {
  position: relative;
  text-align: center;

  i {
    font-size: 2.5rem;
    color: $text-light;
    display: block;
  }

  h2,
  h3,
  h4 {
    display: inline-block;
    letter-spacing: 0.8px;
  }

  h2 {
    font-size: 1.6rem;
    margin: 1rem 0;
    font-family: $big;
    color: $text-dark;
    display: block;
  }

  h3 {
    font-size: 2.5rem;
    font-family: $big;
  }

  h4 {
    margin-bottom: 1rem;
    font-size: 1.3rem;
    color: $text-light;
  }

  .most-popular {
    display: none;
    position: absolute;
    top: -18px;
    left: -32px;
    padding: 0.3rem 1rem 0.3rem 0.7rem;
    font-size: 0.8rem;
    text-align: start;
    border-top-right-radius: 20px;
    border-bottom-right-radius: 20px;
    background-color: $text-lighter;
    color: white;
  }
}

.info-list {
  li {
    display: flex;
    justify-content: space-between;
    margin: 1.3rem 0;
    font-size: 1.15rem;
    letter-spacing: 0.1px;
    color: rgba(33, 62, 55, 0.7);
  }

  i {
    font-size: 1.2rem;
    color: $text-light;
  }
}
</style>
