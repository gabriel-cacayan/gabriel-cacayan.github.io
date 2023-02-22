<template>
  <v-container>
    <v-row align="center" justify="center">
      <v-col cols="12" md="6">
        <v-img
          :src="landing"
          class="h-100 w-100"
          aspec-ration="1"
          cover
        ></v-img>
      </v-col>
      <v-col cols="12" md="6">
        <h1 class="text-h2">Gabriel Cacayan</h1>
        <p class="my-4 text-h6 text-grey">Software Developer</p>
      </v-col>
    </v-row>
    <div class="mt-10">
      <h1 class="text-h3">About Me</h1>
      <p class="text-h6 text-grey-darken-1 my-4">
        I'm Gab. I develop web applications. My core skill is based on Laravel
        and I am open for job opportunities that suits my interest and skills.
      </p>

      <v-row class="my-10">
        <v-col v-for="skill in skills" :key="skill.name" cols="4" sm="4" md="2">
          <v-sheet rounded border class="d-flex flex-column align-center pa-4">
            <v-icon :icon="skill.icon" size="x-large"></v-icon>
            <!-- <img
              src="https://img.icons8.com/ios-filled/256/mysql-logo.png"
              height="60"
              alt=""
            /> -->
            <p>{{ skill.name }}</p>
          </v-sheet>
        </v-col>
      </v-row>
    </div>
  </v-container>
</template>

<script>
import landing from "../assets/landing.svg";

export default {
  data() {
    return {
      landing: landing,
      skills: [
        {
          name: "HTML",
          icon: "mdi-language-html5",
        },
        {
          name: "CSS",
          icon: "mdi-language-css3",
        },
        {
          name: "JavaScript",
          icon: "mdi-language-javascript",
        },
        {
          name: "Bootstrap",
          icon: "mdi-bootstrap",
        },
        {
          name: "Tailwind",
          icon: "mdi-tailwind",
        },

        {
          name: "PHP",
          icon: "mdi-language-php",
        },
        {
          name: "Laravel",
          icon: "mdi-laravel",
        },
        {
          name: "Git",
          icon: "mdi-git",
        },
        {
          name: "Vue.js",
          icon: "mdi-vuejs",
        },
        {
          name: "Firebase",
          icon: "mdi-firebase",
        },
        {
          name: "MySQL",
          icon: "https://img.icons8.com/ios-filled/256/mysql-logo.png",
        },
      ],
    };
  },
};
</script>

<style></style>
