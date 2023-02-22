<template>
  <v-container>
    <h1 class="text-h3 my-4">About the project</h1>
    <p class="mb-4">
      Yowndrift is a blog web application, where anyone can share their ideas or
      knowledge on a specific topic.
    </p>
    <v-divider class="my-4"></v-divider>
    <h1 class="text-h3 mt-10 mb-4">Features</h1>
    <ul class="mb-4">
      <li>
        The system has log in, register, reset password, and email verification.
      </li>
      <li>
        In addition to typical, form based authentication, the system also used
        Laravel Socialite that supports authentication with GitHub and Google.
      </li>
      <li>
        Users can also update account's profile information, email address, and
        password.
      </li>
      <li>
        The system also provides two-factor authentication, browser sessions,
        and delete account option.
      </li>
      <li>
        The system mainly uses the CRUD functions for creating, reading,
        updating, and deleting posts.
      </li>
      <li>Users can also write comments to a post.</li>
      <li>The system used Livewire for Front-end and Laravel for Back-end.</li>
    </ul>
    <v-divider class="my-4"></v-divider>
    <h1 class="text-h3 mt-10 mb-4">Platform Type</h1>
    <p class="mb-4">Web App</p>
    <v-divider class="my-4"></v-divider>
    <h1 class="text-h3 mt-10 mb-4">Technologies used</h1>
    <h3 class="mb-4">For front-end:</h3>
    <ul class="mb-4">
      <li>HTML</li>
      <li>CSS</li>
      <li>Tailwind CSS</li>
      <li>JavaScript</li>
      <li>Laravel Livewire</li>
    </ul>
    <h3 class="mb-4">For back-end:</h3>
    <ul class="mb-4">
      <li>Laravel</li>
    </ul>
    <h3 class="mb-4">For database:</h3>
    <ul>
      <li>MySQL</li>
    </ul>

    <div class="mt-10">
      <v-btn
        variant="outlined"
        append-icon="mdi-code-braces"
        href="https://github.com/gabriel-cacayan/yowndrift"
        :class="displayBlock"
        target="_blank"
        >Source Code</v-btn
      >
      <v-btn
        variant="tonal"
        color="primary"
        append-icon="mdi-eye-outline"
        :class="displayBlock"
        >Launch App
        <v-tooltip activator="parent" location="end"
          >Unavailable at the moment.</v-tooltip
        ></v-btn
      >
    </div>
    <v-divider class="my-4"></v-divider>
    <h1 class="text-h3 mt-10 mb-4">Gallery</h1>
    <lightgallery
      :settings="{ speed: 500, plugins: plugins }"
      :onBeforeOpen="onBeforeOpen"
      :onBeforeClose="onBeforeClose"
    >
      <a v-for="picture in pictures" :key="picture.id" :href="picture.src">
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
import y1 from "../assets/yowndrift/y1.jpeg";
import y2 from "../assets/yowndrift/y2.jpeg";
import y3 from "../assets/yowndrift/y3.jpeg";
import y4 from "../assets/yowndrift/y4.jpeg";
import y5 from "../assets/yowndrift/y5.jpeg";
import y6 from "../assets/yowndrift/y6.png";
import y7 from "../assets/yowndrift/y7.jpeg";
import y8 from "../assets/yowndrift/y8.jpeg";
import y9 from "../assets/yowndrift/y9.jpeg";
import y10 from "../assets/yowndrift/y10.jpeg";
import y11 from "../assets/yowndrift/y11.jpeg";
import y12 from "../assets/yowndrift/y12.jpeg";
import y13 from "../assets/yowndrift/y13.jpeg";

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
          src: y1,
          title: "Landing page",
          show: true,
        },
        {
          id: 2,
          src: y2,
          title: "Home page",
          show: false,
        },
        {
          id: 3,
          src: y3,
          title: "All posts",
          show: false,
        },
        {
          id: 4,
          src: y4,
          title: "Create a post",
          show: false,
        },
        {
          id: 5,
          src: y5,
          title: "Specific post",
          show: false,
        },
        {
          id: 6,
          src: y6,
          title: "Search a post",
          show: false,
        },
        {
          id: 7,
          src: y7,
          title: "Login",
          show: false,
        },
        {
          id: 8,
          src: y8,
          title: "Register",
          show: false,
        },
        {
          id: 9,
          src: y9,
          title: "Reset password",
          show: false,
        },
        {
          id: 10,
          src: y10,
          title: "Dashboard",
          show: false,
        },
        {
          id: 11,
          src: y11,
          title: "Profile",
          show: false,
        },
        {
          id: 12,
          src: y12,
          title: "Update a post",
          show: false,
        },
        {
          id: 13,
          src: y13,
          title: "User's posts",
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
