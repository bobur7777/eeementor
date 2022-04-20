<template>
  <div id="app">
    <div class="container">
      <div class="box" v-for="statystic in statystics" :key="statystic.id">
        <h1 class="number">{{ statystic.number }}</h1>
        <p class="text">{{ statystic.text }}</p>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "app",
  data() {
    return {
      statystics: [
        {
          id: 1,
          text: "теоретических и практических курсов для разного уровня",
          number: "100+",
        },
        {
          id: 2,
          text: "часов видео-лекций и вебинаров от лучших преподавателей",
          number: "3 000",
        },
        {
          id: 3,
          text: "направлений обучения востребованным профессиям",
          number: "15",
        },
        {
          id: 4,
          text: "учеников уже занимаются на нашей платформе",
          number: "2 000",
        },
      ],
    };
  },
};
</script>
<style scoped>
.container {
  display: flex;
  justify-content: space-between;
  padding: 40px 0;
}
.box {
  width: 25%;
  padding: 20px;
  text-align: center;
}
.number {
  color: #10b582;
  font-family: Raleway;
  font-size: 58px;
  font-weight: 500;
  line-height: 58px;
  letter-spacing: 0em;
  text-align: center;
}
.text {
  padding: 20px;
  font-family: Raleway;
  font-size: 14px;
  font-weight: 400;
  line-height: 17px;
  letter-spacing: 0em;
  text-align: center;
}
</style>
