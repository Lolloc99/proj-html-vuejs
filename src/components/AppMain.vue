<template>
  <main>
    <MainBanner :links="bannerLinks"/>
    <MainFirstSection :cards="firstSectionCards"/>
    <MainSecondSection :cards="secondSectionCards"/>
  </main>
</template>

<script>
import MainBanner from "./MainBanner.vue";
import MainFirstSection from './MainFirstSection.vue';
import MainSecondSection from './MainSecondSection.vue';

export default {
  name: "AppMain",
  components: {
    MainBanner,
    MainFirstSection,
    MainSecondSection,
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
      secondSectionCards: [
        {
          icon: "fas fa-award",
          title: "Tradition",
          subtitle: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
        },
        {
          icon: "fas fa-lock",
          title: "Security",
          subtitle: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
        },
        {
          icon: "fas fa-edit",
          title: "Certificate",
          subtitle: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
        },
        {
          icon: "fas fa-graduation-cap",
          title: "Expertise",
          subtitle: "Lorem ipsum dolor sit amet consectetur adipisicing elit." ,
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss"></style>
