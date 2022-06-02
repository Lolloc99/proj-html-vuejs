<template>
  <footer class="section-alt">
    <div class="top-footer container">
      <div class="col intro">
        <h2 class="nexgen">GEN</h2>
        <p class="submain">
          A Functional HTML Template <br />
          for corporate & business
        </p>
        <ul>
          <li>
            <i class="fas fa-phone"></i>
            <p>+1 (305) 1234-5678</p>
          </li>
          <li>
            <i class="fas fa-envelope"></i>
            <p>hello@example.com</p>
          </li>
          <li>
            <i class="fas fa-map-marker-alt"></i>
            <p>Main Evenue, 987</p>
          </li>
        </ul>
        <button class="btn-generic-empty">Get in touch</button>
      </div>
      <ul class="ul">
        <li class="col card" v-for="(item, index) in info" :key="index">
          <h3>{{ item.title }}</h3>
          <ul>
            <li>
              <i class="fas fa-chevron-right"></i>
              <p>{{ item.option1 }}</p>
            </li>
            <li>
              <i class="fas fa-chevron-right"></i>
              <p>{{ item.option2 }}</p>
            </li>
            <li>
              <i class="fas fa-chevron-right"></i>
              <p>{{ item.option3 }}</p>
            </li>
            <li>
              <i class="fas fa-chevron-right"></i>
              <p>{{ item.option4 }}</p>
            </li>
            <li>
              <i class="fas fa-chevron-right"></i>
              <p>{{ item.option5 }}</p>
            </li>
            <li>
              <i class="fas fa-chevron-right"></i>
              <p>{{ item.option6 }}</p>
            </li>
          </ul>
        </li>
      </ul>
    </div>
    <div class="bottom-footer">
      <div class="container">
        <p class="sx">
          Enjoy the low price, We are tracking any intention pf piracy
        </p>
        <p class="dx">
          &copy; 2020 NEXGEN is Proudly Powered by <span>Codings</span>.
        </p>
        <a href="header"><i class="fas fa-arrow-alt-circle-up"></i></a>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "AppFooter",
  props: {
    info: Array,
  },
};
</script>

<style scoped lang="scss">
@import "../style/variables.scss";
@import "~@fortawesome/fontawesome-free/css/all.min.css"; //Font Awesome

.section-alt {
  background-color: $bg-dark-blue;
}

.col {
  width: calc(100% / 4);
  color: $text-footer;

  &:first-child {
    padding: 0;
  }
}

.top-footer {
  display: flex;
  justify-content: space-between;
  padding: 8rem 0;
  margin-bottom: 2rem;

  .nexgen {
    font-size: 1.7rem;
    letter-spacing: 5px;
    color: $text-footer;

    &::before {
      content: "NEX";
      color: $text-lighter;
      padding: 0.7rem 0 0.7rem 2rem;
      margin-right: 3px;
      border-top-left-radius: 30px;
      border-bottom-left-radius: 30px;
      background-color: $nexgen-logo-bg;
    }
  }

  .submain {
    margin: 3rem 0;
    color: $text-footer;
    letter-spacing: 0.6px;
  }

  .intro {
    li {
      width: 100%;
      margin: 1rem 0;

      i {
        display: inline-block;
        margin-right: 1rem;
        color: $text-footer;
        border-radius: 50%;
      }

      p {
        display: inline-block;
        color: $text-footer;
      }
    }

    .btn-generic-empty {
      margin-top: 1rem;
      font-weight: bold;

      &:active {
        color: white;
        border: 1px solid $text-light;
        background-color: $text-light;
      }
    }
  }

  .ul {
    display: flex;
    justify-content: space-between;
  }

  .card {
    width: 100%;
    padding: 2rem 2.5rem;
    min-height: 330px;
    margin: 0 1rem;
    border-radius: 10px;
    background-color: $card-dark;

    h3 {
      font-size: 1.6rem;
      margin-bottom: 1.5rem;
      color: white;
      margin-right: 5rem;
    }

    li {
      display: flex;
      justify-content: flex-start;
      margin: 0.8rem 0;
      letter-spacing: 0.6px;

      i {
        margin-right: 1rem;
      }
    }
  }
}

.bottom-footer {
  display: flex;
  justify-content: center;
  width: 100%;
  background-color: $bg-darker-blue;

  .container {
    position: relative;
    display: flex;
    justify-content: space-between;
    align-items: center;

    p {
      color: $text-footer;
      margin: 2rem 0;
    }

    span {
      color: $text-light;
      margin-left: 0.3rem;
      letter-spacing: 0.5px;
      font-size: 1.2rem;
    }

    i {
      font-size: 2.5rem;
      color: $text-light;
      cursor: pointer;
    }

    a {
      position: absolute;
      right: -350px;
      bottom: 25px;
    }
  }
}
</style>
