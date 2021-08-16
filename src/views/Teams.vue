<template>
  <div>
    <header-banner :is-home="false" />
    <div class="il__container">
      <navigation />
      <v-card
        class="il__card"
        v-for="(team, index) in teams"
        :key="index"
        color="#242c41"
        style="border: 1px solid #fff"
      >
        <v-card-title class="il__card__title">{{ team.name }}</v-card-title>
        <v-card-text class="il__card__content">
          <v-img :src="team.src" class="il__card__image"></v-img>
          <div class="il__card__text__content">
            <div v-for="(pilot, i) in team.pilots" :key="i">
              <h3
                class="il__card__text__content__league"
                v-if="pilot.league === 1 && i !== 1"
              >
                Лига 1
              </h3>
              <h4
                class="il__card__text__content__pilot"
                v-if="pilot.league === 1"
              >
                {{ i + 1 }}. {{ pilot.name }}
              </h4>
              <h3
                class="il__card__text__content__league"
                v-if="pilot.league === 2 && i !== 3"
              >
                Лига 2
              </h3>
              <h4
                class="il__card__text__content__pilot"
                v-if="pilot.league === 2"
              >
                {{ i - 1 }}. {{ pilot.name }}
              </h4>
            </div>
          </div>
        </v-card-text>
      </v-card>
    </div>
  </div>
</template>

<script>
import HeaderBanner from "../components/HeaderBanner";
import Navigation from "../components/Navigation";

export default {
  name: "Teams",
  components: { Navigation, HeaderBanner },
  data() {
    return {
      teams: [
        {
          name: "Alfa Romeo",
          src: require("@/assets/img/teams/alfa_romeo.jpg"),
          pilots: [
            {
              name: "A. Osadchiy",
              league: 1,
              status: "active",
            },
            {
              name: "A. Zakharov",
              league: 1,
              status: "active",
            },
            {
              name: "D. Tsvetkov",
              league: 2,
              status: "active",
            },
            {
              name: "E. Bragin",
              league: 2,
              status: "active",
            },
          ],
        },
        {
          name: "Alpha Tauri",
          src: require("@/assets/img/teams/alpha_tauri.jpg"),
          pilots: [
            {
              name: "S. Shibanov",
              league: 1,
              status: "active",
            },
            {
              name: "A. Derbasov",
              league: 1,
              status: "active",
            },
            {
              name: "V. Dronzikov",
              league: 2,
              status: "active",
            },
            {
              name: "E. Khichin",
              league: 2,
              status: "active",
            },
          ],
        },
        {
          name: "Alpine",
          src: require("@/assets/img/teams/alpine.jpg"),
          pilots: [
            {
              name: "A. Shilov",
              league: 1,
              status: "active",
            },
            {
              name: "O. Antonenko",
              league: 1,
              status: "active",
            },
            {
              name: "A. Alexeev",
              league: 2,
              status: "active",
            },
            {
              name: "D. Poltorak",
              league: 2,
              status: "active",
            },
          ],
        },
        {
          name: "Aston Martin",
          src: require("@/assets/img/teams/aston_martin.jpg"),
          pilots: [
            {
              name: "N. Savosin",
              league: 1,
              status: "active",
            },
            {
              name: "A. Tomazov",
              league: 1,
              status: "active",
            },
            {
              name: "W. Borg",
              league: 2,
              status: "active",
            },
            {
              name: "A. Strelkov",
              league: 2,
              status: "active",
            },
          ],
        },
        {
          name: "Ferrari",
          src: require("@/assets/img/teams/ferrari.jpg"),
          pilots: [
            {
              name: "V. Pavlyukevich",
              league: 1,
              status: "active",
            },
            {
              name: "A. Vlasov",
              league: 1,
              status: "active",
            },
            {
              name: "A. Korzhikov",
              league: 2,
              status: "active",
            },
            {
              name: "V. Bublyk",
              league: 2,
              status: "active",
            },
          ],
        },
        {
          name: "Haas",
          src: require("@/assets/img/teams/haas.jpg"),
          pilots: [
            {
              name: "R. Lavrov",
              league: 1,
              status: "active",
            },
            {
              name: "S. Nevazgniy",
              league: 1,
              status: "active",
            },
            {
              name: "D. Tymoshenko",
              league: 2,
              status: "active",
            },
            {
              name: "M. Zhurkovich",
              league: 2,
              status: "active",
            },
          ],
        },
        {
          name: "McLaren",
          src: require("@/assets/img/teams/mclaren.jpg"),
          pilots: [
            {
              name: "V. Solomko",
              league: 1,
              status: "active",
            },
            {
              name: "N. Sklyarenko",
              league: 1,
              status: "active",
            },
            {
              name: "A. Perminow",
              league: 2,
              status: "active",
            },
            {
              name: "M. Boyko",
              league: 2,
              status: "active",
            },
          ],
        },
        {
          name: "Mercedes",
          src: require("@/assets/img/teams/mercedes.jpg"),
          pilots: [
            {
              name: "S. Makin",
              league: 1,
              status: "active",
            },
            {
              name: "A. Akhmetov",
              league: 1,
              status: "active",
            },
            {
              name: "S. Belov",
              league: 2,
              status: "active",
            },
            {
              name: "J. Stakanova",
              league: 2,
              status: "active",
            },
          ],
        },
        {
          name: "RedBull",
          src: require("@/assets/img/teams/red_bull.jpg"),
          pilots: [
            {
              name: "N. Lipchenko",
              league: 1,
              status: "active",
            },
            {
              name: "S. Kryukov",
              league: 1,
              status: "active",
            },
            {
              name: "S. Bortsova",
              league: 2,
              status: "active",
            },
            {
              name: "A. Dzis",
              league: 2,
              status: "active",
            },
          ],
        },
        {
          name: "Williams",
          src: require("@/assets/img/teams/williams.jpg"),
          pilots: [
            {
              name: "I. Shurakov",
              league: 1,
              status: "active",
            },
            {
              name: "A. Pogodin",
              league: 1,
              status: "active",
            },
            {
              name: "E. Chander",
              league: 2,
              status: "active",
            },
            {
              name: "D. Bondarev",
              league: 2,
              status: "active",
            },
          ],
        },
      ],
    };
  },
};
</script>

<style scoped>
.il__card {
  margin-bottom: 20px;
  border-radius: 20px;
}
.il__card__title {
  color: #fff;
  font-size: 26px;
  font-weight: 700;
}
.il__card__content {
  display: flex;
}
.il__card__image {
  max-width: 750px;
}
.il__card__text__content {
  width: 100%;
  text-align: left;
  padding: 15px 0 0 40px;
}
.il__card__text__content__league {
  color: #fff;
  margin: 60px 0 20px 0;
  font-size: 20px;
}
.il__card__text__content__pilot {
  color: #fff;
  font-size: 18px;
  font-weight: 400;
  margin-bottom: 15px;
}
</style>
