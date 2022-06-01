<template>
  <section class="section">
    <div class="container">
      <small>Our Editorial Content</small>
      <h1>Latest </h1>
      <div class="space-bet">
        <p class="submain">
          Every week we publish content about what is best in the business world
        </p>
        <button class="btn">See all</button>
      </div>
      <ul>
        <li v-for="(item, index) in cards" :key="index">
          <img
            :src="require(`../assets/images/${item.img}`)"
            :alt="item.text"
          />
          <span>{{ item.text }}</span>
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
export default {
  name: "MainFifthSection",
  props: {
    cards: Array,
  },
};
</script>

<style scoped lang="scss">
@import "../style/variables.scss";

.section {
  display: flex;
  justify-content: center;
  width: 100%;
  padding: 7rem 0;
  background-color: white;
}

h1 {
  margin-top: 1.5rem;

  &::after {
    content: "News";
    color: $text-light;
    padding: 0 1rem;
    background-color: $bg-light-blue;
    border-radius: 5px;
  }
}

.btn {
  font-size: 1.1rem;
  padding: 0.7rem 1.5rem;
  border: 1px solid transparent;
  border-radius: 5px;
  text-transform: uppercase;
  color: white;
  background-color: $text-light;
  margin-bottom: 2rem;

  &:active {
    border: 1px solid $text-dark;
  }
}

.space-bet {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

ul {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  margin-top: 1rem;
}

li {
  position: relative;
  width: calc(100% / 3 - 1.3rem);
  margin: 1rem 0;

  &:after {
    content: "";
    width: 100%;
    height: 99%;
    position: absolute;
    top: 0;
    left: 0;
    border-radius: 10px;
    background-color: rgba(0, 0, 0, 0.5);
  }

  img {
    width: 100%;
    border-radius: 10px;
  }

  span {
    position: absolute;
    width: 80%;
    bottom: 3rem;
    left: 2.5rem;
    color: white;
    font-size: 1.7rem;
    font-weight: bold;
    font-family: $big;
    text-align: center;
    z-index: 1;
    line-height: 1.7rem;
  }
}
</style>
