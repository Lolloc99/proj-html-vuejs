<template>
  <main class="banner">
    <section class="container">
      <!-- Navbar -->
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
          <button class="btn-generic">Get in touch</button>
        </div>
      </nav>
      <!-- /Navbar -->

      <!-- Banner content -->
      <div class="lead-c">
        <h1>Lead ~</h1>
        <p>
          Successful strategies require data analysis , creativity and customer
          focus , taking <br />
          advantage of the latest technologies to offer excellent services .
        </p>
        <div class="btns">
          <button class="btn-generic">Get in touch</button>
          <button class="btn-generic-empty">Read more</button>
        </div>
      </div>
      <!-- /Banner content -->
    </section>
  </main>
</template>

<script>
export default {
  name: "MainBanner",
  props: {
    links: Array,
  },
};
</script>

<style scoped lang="scss">
@import "../style/variables.scss";

.banner {
  position: relative;
  display: flex;
  justify-content: center;
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
      color: $text-light;
    }
  }

  ul {
    display: inline-block;
  }
}

.btn-generic {
  display: inline-block;
  margin-left: 0.3rem;
  font-weight: bold;
}

.btn-generic-empty {
  display: inline-block;
  margin-left: 0.3rem;
  margin: 0 0.3rem 0 1.5rem;
  font-weight: bold;
}

.nexgen::before {
  content: "NEX";
  color: $text-lighter;
  padding: 0.7rem 0 0.7rem 2rem;
  margin-right: 3px;
  border-top-left-radius: 30px;
  border-bottom-left-radius: 30px;
  background-color: $nexgen-logo-bg;
}

.lead-c {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 80%;

  h1 {
    font-size: 5rem;
    color: white;

    &::after {
      content: "Customer";
      padding: 0 1rem;
      background-color: rgba(0, 128, 53, 0.1);
    }
  }

  p {
    margin-top: 2rem;
    text-align: center;
    font-size: 1.3rem;
    color: rgb(179, 175, 175);
  }
}

.btns {
  margin-top: 2.5rem;
}
</style>
