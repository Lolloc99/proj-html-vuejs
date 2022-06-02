<template>
  <section class="section">
    <div class="container">
      <div class="col-sx">
        <small>Send a message</small>
        <h1>Get in</h1>
        <p class="submain">
          We will responde to your message as soon as possible
        </p>
        <ul class="input-container">
          <li>
            <input type="text" placeholder="Name" />
            <img src="../assets/images/image-(1).png" alt="name" />
          </li>
          <li>
            <input type="text" placeholder="Email" />
          </li>
          <li>
            <input type="text" placeholder="Phone" />
          </li>
          <li>
            <input type="text" placeholder="More Info" />
            <i class="fas fa-chevron-down"></i>
          </li>
          <li>
            <input type="text" placeholder="Message" class="big-input" />
          </li>
        </ul>
        <button class="btn-generic">Send</button>
      </div>
      <div class="col-dx">
        <h2>Example Inc.</h2>
        <p class="submain">
          Lorem ipsum dolor sit amet, consectetur adipisicing elit.
        </p>
        <p class="submain">
          Praesent diam lacus, dipibus sed imperdiet consectetur
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
        <button class="btn-generic-empty">View Map</button>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "MainSeventhSection",
};
</script>

<style scoped lang="scss">
@import "../style/variables.scss";
@import "~@fortawesome/fontawesome-free/css/all.min.css"; //Font Awesome

.section {
  padding: 7.5rem 0;
  background-color: white;
}

.container {
  display: flex;
  justify-content: space-between;
}

.col-sx {
  width: 60%;

  h1 {
    margin-top: 1rem;
    margin-bottom: 1.6rem;

    &::after {
      content: "Touch";
      color: $text-light;
      padding: 0 1rem;
      margin-left: 0.5rem;
      background-color: $bg-light-blue;
      border-radius: 5px;
    }
  }
  .input-container {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    margin-top: 2rem;

    input {
      width: 100%;
      height: 3rem;
      padding: 1rem;
      margin: 0.7rem 0;
      font-size: 1rem;
      border: none;
      border-radius: 5px;
      background-color: #ececec;
    }

    .big-input {
      height: 10rem;
    }

    li {
      position: relative;
      width: calc(100% / 2 - 0.5rem);

      &:last-child {
        width: 100%;
        margin-bottom: 1rem;
      }
    }

    li img,
    li i {
      position: absolute;
      top: 26px;
      right: 5px;
    }
  }
}

.col-dx {
  width: 40%;
  padding-left: 5rem;

  h2 {
    color: $text-dark;
    letter-spacing: 1px;
  }

  p {
    font-size: 1rem;
    letter-spacing: 0.7px;
    margin: 1.3rem 0;
    line-height: 1.4rem;
  }

  li {
    width: 100%;

    i {
      display: inline-block;
      font-size: 1.2rem;
      margin-right: 1rem;
      color: $text-light;
      background-color: $bg-light-blue;
      padding: 0.7rem;
      border-radius: 50%;
    }

    p {
      display: inline-block;
      color: $text-light;
      font-size: 1.2rem;
    }

    &:last-child i {
      padding: 0.7rem 0.9rem;
    }
  }
}

.btn-generic {
  margin-bottom: 2rem;

  &:active {
    border: 1px solid $text-dark;
  }
}

.btn-generic-empty {
  color: $text-light;
  margin-top: 1rem;

  &:active {
    border: 1px solid $text-dark;
    background-color: $text-light;
    border: 1px solid white;
    color: white;
  }
}
</style>
