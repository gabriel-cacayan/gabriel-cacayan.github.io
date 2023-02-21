<template>
  <v-container>
    <h1 class="text-center my-4">Projects</h1>
    <v-row>
      <v-col
        v-for="project in projects"
        :key="project.name"
        cols="12"
        sm="4"
        md="6"
      >
        <v-card class="mx-auto" max-width="400" v-ripple>
          <v-img
            class="align-end text-white"
            height="400"
            :src="project.img"
            cover
          >
          </v-img>
          <v-card-title>{{ project.name }}</v-card-title>
          <v-card-subtitle>{{ project.technology }}</v-card-subtitle>
          <v-card-text>
            <div class="text-truncate">
              {{ project.description }}
            </div>
          </v-card-text>

          <v-card-actions>
            <v-btn color="orange">View</v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import yowndriftHomeMobile from "../assets/yowndrift/yowndrift_home_mobile.jpg";
import vueMovie from "../assets/vue_movie/vue_movie.png";

export default {
  data() {
    return {
      projects: [
        {
          img: vueMovie,
          name: "Vue Movie",
          technology: "Vue.js",
          description:
            "Vue Movie is an online database of information related to films, television series, music videos, podcasts, home videos, video games, and streaming content online including cast, production crew and personal biographies, plot summaries, trivia, ratings, and fan and critical reviews.",
          link: "",
        },
        {
          img: yowndriftHomeMobile,
          name: "Yowndrift",
          technology: "Laravel",
          description:
            "Yowndrift is a blog web application, where anyone can share their ideas or knowledge on a specific topic.",
          link: "",
        },
      ],
    };
  },
};
</script>

<style></style>
