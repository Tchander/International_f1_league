<template>
  <nav class="navigation">
    <router-link class="logo__link" to="/">
      <img class="logo__img" src="../assets/img/il_logo.jpg" alt="logo" />
      <div class="logo__home">Главная</div>
    </router-link>
    <div class="navigation__links">
      <router-link class="navigation__link" to="/calendar"
        >Календарь</router-link
      >
      <router-link class="navigation__link" to="/tournament_table"
        >Турнирная таблица</router-link
      >
      <router-link class="navigation__link" to="/teams">Команды</router-link>
    </div>
  </nav>
</template>

<script>
export default {
  name: "Navigation",
};
</script>

<style scoped>
.navigation {
  width: 100%;
  max-width: 1440px;
  margin: 0 auto 40px auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.logo__link {
  display: flex;
  justify-content: space-between;
  align-items: center;
  text-decoration: none;
}
.logo__img {
  width: 60px;
  height: 60px;
  border-radius: 50%;
}
.logo__home {
  margin-left: 20px;
  text-decoration: none;
  list-style-type: none;
  color: #cee2f6;
}
.logo__home:hover {
  color: #fff;
}
.navigation__link {
  text-decoration: none;
  list-style-type: none;
  margin-left: 35px;
  color: #cee2f6;
}
.navigation__link:hover {
  color: #fff;
}
</style>
