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
        <router-link
          class="il__teams__link"
          :to="{
            name: 'Team',
            path: '/team' + team.urlName,
            params: { team: team, teamName: team.urlName },
          }"
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
        </router-link>
      </v-card>
    </div>
    <footer-info />
  </div>
</template>

<script>
import HeaderBanner from "../components/HeaderBanner";
import Navigation from "../components/Navigation";
import FooterInfo from "../components/FooterInfo";

export default {
  name: "Teams",
  components: { FooterInfo, Navigation, HeaderBanner },
  data() {
    return {
      teams: [
        {
          name: "Alfa Romeo",
          id: 1,
          urlName: "alfaromeo",
          src: require("@/assets/img/teams/alfa_romeo.jpg"),
          pilots: [
            {
              id: 1,
              name: "A. Osadchiy",
              league: 1,
              status: "active",
            },
            {
              id: 2,
              name: "A. Zakharov",
              league: 1,
              status: "active",
            },
            {
              id: 3,
              name: "D. Tsvetkov",
              league: 2,
              status: "active",
            },
            {
              id: 4,
              name: "E. Bragin",
              league: 2,
              status: "active",
            },
          ],
        },
        {
          name: "Alpha Tauri",
          id: 2,
          urlName: "alphatauri",
          src: require("@/assets/img/teams/alpha_tauri.jpg"),
          pilots: [
            {
              id: 1,
              name: "S. Shibanov",
              league: 1,
              status: "active",
            },
            {
              id: 2,
              name: "A. Derbasov",
              league: 1,
              status: "active",
            },
            {
              id: 3,
              name: "V. Dronzikov",
              league: 2,
              status: "active",
            },
            {
              id: 4,
              name: "E. Khichin",
              league: 2,
              status: "active",
            },
          ],
        },
        {
          name: "Alpine",
          id: 3,
          urlName: "alpine",
          src: require("@/assets/img/teams/alpine.jpg"),
          pilots: [
            {
              id: 1,
              name: "A. Shilov",
              league: 1,
              status: "active",
            },
            {
              id: 2,
              name: "O. Antonenko",
              league: 1,
              status: "active",
            },
            {
              id: 3,
              name: "A. Alexeev",
              league: 2,
              status: "active",
            },
            {
              id: 4,
              name: "D. Poltorak",
              league: 2,
              status: "active",
            },
          ],
        },
        {
          name: "Aston Martin",
          id: 4,
          urlName: "astonmartin",
          src: require("@/assets/img/teams/aston_martin.jpg"),
          pilots: [
            {
              id: 1,
              name: "N. Savosin",
              league: 1,
              status: "active",
            },
            {
              id: 2,
              name: "A. Tomazov",
              league: 1,
              status: "active",
            },
            {
              id: 3,
              name: "W. Borg",
              league: 2,
              status: "active",
            },
            {
              id: 4,
              name: "A. Strelkov",
              league: 2,
              status: "active",
            },
          ],
        },
        {
          name: "Ferrari",
          id: 5,
          urlName: "ferrari",
          src: require("@/assets/img/teams/ferrari.jpg"),
          pilots: [
            {
              id: 1,
              name: "V. Pavlyukevich",
              league: 1,
              status: "active",
            },
            {
              id: 2,
              name: "A. Vlasov",
              league: 1,
              status: "active",
            },
            {
              id: 3,
              name: "A. Korzhikov",
              league: 2,
              status: "active",
            },
            {
              id: 4,
              name: "V. Bublyk",
              league: 2,
              status: "active",
            },
          ],
        },
        {
          name: "Haas",
          id: 6,
          urlName: "haas",
          src: require("@/assets/img/teams/haas.jpg"),
          pilots: [
            {
              id: 1,
              name: "R. Lavrov",
              league: 1,
              status: "active",
            },
            {
              id: 2,
              name: "S. Nevazgniy",
              league: 1,
              status: "active",
            },
            {
              id: 3,
              name: "D. Tymoshenko",
              league: 2,
              status: "active",
            },
            {
              id: 4,
              name: "M. Zhurkovich",
              league: 2,
              status: "active",
            },
          ],
        },
        {
          name: "McLaren",
          id: 7,
          urlName: "mclaren",
          src: require("@/assets/img/teams/mclaren.jpg"),
          pilots: [
            {
              id: 1,
              name: "V. Solomko",
              league: 1,
              status: "active",
            },
            {
              id: 2,
              name: "N. Sklyarenko",
              league: 1,
              status: "active",
            },
            {
              id: 3,
              name: "A. Perminow",
              league: 2,
              status: "active",
            },
            {
              id: 4,
              name: "M. Boyko",
              league: 2,
              status: "active",
            },
          ],
        },
        {
          name: "Mercedes",
          id: 8,
          urlName: "mercedes",
          src: require("@/assets/img/teams/mercedes.jpg"),
          pilots: [
            {
              id: 1,
              name: "S. Makin",
              league: 1,
              status: "active",
            },
            {
              id: 2,
              name: "A. Akhmetov",
              league: 1,
              status: "active",
            },
            {
              id: 3,
              name: "S. Belov",
              league: 2,
              status: "active",
            },
            {
              id: 4,
              name: "J. Stakanova",
              league: 2,
              status: "active",
            },
          ],
        },
        {
          name: "RedBull",
          id: 9,
          urlName: "redbull",
          src: require("@/assets/img/teams/red_bull.jpg"),
          pilots: [
            {
              id: 1,
              name: "N. Lipchenko",
              league: 1,
              status: "active",
            },
            {
              id: 2,
              name: "S. Kryukov",
              league: 1,
              status: "active",
            },
            {
              id: 3,
              name: "S. Bortsova",
              league: 2,
              status: "active",
            },
            {
              id: 4,
              name: "A. Dzis",
              league: 2,
              status: "active",
            },
          ],
        },
        {
          name: "Williams",
          id: 10,
          urlName: "williams",
          src: require("@/assets/img/teams/williams.jpg"),
          pilots: [
            {
              id: 1,
              name: "I. Shurakov",
              league: 1,
              status: "active",
            },
            {
              id: 2,
              name: "A. Pogodin",
              league: 1,
              status: "active",
            },
            {
              id: 3,
              name: "E. Chander",
              league: 2,
              status: "active",
            },
            {
              id: 4,
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
.il__teams__link {
  text-decoration: none;
}
</style>
