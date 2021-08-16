<template>
  <div>
    <header-banner :is-home="false" />
    <div class="il__container">
      <navigation />
    </div>
    {{ team }}
    <footer-info />
  </div>
</template>

<script>
import HeaderBanner from "../components/HeaderBanner";
import Navigation from "../components/Navigation";
import FooterInfo from "../components/FooterInfo";
export default {
  name: "Team",
  components: { FooterInfo, Navigation, HeaderBanner },
  props: {
    team: {
      type: Object,
      required: true,
      default: () => ({}),
    },
    teamName: {
      type: String,
      required: true,
    },
  },
};
</script>

<style scoped></style>
