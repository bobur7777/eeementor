<template>
  <div class="all-courses">
    <div class="container">
      <div class="courses">
        <div class="cours" v-for="cours in courses" :key="cours.id">
          <img :src="getImageUrl(cours.url)" alt="" />
          <p class="text">
            {{ cours.text }}
          </p>
        </div>
      </div>
      <button class="btn">Все курсы</button>
    </div>
  </div>
</template>
<script>
export default {
  name: "all-courses",
  data() {
    return {
      courses: [
        { id: 1, text: "Motion design", url: "1.svg" },
        { id: 2, text: "Таргет в Instagram", url: "2.svg" },
        { id: 3, text: "Эффектные презентации", url: "3.svg" },
        { id: 4, text: "SMM-стратегия", url: "4.svg" },
      ],
    };
  },

  methods: {
    getImageUrl(img) {
      return require("../assets/all-courses/" + img);
    },
  },
};
</script>

<style scoped>
.courses {
  margin: 90px 0;
  display: flex;
  justify-content: space-between;
}
.cours {
  height: 226px;
  width: 270px;
  left: 135px;
  top: 2578.9999999999995px;
  border-radius: 10px;
  background: #fdfdfd;
  box-shadow: 5px 5px 30px 0px #6565651f;
  display: flex;
  flex-direction: column;
}
img {
  padding: 20px;
}
.text {
  font-family: Raleway;
  font-size: 16px;
  font-weight: 500;
  line-height: 16px;
  letter-spacing: 0em;
  text-align: left;
  color: #353a5a;
  padding-left: 20px;
}
.btn {
  position: absolute;
  height: 56px;
  width: 230px;
  border-radius: 0 20px 0 20px;
  border: none;
  background: #10b582;
  display: flex;
  justify-content: center;
  align-items: center;
  left: 50%;
  transform: translate(-50%);

  font-family: Raleway;
  font-size: 16px;
  font-weight: 500;
  line-height: 16px;
  letter-spacing: 0em;
  text-align: center;
  color: #fdfdfd;
}
</style>