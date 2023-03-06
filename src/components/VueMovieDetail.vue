<template>
  <v-container>
    <h1 class="text-h3 my-4">About the project</h1>
    <p class="mb-4">
      Vue Movie is an online database of information related to films,
      television series, ratings, and reviews.
    </p>
    <v-divider class="my-4"></v-divider>
    <h1 class="text-h3 mt-10 mb-4">Features</h1>
    <ul class="mb-4">
      <li>
        Allow users to search for movies based on various criteria, such as
        movie, peopl or tv. Also, allow users to browse movies based on popular
        or new releases, trending topics, or recommended titles.
      </li>
      <li>
        Provide users with detailed information about each movie, including plot
        summary, cast and crew, rating, reviews, and related movies. Allow users
        to rate and review movies they have watched and see the average rating
        and reviews from other users.
      </li>
      <li>
        Ensure the web application is responsive and optimized for mobile
        devices, such as smartphones and tablets, to provide a seamless and
        convenient user experience on the go.
      </li>
    </ul>
    <v-divider class="my-4"></v-divider>
    <h1 class="text-h3 mt-10 mb-4">Platform Type</h1>
    <p class="mb-4">Web App</p>
    <v-divider class="my-4"></v-divider>
    <h1 class="text-h3 mt-10 mb-4">Technologies used</h1>
    <h3 class="mb-4">For front-end:</h3>
    <ul class="mb-4">
      <li>Vue.js</li>
      <li>Vuetify</li>
    </ul>
    <h3 class="mb-4">For back-end:</h3>
    <ul class="mb-4">
      <li>API</li>
    </ul>

    <div class="mt-10">
      <v-btn
        variant="outlined"
        append-icon="mdi-code-braces"
        href="https://github.com/gabriel-cacayan/vue-movie"
        :class="displayBlock"
        target="_blank"
        >Source Code</v-btn
      >
      <v-btn
        variant="tonal"
        color="primary"
        append-icon="mdi-eye-outline"
        href="https://gabriel-cacayan.github.io/vue-movie"
        :class="displayBlock"
        target="_blank"
        >Launch App
      </v-btn>
    </div>
    <v-divider class="my-4"></v-divider>
    <h1 class="text-h3 mt-10 mb-4">Gallery</h1>
    <lightgallery
      :settings="{ speed: 500, plugins: plugins }"
      :onBeforeOpen="onBeforeOpen"
      :onBeforeClose="onBeforeClose"
    >
      <a
        v-for="picture in pictures"
        :key="picture.id"
        :href="picture.src"
        :data-sub-html="`<h4>${picture.title}</h4><p>Zoom in to see the details.</p>`"
      >
        <img
          v-show="picture.show"
          :alt="picture.title"
          :src="picture.src"
          :width="galleryWidth"
        />
      </a>
    </lightgallery>
  </v-container>
</template>

<script>
// import { Options, Vue } from "vue-class-component";
import { useDisplay } from "vuetify";
import Lightgallery from "lightgallery/vue";
import lgThumbnail from "lightgallery/plugins/thumbnail";
import lgZoom from "lightgallery/plugins/zoom";
import v0 from "../assets/vue_movie/v0.jpg";
import v1 from "../assets/vue_movie/v1.jpeg";
import v2 from "../assets/vue_movie/v2.jpeg";
import v3 from "../assets/vue_movie/v3.jpeg";
import v4 from "../assets/vue_movie/v4.jpeg";
import v5 from "../assets/vue_movie/v5.png";
import v6 from "../assets/vue_movie/v6.jpeg";
import v7 from "../assets/vue_movie/v7.png";
import v8 from "../assets/vue_movie/v8.jpeg";
import v9 from "../assets/vue_movie/v9.jpeg";
import v10 from "../assets/vue_movie/v10.jpeg";
import v11 from "../assets/vue_movie/v11.jpeg";
import v12 from "../assets/vue_movie/v12.jpeg";
import v13 from "../assets/vue_movie/v13.jpeg";
import v14 from "../assets/vue_movie/v14.jpeg";
import v15 from "../assets/vue_movie/v15.jpeg";

export default {
  components: {
    Lightgallery,
  },
  data() {
    return {
      plugins: [lgThumbnail, lgZoom],
      pictures: [
        {
          id: 1,
          src: v0,
          title: "Landing page in user's perspective",
          show: true,
        },
        {
          id: 2,
          src: v1,
          title: "Landing page",
          show: false,
        },
        {
          id: 3,
          src: v2,
          title: "Tv details",
          show: false,
        },
        {
          id: 4,
          src: v3,
          title: "List of episode in a season",
          show: false,
        },
        {
          id: 5,
          src: v4,
          title: "Tv episode",
          show: false,
        },
        {
          id: 6,
          src: v5,
          title: "Tv's pictures",
          show: false,
        },
        {
          id: 7,
          src: v6,
          title: "Detail of a person",
          show: false,
        },
        {
          id: 8,
          src: v7,
          title: "Pictures of a person",
          show: false,
        },
        {
          id: 9,
          src: v8,
          title: "Tv credits of a person",
          show: false,
        },
        {
          id: 10,
          src: v9,
          title: "Movie credits of a person",
          show: false,
        },
        {
          id: 11,
          src: v10,
          title: "Movie Details",
          show: false,
        },
        {
          id: 12,
          src: v11,
          title: "Movie's casts (Avengers: Endgame)",
          show: false,
        },
        {
          id: 13,
          src: v12,
          title: "Search for anything (Movie, People, or Tv)",
          show: false,
        },
        {
          id: 14,
          src: v13,
          title: "Search Result",
          show: false,
        },
        {
          id: 15,
          src: v14,
          title: "List of popular tv series",
          show: false,
        },
        {
          id: 16,
          src: v15,
          title: "List of top rated tv series",
          show: false,
        },
      ],
      responsive: useDisplay().name.value,
    };
  },
  computed: {
    displayBlock() {
      if (this.responsive == "xs" || this.responsive == "sm") {
        return "mt-4 w-100";
      } else {
        return "mr-2";
      }
    },
    galleryWidth() {
      if (this.responsive == "xs" || this.responsive == "sm") {
        return 300;
      } else {
        return 700;
      }
    },
  },
  methods: {
    onBeforeOpen: function () {
      this.pictures.map((picture) => (picture.show = true));
    },
    onBeforeClose: function () {
      this.pictures.map((picture, i) => {
        if (i == 0) {
          picture.show = true;
        } else {
          picture.show = false;
        }
      });
    },
  },
};
</script>

<style scoped>
@import "lightgallery/css/lightgallery.css";
@import "lightgallery/css/lg-thumbnail.css";
@import "lightgallery/css/lg-zoom.css";
</style>
