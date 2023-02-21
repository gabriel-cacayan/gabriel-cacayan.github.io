<template>
  <v-container>
    <h1>About the project</h1>
    <p class="mb-4">
      Yowndrift is a blog web application, where anyone can share their ideas or
      knowledge on a specific topic.
    </p>
    <v-divider class="my-4"></v-divider>
    <h1>Features</h1>
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
    <h1>Platform Type</h1>
    <p class="mb-4">Web App</p>
    <v-divider class="my-4"></v-divider>
    <h1>Technologies used</h1>
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

    <v-divider class="my-4"></v-divider>
    <div>
      <v-btn
        variant="outlined"
        append-icon="mdi-code-braces"
        href="https://github.com/gabriel-cacayan/yowndrift"
        target="_blank"
        class="mr-10"
        >Source Code</v-btn
      >
      <v-btn variant="tonal" color="primary" append-icon="mdi-eye-outline"
        >Launch App
        <v-tooltip activator="parent" location="end"
          >Unavailable at the moment.</v-tooltip
        ></v-btn
      >
    </div>
    <v-divider class="my-4"></v-divider>
    <h1>Gallery</h1>
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
          width="300"
        />
      </a>
    </lightgallery>
  </v-container>
</template>

<script>
// import { Options, Vue } from "vue-class-component";
import Lightgallery from "lightgallery/vue";
import lgThumbnail from "lightgallery/plugins/thumbnail";
import lgZoom from "lightgallery/plugins/zoom";
import y1 from "../assets/yowndrift/yowndrift_landing.jpeg";
import y2 from "../assets/yowndrift/yowndrift_home.jpeg";

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
          title: "Landing Page",
          show: true,
        },
        {
          id: 2,
          src: y2,
          title: "Home Page",
          show: false,
        },
      ],
      msg: "hello",
    };
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
