<template>
  <v-footer color="rgb(36, 44, 65)">
    <v-card flat tile class="il__footer__card">
      <v-card-text class="footer__card__text">
        <v-btn
          class="footer_card__button"
          v-for="icon in icons"
          :key="icon"
          icon
        >
          <a
            v-if="icon === 'mdi-vk'"
            class="footer__link"
            href="https://vk.com/f1ileague"
            target="_blank"
          >
            <v-icon color="#fff" size="40px">
              {{ icon }}
            </v-icon>
          </a>
          <a
            v-if="icon === 'mdi-telegram'"
            class="footer__link"
            href="https://t.me/joinchat/JmWgNEOkS9tfo58lIOBhhw"
            target="_blank"
          >
            <v-icon color="#fff" size="40px">
              {{ icon }}
            </v-icon>
          </a>
          <a
            v-if="icon === 'mdi-youtube'"
            class="footer__link"
            href="https://youtube.com/channel/UC9F7VXNzjL4y07XXao0D4PQ"
            target="_blank"
          >
            <v-icon color="#fff" size="40px">
              {{ icon }}
            </v-icon>
          </a>
          <a
            v-if="icon === 'mdi-discord'"
            class="footer__link"
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
.footer__card__text {
  background-color: rgb(36, 44, 65);
  color: #fff;
}
.footer_card__button {
  margin: 0 20px;
}
.footer__link {
  text-decoration: none;
}
</style>
