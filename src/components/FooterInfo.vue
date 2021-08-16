<template>
  <v-footer color="#0f3368">
    <v-card flat tile class="il__footer__card">
      <v-card-text class="il__footer__card__text">
        <v-btn
          class="il__footer_card__button"
          v-for="icon in icons"
          :key="icon"
          icon
        >
          <a
            v-if="icon === 'mdi-vk'"
            class="il__footer__link"
            href="https://vk.com/f1ileague"
            target="_blank"
          >
            <v-icon color="#fff" size="40px">
              {{ icon }}
            </v-icon>
          </a>
          <a
            v-if="icon === 'mdi-telegram'"
            class="il__footer__link"
            href="https://t.me/joinchat/JmWgNEOkS9tfo58lIOBhhw"
            target="_blank"
          >
            <v-icon color="#fff" size="40px">
              {{ icon }}
            </v-icon>
          </a>
          <a
            v-if="icon === 'mdi-youtube'"
            class="il__footer__link"
            href="https://youtube.com/channel/UC9F7VXNzjL4y07XXao0D4PQ"
            target="_blank"
          >
            <v-icon color="#fff" size="40px">
              {{ icon }}
            </v-icon>
          </a>
          <a
            v-if="icon === 'mdi-discord'"
            class="il__footer__link"
            href="https://discord.gg/g6ADEgp9tH"
            target="_blank"
          >
            <v-icon color="#fff" size="40px">
              {{ icon }}
            </v-icon>
          </a>
        </v-btn>
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<script>
export default {
  name: "FooterInfo",
  data: () => ({
    icons: ["mdi-vk", "mdi-telegram", "mdi-youtube", "mdi-discord"],
  }),
};
</script>

<style scoped>
.il__footer__card {
  width: 100%;
  color: #fff;
  border-radius: 5px;
}
.il__footer__card__text {
  /*background-color: #2aaae6;*/
  background-color: #0f3368;
  /*background-color: #2a76e6;*/
  /*background-color: rgb(66, 6, 1);*/
  color: #fff;
}
.il__footer_card__button {
  margin: 0 20px;
}
.il__footer__link {
  text-decoration: none;
}
</style>
