<template>
  <header class="header">
    <img
      v-if="isHome"
      class="img__banner"
      src="../assets/img/il_banner.jpg"
      alt="banner"
    />
    <img
      v-else
      class="img__banner"
      src="../assets/img/il_banner2.jpg"
      alt="banner2"
    />
  </header>
</template>

<script>
export default {
  name: "HeaderBanner",
  props: {
    isHome: {
      type: Boolean,
      required: true,
    },
  },
};
</script>

<style scoped>
.header {
  margin-bottom: 30px;
}
.header img {
  border-radius: 0 0 20px 20px;
}
</style>
