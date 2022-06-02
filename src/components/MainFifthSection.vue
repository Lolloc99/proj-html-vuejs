<template>
  <section class="section">
    <div class="container">
      <small>Our Editorial Content</small>
      <h1>Latest</h1>
      <div class="space-bet">
        <p class="submain">
          Every week we publish content about what is best in the business world
        </p>
        <button class="btn-generic">See all</button>
      </div>
      <ul>
        <li v-for="(item, index) in cards" :key="index">
          <div class="info1">
            <div class="abs first">
              <i class="far fa-user"></i>
              <span>{{ item.user }}</span>
            </div>
            <div class="abs second">
              <i class="far fa-clock"></i>
              <span>{{ item.time }}</span>
            </div>
            <div class="abs third">
              <span>{{ item.text }}</span>
            </div>
          </div>
          <img
            :src="require(`../assets/images/${item.img}`)"
            :alt="item.title"
          />
          <span class="main-span">{{ item.title }}</span>
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
  padding: 7rem 0;
  background-color: white;
}

h1 {
  margin-top: 1.5rem;

  &::after {
    content: "News";
    color: $text-light;
    padding: 0 1rem;
    margin-left: 0.5rem;
    background-color: $bg-light-blue;
    border-radius: 5px;
  }
}

.btn-generic:active {
  border: 1px solid $text-dark;
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

  .main-span {
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
    transition: 0.2s;
  }

  &:hover .info1 {
    display: inline;
  }

  &:hover .main-span {
    bottom: 8rem;
  }

  .info1 {
    display: none;

    .abs {
      position: absolute;
      color: white;
      z-index: 1;
      font-size: 1rem;
    }

    i {
      margin-right: 0.5rem;
    }

    .first {
      top: 35px;
      left: 60px;
    }

    .second {
      top: 35px;
      right: 60px;
    }

    .third {
      bottom: 55px;
      left: 60px;
      font-size: 1.2rem;
    }
  }
}
</style>
