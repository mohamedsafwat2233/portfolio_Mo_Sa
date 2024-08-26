<template>
  <v-app id="home">
    <NavBar />

    <v-container fluid>
      <div class="head">
        <v-row>
          <v-col class="col-sm-12 col-md-8">
            <div style="position:relative;left:27%" class="mt-16 ps-5">
              <h1 class="text-grey" style="font-size:30px ">Hello,</h1>
              <h1 class="text-white" style="font-size:55px ">I'm Mohamed Safwat abdelgaber</h1>
              <span class="text-grey fs-sm-5">a full stack developer</span>
              <br />
              <v-btn tile class="text-green mt-8" variant="outlined">contact me</v-btn>
            </div>
          </v-col>

          <v-col cols="2">
            <div
              style="
                position: absolute;
                z-index: 9999;
                bottom: 0;
                margin-left: auto;
                margin-right: auto;
                left: 0;
                right: 0;
                text-align: center;
              "
              class="mt-16"
            >
              <v-icon>fas fa-angle-double-down</v-icon>
            </div>
          </v-col>

          <v-col cols="5">
            <div style="position: relative; z-index: 9999" class="mt-16">
              <v-avatar color="grey" size="270" rounded="5">
                <v-img class="ms-0" src="../assets/IMG_20231219_000139_252.jpg" contain max-height="270"></v-img>
              </v-avatar>
            </div>
          </v-col>
        </v-row>
      </div>

      <v-container id="skills">
        <h1 class="text-center mt-10 " style="font-size:45px">Skills</h1>
        <v-container>
          <v-row class="d-flex justify-content-center">
            <v-col cols="6" class="mt-6">
              <Skills :skills="front_skills" title="front"></Skills>
            </v-col>
            <v-col cols="6" class="mt-6">
              <Skills :skills="back_skills" title="back"></Skills>
            </v-col>
          </v-row>

          <v-row class="mx-5 " >
            <v-col cols="6"  md="12" class=" mt-6 " >
              <Skills :skills="db_skills" title="Database"></Skills>
            </v-col>
          </v-row>

        </v-container>
      </v-container>

      <v-container id="about">
        <h1 class="text-center mt-10" style="font-size:55px">About me</h1>
        <v-row class="d-flex justify-content-center">
          <v-col cols="12" class="mt-6 text-start">
            <h4 class="mt-n4">I am a Creative full stack web developer</h4>
            <Panel header="Header">
              <p class="m-0">
                Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
                consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
              </p>
            </Panel>
            <v-btn tile dark color="green" class="mt-4">Download Resume</v-btn>
          </v-col>
        </v-row>
      </v-container>
    </v-container>

    <Footer />
  </v-app>
</template>

<script>
import { defineComponent } from "vue";
import NavBar from "@/components/navbar.vue";
import Footer from "@/components/footer.vue";
import Skills from "@/components/skills.vue";
export default defineComponent({
  name: "HomeView",
  components: {
    NavBar,
    Footer,
    Skills
  },
  data() {
    return {
      front_skills: [
        "skills/front/HTML5.png",
        "skills/front/CSS3.svg",
        "skills/front/JS.webp",
        "skills/front/typescript.png",
        "skills/front/React_logo.png",
        "skills/front/vuejs.png"
      ],
      back_skills: [
        "skills/back/laravell.png",
        "skills/back/php.png",
        "skills/back/nodejs.png",
        "skills/back/Python.png"
      ],
      db_skills: [
        "skills/db/mysql.png",
        "skills/db/MongoDB-Logo.png",
      ]
    };
  }
});
</script>

<style scoped>
.v-container {
  padding: 16px 0;
}
.head {
  position: relative;
  text-align: center;
  padding: 12px;
  margin-bottom: 6px;
  height: 400px;
  width: 100%;
  color: white;
}
.head:before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 50%;
  background: rgb(98, 238, 161);
  transform: skew(0deg, 6deg);
}
.head:after {
  content: "";
  position: absolute;
  top: 0;
  right: 0;
  height: 100%;
  width: 50%;
  background: rgb(110, 91, 216);
  transform: skew(0deg, -6deg);
}
.egg {
  display: block;
  margin-left: 100px;
  margin-top: 50px;
  width: 356px;
  height: 300px;
  background-color: #fbdf7e;
  border-radius: 50% 50% 50% 50% / 60% 60% 40% 40%;
}
</style>