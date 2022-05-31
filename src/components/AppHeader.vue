<template>
  <header class="header">
    <section class="container">
      <div class="col-sx">
        <i class="fas fa-clock"></i>
        <span>Open Hours: Mon - Sat - 9:00 - 18:00</span>
      </div>
      <ul class="col-dx">
        <li v-for="(item, index) in contacts" :key="index">
          <i :class="item.icon"></i>
          <span>{{ item.text }}</span>
        </li>
      </ul>
    </section>
  </header>
</template>

<script>
export default {
  name: "AppHeader",
  props: {
    contacts: Array,
  }
};
</script>

<style scoped lang="scss">
@import "../style/variables.scss";
@import "~@fortawesome/fontawesome-free/css/all.min.css"; //Font Awesome
.header {
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: $bg-header;
}

.container {
  display: flex;
  justify-content: space-between;
  padding: 1rem 0;
}

span {
  color: #c4c3c3;
  font-size: 1rem;
}

.col-sx {
  display: flex;
  align-items: center;

  i {
    color: #c4c3c3;
    margin-right: 0.6rem;
    font-size: 1rem;
  }
}

.col-dx {
  display: flex;
  align-items: center;

  li {
    margin: 0 0.5rem;
    cursor: pointer;
  }
  
  i {
    margin: 0 0.5rem;
    color: #c4c3c3;
  }
}
</style>
