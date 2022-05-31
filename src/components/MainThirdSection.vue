<template>
  <section class="section">
    <div class="container">
      <small>Our business areas</small>
      <h1>Excellence in</h1>
      <div class="space-bet">
        <p>
          We are leaders in providing consultancy services with a set of
          cutting-edge technologies and a team of <br />
          experienced and renowed professionals. These are some options that you
          can hire.
        </p>
        <button class="third-section-btn">See all</button>
      </div>
      <ul>
        <li v-for="(item, index) in cards" :key="index">
          <i :class="item.icon"></i>
          <h2>{{ item.title }}</h2>
          <p>{{ item.subtitle }}</p>
          <button class="third-section-btn">Read more</button>
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
export default {
  name: "MainThirdSection",
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
  padding: 8rem 0;
  width: 100%;
  background-color: $bg-dark-blue;
}

h1 {
  color: white;

  &::after {
    content: "Services";
    color: white;
    padding: 0 1rem;
    background-color: $services-evidencer;
    border-radius: 5px;
  }
}

.third-section-btn {
  font-size: 1.1rem;
  padding: 0.7rem 1.5rem;
  border: 1px solid $text-light;
  border-radius: 5px;
  text-transform: uppercase;
  color: white;
  background-color: transparent;

  &:active {
    border: 1px solid white;
  }
}

.space-bet {
  display: flex;
  justify-content: space-between;
}

p {
  letter-spacing: 1px;
  color: rgba(255, 255, 255, 0.692);
}

ul {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  margin-top: 2rem;

  i {
    font-size: 3rem;
    color: $text-light;
  }

  h2 {
    margin: 1.5rem 0;
    color: white;
  }

  button {
    font-size: 1rem;
    margin-top: 2rem;
  }

  li {
    display: inline-block;
    max-width: calc(100% / 3 - 1.5rem);
    min-height: 300px;
    margin: 1.5rem 0;
    padding: 3rem;
    border-radius: 10px;
    background-color: $card-dark;
  }
}
</style>
