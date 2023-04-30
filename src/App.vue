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
          max-width="344"
          class="bg-white"
        ></v-card>
      </v-container>
    </v-main>

    <!-- <v-switch
      v-model="theme"
      label="Dark Mode"
      color="orange"
      value="dark"
      hide-details
    ></v-switch>
    {{ theme }} -->
    <!-- <TheHeader :drawer="drawer" />
    <v-main>
      <template v-if="tab == 'Home'">
        <HomeDetail />
      </template>
      <template v-else-if="tab == 'Projects'">
        <ProjectDetail />
      </template>
      <template v-else>
        <ExperienceDetail />
      </template>
      <v-footer class="d-flex align-center justify-center bg-grey-darken-1">
        {{ new Date().getFullYear() }} —
        <strong class="ml-2">Gabriel Cacayan</strong></v-footer
      >
    </v-main> -->
  </v-app>
</template>

<script>
// import ExperienceDetail from "./components/ExperienceDetail.vue";
// import HomeDetail from "./components/HomeDetail.vue";
// import ProjectDetail from "./components/ProjectDetail.vue";
// import TheHeader from "./components/TheHeader.vue";

export default {
  name: "App",

  components: {
    // ExperienceDetail,
    // TheHeader,
    // HomeDetail,
    // ProjectDetail,
  },

  data() {
    return {
      tab: "Home",
      theme: "dark",
    };
  },
  methods: {
    selectedTab: function (tab) {
      this.tab = tab;
    },
  },
  provide() {
    return {
      selectedTab: this.selectedTab,
    };
  },
};
</script>

<style>
.pointer {
  cursor: pointer;
}
</style>
