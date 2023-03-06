<template>
  <v-container class="mb-10">
    <h1 class="text-center my-4" v-if="!selectedProject">Projects</h1>
    <v-row v-if="!selectedProject">
      <v-col
        v-for="project in projects"
        :key="project.name"
        cols="12"
        sm="4"
        md="6"
      >
        <v-card class="mx-auto" max-width="400" v-ripple border>
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

          <v-card-actions class="d-flex justify-space-between">
            <v-btn color="orange" @click="selectProject(project.name)"
              >View</v-btn
            >

            <p class="text-grey-darken-1">
              {{ project.dateCreated }}
            </p>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>

    <template v-if="selectedProject == 'Vue Movie'">
      <div class="d-flex justify-end">
        <v-btn
          prepend-icon="mdi-arrow-left"
          variant="outlined"
          color="info"
          @click="selectProject(null)"
          >Go Back</v-btn
        >
      </div>
      <VueMovie />
    </template>
    <template v-else-if="selectedProject == 'Yowndrift'">
      <div class="d-flex justify-end">
        <v-btn
          prepend-icon="mdi-arrow-left"
          variant="outlined"
          color="info"
          @click="selectProject(null)"
          >Go Back</v-btn
        >
      </div>
      <Yowndrift />
    </template>
  </v-container>
</template>

<script>
import y0 from "../assets/yowndrift/y0.jpg";
import v0 from "../assets/vue_movie/v0.jpg";
import Yowndrift from "./YowndriftDetail.vue";
import VueMovie from "./VueMovieDetail.vue";

export default {
  components: {
    Yowndrift,
    VueMovie,
  },
  data() {
    return {
      selectedProject: null,
      projects: [
        {
          img: v0,
          name: "Vue Movie",
          technology: "Vue.js",
          description:
            "Vue Movie is an online database of information related to films, television series, ratings, and reviews.",
          link: "",
          dateCreated: "2-18-2023",
        },
        {
          img: y0,
          name: "Yowndrift",
          technology: "Laravel",
          description:
            "Yowndrift is a blog web application, where anyone can share their ideas or knowledge on a specific topic.",
          link: "",
          dateCreated: "5-10-2021",
        },
      ],
    };
  },
  methods: {
    selectProject: function (name) {
      this.selectedProject = name;
    },
  },
};
</script>

<style></style>
