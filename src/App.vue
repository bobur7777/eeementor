<template>
  <div id="app">
    <router-view />

    <Header />
    <Statystic />
    <Teachers />
    <Choose />
    <AllCourses />
    <VueBannerSec />
    <Footer />
  </div>
</template>

<script>
import Header from "@/components/Header.vue"
import Statystic from "@/components/Statystic.vue"
import Teachers from "@/components/Teachers.vue"
import Choose from "@/components/Choose.vue"
import AllCourses from "@/components/All-courses.vue"
import VueBannerSec from "@/components/Vue-Banner.vue"
import Footer from "@/components/Vue-Footer.vue"

export default {
  name: "App",
  components: {
    Header,
    Statystic,
    Teachers,
    Choose,
    AllCourses,
    VueBannerSec,
    Footer,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Raleway:wght@400;500&display=swap");

* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
ul li {
  list-style: none;
}
a {
  text-decoration: none;
}
.container {
  width: 1170px;
  margin: 0 auto;
}
</style>
