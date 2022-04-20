<template>
  <div class="choose-form">
    <div class="container">
      <div class="img">
        <img src="../assets/choose-form/img.png" alt="" />
      </div>
      <div class="choose-text">
        <h1 class="title">Выбирайте свой формат обучения</h1>
        <p class="text">
          Смотрите видео-лекции в удобное для вас время, обучайтесь на
          тренажере, участвуйте в интенсивных воркшопах с командой или проходите
          курс с гибким расписанием. На нашей платформе каждый найдет подходящий
          формат.
        </p>
        <button class="btn">Все курсы</button>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "choose-form",
};
</script>
<style scoped>
.choose-form {
  width: 100%;
  background: #10b582;
}
.container {
  padding: 120px 0;
  display: flex;
  justify-content: space-between;
}
.img {
  width: 48%;
}
.img img{
    width: 500px;
}
.choose-text {
  display: flex;
  flex-direction: column;
  width: 48%;
}
.title {
  font-family: Raleway;
  font-size: 58px;
  font-weight: 500;
  line-height: 70px;
  letter-spacing: 0em;
  text-align: left;
  color: #fdfdfd;
}
.text {
  padding-top: 20px;
  font-family: Raleway;
  font-size: 16px;
  font-weight: 400;
  line-height: 24px;
  letter-spacing: 0em;
  text-align: left;
  color: #fdfdfd;
}
.btn {
  margin-top: 50px;
  height: 56px;
  width: 230px;
  left: 700px;
  top: 2333.9999999999995px;
  border-radius: 0 20px 0 20px;
  border: none;
  background: #fa9f42;

  font-family: Raleway;
  font-size: 16px;
  font-weight: 500;
  line-height: 16px;
  letter-spacing: 0em;
  text-align: center;
  color: #fdfdfd;
}
</style>