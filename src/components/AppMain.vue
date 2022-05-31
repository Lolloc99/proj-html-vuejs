<template>
  <main>
    <MainBanner />
    <MainFirstSection />
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
};
</script>

<style scoped lang="scss"></style>
