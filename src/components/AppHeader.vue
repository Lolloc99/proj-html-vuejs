<template>
  <header class="header">
    <section class="container">
      <div class="col-sx">
        <i class="fas fa-clock"></i>
        <span>Open Hours: Mon - Sat - 9:00 - 18:00</span>
      </div>
      <div class="col-dx">
        <div>
          <i class="fas fa-phone"></i>
          <span>+1 (305) 1234-5678</span>
        </div>
        <div>
          <i class="fas fa-envelope"></i>
          <span>hello@example.com</span>
        </div>
        <i class="fab fa-facebook-f"></i>
        <i class="fab fa-twitter"></i>
        <i class="fab fa-linkedin-in"></i>
      </div>
    </section>
  </header>
</template>

<script>
export default {
  name: "AppHeader",
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

  i {
    color: #c4c3c3;
    margin: 0 1rem;
    font-size: 0.9rem;
    cursor: pointer;
  }

  div {
    margin: 0 0.8rem;
    cursor: pointer;
  }

  div i {
    margin: 0 0.5rem;
  }
}
</style>
