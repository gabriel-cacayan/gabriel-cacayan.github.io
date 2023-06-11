<template>
  <v-app>
    <v-main class="d-flex justify-center align-center bg-grey-lighten-4">
      <v-container class="d-flex justify-center align-center">
        <v-card
          title="Gabriel Cacayan"
          subtitle="Web Developer"
          text="As a web developer, my focus is on creating engaging and
                user-friendly websites and applications. I have experience
                working with a range of technologies, but I particularly enjoy
                using Laravel and Vue, which I find to be powerful and effective
                tools for building high-quality web projects."
          variant="outlined"
          max-width="400"
          class="bg-white py-4"
        >
          <v-divider></v-divider>
          <div class="ml-4 py-4">
            <h1 class="text-h6">Projects</h1>
            <a
              href="https://vue-movie.gabrielcacayan.com/"
              target="_blank"
              class="card-link bullet-link"
              >Vue Movie</a
            >
          </div>
        </v-card>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "App",

  data() {
    return {
      // Your data here
    };
  },
};
</script>

<style>
.pointer {
  cursor: pointer;
}

.card-heading {
  font-size: 24px;
  font-weight: bold;
  margin-bottom: 16px;
}

.card-link {
  color: #41b883; /* Adjust the color as desired */
  font-size: 16px;
  text-decoration: none;
  position: relative;
  padding-left: 20px;
}

.card-link:before {
  content: "";
  position: absolute;
  left: 0;
  top: 50%;
  transform: translateY(-50%);
  height: 6px;
  width: 6px;
  background-color: #41b883; /* Adjust the color as desired */
  border-radius: 50%;
}

.card-link:hover {
  text-decoration: underline;
}
</style>
