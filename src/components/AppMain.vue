<template>
  <main>
    <MainBanner :links="bannerLinks" />
    <MainFirstSection :cards="firstSectionCards" />
    <MainSecondSection :cards="secondSectionCards" />
    <MainThirdSection :cards="thirdSectionCards" />
    <MainFourthSection :cards="fourthSectionCards" />
    <MainFifthSection :cards="fifthSectionCards" />
    <MainSixthSection />
    <MainSeventhSection />
  </main>
</template>

<script>
import MainBanner from "./MainBanner.vue";
import MainFirstSection from "./MainFirstSection.vue";
import MainSecondSection from "./MainSecondSection.vue";
import MainThirdSection from "./MainThirdSection.vue";
import MainFourthSection from "./MainFourthSection.vue";
import MainFifthSection from "./MainFifthSection.vue";
import MainSixthSection from "./MainSixthSection.vue";
import MainSeventhSection from "./MainSeventhSection.vue";

export default {
  name: "AppMain",
  components: {
    MainBanner,
    MainFirstSection,
    MainSecondSection,
    MainThirdSection,
    MainFourthSection,
    MainFifthSection,
    MainSixthSection,
    MainSeventhSection,
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
          subtitle:
            "Humanizing business: Harness the power of technology to improve way people work.",
        },
        {
          icon: "fas fa-chart-pie",
          title: "Core Business",
          subtitle:
            "It takes innovative approaches to transform, modernize, and run existing platforms.",
        },
        {
          icon: "fas fa-tachometer-alt",
          title: "Performance",
          subtitle:
            "Achieving maximum impact and value from investments in finance and supply chain.",
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
          subtitle: "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
        },
      ],
      thirdSectionCards: [
        {
          icon: "fas fa-sitemap",
          title: "Audit & Assurance",
          subtitle: "Lorem ipsum dolor sit amet, consectetur adipisicing elit.",
        },
        {
          icon: "fas fa-briefcase",
          title: "Financial Advisory",
          subtitle: "Lorem ipsum dolor sit amet, consectetur adipisicing elit.",
        },
        {
          icon: "fas fa-chart-line",
          title: "Analytics and M&A",
          subtitle: "Lorem ipsum dolor sit amet, consectetur adipisicing elit.",
        },
        {
          icon: "fas fa-plane",
          title: "Middle Marketing",
          subtitle: "Lorem ipsum dolor sit amet, consectetur adipisicing elit.",
        },
        {
          icon: "fas fa-globe",
          title: "Legal Consulting",
          subtitle: "Lorem ipsum dolor sit amet, consectetur adipisicing elit.",
        },
        {
          icon: "fas fa-inbox",
          title: "Regulatory Risk",
          subtitle: "Lorem ipsum dolor sit amet, consectetur adipisicing elit.",
        },
      ],
      fourthSectionCards: [
        {
          icon: "fas fa-rocket",
          title: "Standard",
          price: 490,
          option1: "fas fa-check",
          option2: "fas fa-check",
          option3: "fas fa-times",
          option4: "fas fa-times",
          option5: "fas fa-times",
        },
        {
          icon: "fas fa-briefcase",
          title: "Professional",
          price: 890,
          option1: "fas fa-check",
          option2: "fas fa-check",
          option3: "fas fa-check",
          option4: "fas fa-times",
          option5: "fas fa-times",
        },
        {
          icon: "far fa-gem",
          title: "Ultimate",
          price: 1390,
          option1: "fas fa-check",
          option2: "fas fa-check",
          option3: "fas fa-check",
          option4: "fas fa-check",
          option5: "fas fa-check",
        },
      ],
      fifthSectionCards: [
        {
          img: "news-1.jpg",
          title: "Increasing creativity is possible for everyone",
          text: "Lorem ipsum dolor, sit amet consectetur adipisicing elit.",
          time: "3 Days Ago",
          user: "Andrea Miller",
        },
        {
          img: "news-2.jpg",
          title: "Because market research is part of the business plan",
          text: "Lorem ipsum dolor, sit amet consectetur adipisicing elit.",
          time: "2 Days Ago",
          user: "Roberto Rossi",
        },
        {
          img: "news-3.jpg",
          title: "Working from home is now a trend",
          text: "Lorem ipsum dolor, sit amet consectetur adipisicing elit.",
          time: "4 Days Ago",
          user: "Arianna Esper",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss"></style>
