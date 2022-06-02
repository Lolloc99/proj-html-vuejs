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
        <button class="btn-generic-empty see-all">See all</button>
      </div>
      <ul>
        <li v-for="(item, index) in cards" :key="index">
          <i :class="item.icon"></i>
          <h2>{{ item.title }}</h2>
          <p>{{ item.subtitle }}</p>
          <button class="btn-generic-empty">Read more</button>
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
  padding: 8rem 0;
  background-color: $bg-dark-blue;
}

h1 {
  color: white;
  margin: 1.7rem 0;

  &::after {
    content: "Services";
    color: white;
    margin-left: 0.5rem;
    padding: 0 1rem;
    background-color: $services-evidencer;
    border-radius: 5px;
  }
}

.btn-generic-empty {
  font-size: 1.1rem;
  padding: 0.7rem 1.5rem;

  &:active {
    color: white;
  }
}

.see-all:active {
  color: $text-light;
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
    transition: 0.5s;

    &:hover {
      transform: translate(0px, -12px);
    }

    &:hover button {
      background-color: $text-light;
    }
  }
}
</style>
