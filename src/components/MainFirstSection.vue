<template>
  <section class="section">
    <ul class="container row">
      <li v-for="(card, index) in cards" :key="index" class="col">
        <i :class="card.icon"></i>
        <h2>{{ card.title }}</h2>
        <p>{{ card.subtitle }}</p>
      </li>
    </ul>
  </section>
</template>

<script>
export default {
  name: "MainFirstSection",
  props: {
    cards: Array,
  },
};
</script>

<style scoped lang="scss">
@import "../style/variables.scss";
@import "~@fortawesome/fontawesome-free/css/all.min.css"; //Font Awesome

.section {
  align-items: center;
  padding: 8rem 0;
  background-color: $bg-light-green;
}

.row {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
}

.col {
  max-width: 360px;
  min-height: 270px;
  padding: 3rem;
  background-color: white;
  margin: 1rem 0;
  transition: 0.5s;

  &:hover {
    transform: translate(0px, -12px);
  }
}

h2 {
  margin: 1.3rem 0;
  color: $text-dark;
  letter-spacing: 1px;
}

p {
  color: rgba(33, 62, 55, 0.7);
  font-size: 1.15rem;
}

i {
  font-size: 1.8rem;
  padding: 1rem;
  border-radius: 50%;
  color: $text-light;
  background-color: $bg-light-blue;
}
</style>
