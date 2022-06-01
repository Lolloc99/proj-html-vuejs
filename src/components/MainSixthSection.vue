<template>
  <section class="section">
    <div class="container">
      <div class="col">
        <small>Newsletter</small>
        <h1> First</h1>
        <p class="submain">
          Follow closely and receive content about our company <br />
          and the news of the current market
        </p>
      </div>
      <div class="col">
        <input type="text" placeholder="Name" />
        <input type="text" placeholder="Email" />
        <button class="btn">Subscribe</button>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "MainSixthSection",
};
</script>

<style scoped lang="scss">
@import "../style/variables.scss";

.section {
  display: flex;
  justify-content: center;
  width: 100%;
  height: 49vh;
  background-image: url(../assets/images/bg-1.jpg);
  background-position: center;
  background-repeat: no-repeat;
}

.container {
  display: flex;
  justify-content: space-between;
  padding: 7.8rem 6.7rem;
}

.col {
  width: 50%;
}

h1 {
  margin: 1.5rem 0;
  color: white;

  &::before {
    content: "Know";
    color: white;
    padding: 0 1rem;
    background-color: rgba(30, 62, 68, .7);
    border-radius: 5px;
  }
}

p {
  color: white;
  font-size: 1rem;
  letter-spacing: 0.8px;
  font-weight: 300;
}

.btn {
  font-size: 1.1rem;
  padding: 0.7rem 1.5rem;
  border: 1px solid transparent;
  border-radius: 5px;
  text-transform: uppercase;
  color: white;
  background-color: $text-light;
  margin-top: .7rem;
  margin-left: 1rem;

  &:active {
    border: 1px solid $text-dark;
  }
}

input {
  width: 95%;
  height: 3rem;
  padding: 1rem;
  margin: 0.7rem 0;
  margin-left: 1rem;
  font-size: 1rem;
  border: none;
  border-radius: 5px;
  background-color: rgba(211, 223, 222, 0.6);
}
</style>
