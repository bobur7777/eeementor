<template>
  <div class="app">
    <div class="container">
      <nav class="nav">
        <ul class="nav__list">
          <li class="list__item" v-for="nav in navs" :key="nav.id">
            <a href="#">
              {{ nav.name }}
            </a>
          </li>
        </ul>
      </nav>
      <div class="header__content">
        <div class="left__coloumn">
          <div class="cotial">
            <img
              :src="getCotialUrl(cotial.url)"
              class="cotial__links"
              v-for="cotial in cotials"
              :key="cotial.id"
            />
          </div>
          <img src="../assets/header/left.png" alt="" />
        </div>
        <div class="center__coloumn">
          <img src="../assets/header/logo.svg" alt="" class="logo" />
          <h1 class="title">Образовательная онлайн-платформа</h1>
          <p class="text">
            Курсы и видео-лекции по дизайну, копирайтингу, SMM, таргету и многим
            другим направлениям
          </p>
          <button class="btn">Все направления</button>
        </div>
        <div class="right__coloumn">
          <img class="img" src="../assets/header/right.png" />
          <div class="scroll">
            <img src="../assets/header/icons/arrow-left.svg" alt="" />
            <p>Листайте вниз</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "app",
  data() {
    return {
      navs: [
        { id: 1, name: "О нас", sendUrl: "" },
        { id: 2, name: "Платформа", sendUrl: "" },
        { id: 3, name: "Курсы", sendUrl: "" },
        { id: 4, name: "Лекции", sendUrl: "" },
        { id: 5, name: "Тарифы", sendUrl: "" },
        { id: 6, name: "Блог", sendUrl: "" },
        { id: 7, name: "Контакты", sendUrl: "" },
      ],
      cotials: [
        { id: 1, name: "facebook", url: "facebook.svg" },
        { id: 2, name: "vk", url: "vk.svg" },
        { id: 3, name: "instagram", url: "instagram.svg" },
      ],
    };
  },
  methods: {
    getCotialUrl(pic) {
      return require("../assets/header/" + pic);
    },
  },
};
</script>

<style scoped>
.app {
  border-radius: 0px;
  background: #10b582;
}
.container {
  min-height: 400px;
}
nav ul {
  display: flex;
  justify-content: center;
}
nav ul li{
  padding: 20px;
}
nav ul li a:hover {
  border-bottom: 3px dashed #FA9F42
}
nav ul li a {
  font-family: Raleway;
  font-size: 16px;
  font-weight: 500;
  line-height: 16px;
  letter-spacing: 0em;
  text-align: left;
  color: #fdfdfd;
  transition: 0.1s;
}
.header__content {
  margin-top: 20px;
  position: relative;
  width: 100%;
  height: 560px;
  bottom: 1px solid red;
  display: flex;
  justify-content: space-between;
}
.left__coloumn {
  position: relative;
  height: 90%;
  flex: 1;
}
.center__coloumn {
  position: relative;
  height: 90%;
  flex: 2;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.right__coloumn {
  position: relative;
  position: relative;
  height: 90%;
  flex: 1;
}
.center__coloumn .title {
  font-family: Raleway;
  font-size: 58px;
  font-weight: 500;
  line-height: 70px;
  letter-spacing: 0em;
  text-align: center;
  color: #fdfdfd;
}
.center__coloumn .text {
  font-family: Raleway;
  font-size: 16px;
  font-weight: 400;
  line-height: 24px;
  letter-spacing: 0em;
  text-align: center;
  color: #fdfdfd;
  padding: 20px 50px;
}
.center__coloumn .btn {
  margin-top: 50px;
  height: 56px;
  width: 230px;
  background: #fa9f42;
  color: #fdfdfd;
  border: none;
  cursor: pointer;

  font-family: Raleway;
  font-size: 16px;
  font-weight: 500;
  line-height: 16px;
  letter-spacing: 0em;
  text-align: center;
}
.cotial {
  display: flex;
  flex-direction: column;
}
.cotial img {
  width: 22px;
  margin-bottom: 30px;
}
.scroll {
  width: 130px;
  display: flex;
  position: absolute;
  left: 67%;
  top: 85%;
  transform: rotate(270deg);
  cursor: pointer;
}
.scroll p {
  font-family: Raleway;
  font-size: 14px;
  font-weight: 400;
  line-height: 14px;
  letter-spacing: 0em;
  text-align: center;
  color: #fdfdfd;
  margin-left: 10px;
}
</style>
