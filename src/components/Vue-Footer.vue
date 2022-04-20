<template>
  <div class="VueFooter">
    <div class="container">
      <div class="footer-main">
        <div class="logo">
          <img src="../assets/footer/logotype.svg" alt="" class="img" />
          <p class="text">
            Образовательная онлайн-платформа для развития и тренировки навыков в
            сфере информационных технологий
          </p>
          <div class="cotial">
            <img
              v-for="link in links"
              :key="link.id"
              :src="getUrl(link.url)"
              alt=""
            />
          </div>
        </div>
        <div class="info">
          <div class="box" v-for="box in boxses" :key="box.id">
            <h1 class="name">
              {{ box.name }}
            </h1>
            <p class="text">
              {{ box.first }} <br />
              {{ box.second }} <br />
              {{ box.third }} <br />
              {{ box.fourth }}
            </p>
          </div>
        </div>
      </div>
      <div class="footer-bootom"></div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      boxses: [
        {
          id: 1,
          name: "Обучение",
          first: "Курсы",
          second: "Вебинары",
          third: "Тренажеры",
          fourth: "Воркшопы",
        },
        {
          id: 2,
          name: "О нас",
          first: "О платформе",
          second: "Преподаватели",
          third: "Тарифы",
          fourth: "Отзывы",
        },
        {
          id: 3,
          name: "Контакты",
          first: "Связаться с нами",
          second: "Консультация",
          third: "Реквизиты",
          fourth: "Поддержка",
        },
        {
          id: 4,
          name: "Возникли вопросы?",
          first: "Напишите нам на почту education@ementor.info",
        },
      ],
      links: [
        { id: 1, name: "facebook", url: "facebook.svg" },
        { id: 2, name: "vk", url: "vk.svg" },
        { id: 3, name: "instagram", url: "instagram.svg" },
      ],
    };
  },
  methods: {
    getUrl(pic) {
      return require("../assets/footer/" + pic);
    },
  },
};
</script>

<style scoped>
.footer-main {
  display: flex;
}
.logo {
  flex: 2;
  padding: 25px;
}
.logo img {
  margin-right: 25px;
  left:0%
}
.info {
  display: flex;
  flex: 5;
  padding: 25px;
}
.box {
  width: 25%;
}
.name {
  font-family: Raleway;
  font-size: 16px;
  font-weight: 500;
  line-height: 16px;
  letter-spacing: 0em;
  text-align: left;
  margin-bottom: 31px;
  color: #353a5a;
}
.text {
  margin-top: 27px;
  font-family: Raleway;
  font-size: 16px;
  font-weight: 400;
  line-height: 25px;
  padding-bottom: 20px;
  letter-spacing: 0em;
  text-align: left;

  color: #353a5a;
}
.cotial {
  margin-top: 7px;
}
</style>