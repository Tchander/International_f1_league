<template>
  <div class="home">
    <header-banner :is-home="true" />
    <div class="il__container">
      <navigation />
      <home-slider />
    </div>
    <footer-info />
  </div>
</template>

<script>
import Navigation from "../components/Navigation";
import HeaderBanner from "../components/HeaderBanner";
import HomeSlider from "../components/HomeSlider";
import FooterInfo from "../components/FooterInfo";

export default {
  name: "Home",
  components: { FooterInfo, HomeSlider, HeaderBanner, Navigation },
};
</script>

<style scoped>
.home {
  font-family: "Lato", sans-serif;
}
</style>
