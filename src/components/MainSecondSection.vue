<template>
  <section class="section">
    <div class="col sx">
      <small>About the network</small>
      <h1>Company</h1>
      <p>
        For 12 years we have been providing audit and warrenty, financial
        advice, risk advice, taxes and related services to selcet clients.
      </p>
      <ul>
        <li v-for="(item, index) in cards" :key="index">
          <i :class="item.icon"></i>
          <h2>{{ item.title }}</h2>
          <p>{{ item.subtitle }}</p>
        </li>
      </ul>
    </div>
    <div class="col dx"></div>
  </section>
</template>

<script>
export default {
  name: "MainSecondSection",
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
  height: 85vh;
  background-color: white;
}

.col {
  width: 50%;
  height: 100%;
}

.sx {
  padding: 7.5rem 0;
  padding-left: 20%;
}

.dx {
  background-image: url(../assets/images/about-3.jpg);
  background-position: center;
  background-size: cover;
}

img {
  height: 100%;
}

h1 {
  margin: 1.7rem 0;

  &::before {
    content: "The";
    color: $text-light;
    padding: 0 1rem;
    background-color: $bg-light-blue;
    border-radius: 5px;
  }
}

p {
  color: rgba(33, 62, 55, 0.7);
  font-size: 1.15rem;
  font-family: $big
}

ul {
  margin-top: 4rem;

  h2 {
    display: inline-block;
    color: $text-dark;
  }

  i {
    font-size: 1.5rem;
    color: $text-light;
    margin-right: 0.5rem;
  }

  p {
    margin-top: 2rem;
  }

  li {
    display: inline-block;
    max-width: calc(100% / 2);
    min-height: 150px;
  }
}
</style>
