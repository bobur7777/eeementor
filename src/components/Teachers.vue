<template>
  <div class="app">
    <div class="container">
      <div class="teachers__text">
        <h1 class="text__title">Учитесь у лучших</h1>
        <p class="text">
          Наши преподаватели – профессионалы, которые добились успеха в своей
          области. Лид-дизайнеры известных студий, маркетологи крупнейших
          компаний, редакторы популярных медиа: получайте опыт из первых рук, в
          любое время. <br />
          Кураторы курсов – наши лучшие выпускники, будут помогать и
          поддерживать вас на протяжении всего обучения.
        </p>
        <button class="btn">Все преподаватели</button>
      </div>
      <div class="teachers__info">
        <div class="box" v-for="teacher in teachers" :key="teacher.id">
          <img :src="getImagesUrl(teacher.img)" alt="?" />
          <p class="name">
            {{ teacher.name }}
          </p>
          <p class="work">
            {{ teacher.work }}
          </p>
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
      teachers: [
        {
          id: 1,
          name: "Катя, ведущий дизайнер",
          work: "TailGroup",
          img: "1.png",
        },
        {
          id: 1,
          name: "Марина, маркетолог",
          work: "Headers Market",
          img: "2.png",
        },
        {
          id: 1,
          name: "Сава, PR-менеджер",
          work: "Central Media",
          img: "3.png",
        },
        { id: 1, name: "Паша, основатель", work: "LeadCompany", img: "4.png" },
        {
          id: 1,
          name: "Саша, главный редактор",
          work: "Just Journal",
          img: "5.png",
        },
        {
          id: 1,
          name: "Лёня, ведущий",
          work: "разработчик Ymail",
          img: "6.png",
        },
      ],
    };
  },
  methods: {
    getImagesUrl(pic) {
      return require("../assets/teachers/" + pic);
    },
  },
};
</script>
<style scoped>
.container {
  display: flex;
  justify-content: space-between;
}
.teachers__text {
  display: flex;
  align-self: center;
  flex-direction: column;
}
.btn {
    margin-top: 50px;

  height: 56px;
  width: 230px;
  left: 135px;
  top: 1498.9999999999995px;
  border-radius: [object Object]px;
  background: #10b582;
  border-radius: 0 20px 0 20px;
  border: none;

  font-family: Raleway;
  font-size: 16px;
  font-weight: 500;
  line-height: 16px;
  letter-spacing: 0em;
  text-align: center;
  color: #FDFDFD;
}

.teachers__text,
.teachers__info {
  width: 48%;
}

.text__title {
  font-family: Raleway;
  font-size: 58px;
  font-weight: 500;
  line-height: 58px;
  letter-spacing: 0em;
  text-align: left;
  color: #353a5a;
}
.text {
  margin-top: 20px;
  font-family: Raleway;
  font-size: 16px;
  font-weight: 400;
  line-height: 24px;
  letter-spacing: 0em;
  text-align: left;
  color: #353a5a;
}

.teachers__info {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  align-items: center;
}
.box {
  padding: 31px 0;
}
.teachers__info img {
  margin-bottom: 15px;
}
.name,
.work {
  text-align: center;
  font-family: Raleway;
  font-size: 14px;
  font-weight: 400;
  line-height: 18px;
  letter-spacing: 0em;
  text-align: center;
}
</style>