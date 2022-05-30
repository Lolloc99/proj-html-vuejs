<template>
  <main class="bg-container banner">
    <section class="container">
      <nav>
        <div col-sx>
          <h2 class="nexgen">GEN</h2>
        </div>

        <div col-dx>
          <ul>
            <li v-for="(item, index) in links" :key="index">
              <h3>{{ item.text }}</h3>
            </li>
          </ul>
          <button>GET IN TOUCH</button>
        </div>
      </nav>
    </section>
  </main>
</template>

<script>
export default {
  name: "MainBanner",
  data: function () {
    return {
      links: [
        {
          text: "HOME",
        },
        {
          text: "ABOUT",
        },
        {
          text: "SERVICES",
        },
        {
          text: "PRICING",
        },
        {
          text: "BLOG",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
@import "../style/variables.scss";

.banner {
  position: relative;
  width: 100%;
  height: 92vh;
  background-image: url(../assets/lead-customer/hero-image.png);
  background-repeat: no-repeat;
  background-size: cover;
  background-position-y: 100%;
}

.banner::after {
  content: "";
  width: 100%;
  height: 100%;
  position: absolute;
  top: 0;
  left: 0;
  background-color: rgba(1, 1, 12, 0.7);
}

.container {
  z-index: 1;
}

nav {
  display: flex;
  justify-content: space-between;
  align-content: center;
  margin-top: 2rem;

  h2 {
    display: inline-block;
    color: lightgrey;
    letter-spacing: 5px;
  }

  li {
    display: inline-block;
    color: white;
    margin: 0 1rem;
    cursor: pointer;

    &:hover {
        color: $btn-get-in-touch;
    }
  }

  ul {
      display: inline-block;
  }

  button {
    display: inline-block;
    border: transparent;
    padding: 0.8rem 1.6rem;
    font-size: 1rem;
    font-weight: bold;
    border-radius: 5px;
    color: white;
    background-color: $btn-get-in-touch;
    margin-left: .3rem;
    cursor: pointer;

    &:active {
      color: $btn-get-in-touch;
      background-color: white;
      border: 1px solid $btn-get-in-touch;
    }
  }
}

.nexgen::before {
  content: "NEX";
  color: $bg-most-popular;
  padding: 0.7rem 0.1rem 0.7rem 2rem;
  border-top-left-radius: 20px;
  border-bottom-left-radius: 20px;
  background-color: $nexgen-logo-bg;
}
</style>
