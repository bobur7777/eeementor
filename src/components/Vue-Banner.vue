<template>
  <div class="banner-sec">
    <div class="container">
      <div class="banner-text">
        <h1 class="title">Присоединяйтесь к E-Mentor сейчас</h1>
        <p class="text">
          Выберите подходящий тариф и формат обучения, пройдите 2 урока и мы
          подарим вам дополнительные лекции по любому направлению бесплатно!
        </p>
        <button class="btn">Выбрать тариф</button>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "banner-sec",
};
</script>
<style scoped>
.banner-sec {
  position: relative;
  margin: 250px 0;
  width: 100%;
  height: 578px;
  background-image: url(../assets/banner/bg.png);
  background-repeat: no-repeat;
  background-position: center;
}
.container {
  position: relative;
  width: 1170px;
  height: 578px;
}
.banner-text {
  position: absolute;
  width: 45%;
  height: 100%;
  left: 50%;
}
.title {
  margin-top: 120px;
  width: 100%;
  font-family: Raleway;
  font-size: 58px;
  font-weight: 500;
  line-height: 70px;
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
.btn {
  height: 56px;
  width: 230px;
  margin-top: 50px;
  border-radius: 0 20px 0 20px;
  background: #fa9f42;
  border: none;

  font-family: Raleway;
  font-size: 16px;
  font-weight: 500;
  line-height: 16px;
  letter-spacing: 0em;
  text-align: center;
  color: #fdfdfd;
}
</style>