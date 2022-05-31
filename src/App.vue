<template>
  <div id="app">
    <AppHeader :contacts="headerContacts"/>
    <AppMain />
    <AppFooter />
  </div>
</template>

<script>
import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";
import AppFooter from "./components/AppFooter.vue";

export default {
  name: "App",
  components: {
    AppHeader,
    AppMain,
    AppFooter,
  },

  data: function () {
    return {
      headerContacts: [
        {
          icon: "fas fa-phone",
          text: "+1 (305) 1234-5678",
        },
        {
          icon: "fas fa-envelope",
          text: "hello@example.com",
        },
        {
          icon: "fab fa-facebook-f",
          text: "",
        },
        {
          icon: "fab fa-twitter",
          text: "",
        },
        {
          icon: "fab fa-linkedin-in",
          text: "",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@import "./style/common.scss";
// @import url('https://fonts.googleapis.com/css2?family=Roboto:wght@100;300;400;500;700;900&display=swap'); [non funziona, messo manualmente nell'index]
</style>
