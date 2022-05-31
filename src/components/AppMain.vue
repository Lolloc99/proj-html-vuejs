<template>
  <main>
    <MainBanner :links="bannerLinks"/>
    <MainFirstSection :cards="firstSectionCards"/>
  </main>
</template>

<script>
import MainBanner from "./MainBanner.vue";
import MainFirstSection from './MainFirstSection.vue';

export default {
  name: "AppMain",
  components: {
    MainBanner,
    MainFirstSection,
  },

  data: function () {
    return {
      bannerLinks: [
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
      firstSectionCards: [
        {
          icon: "far fa-user",
          title: "Human Capital",
          subtitle: "Humanizing business: Harness the power of technology to improve way people work."
        },
        {
          icon: "fas fa-chart-pie",
          title: "Core Business",
          subtitle: "It takes innovative approaches to transform, modernize, and run existing platforms."
        },
        {
          icon: "fas fa-tachometer-alt",
          title: "Performance",
          subtitle: "Achieving maximum impact and value from investments in finance and supply chain."
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss"></style>
