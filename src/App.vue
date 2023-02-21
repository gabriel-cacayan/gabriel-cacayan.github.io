<template>
  <v-app theme="dark">
    <TheHeader :drawer="drawer" />
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
    </v-main>
  </v-app>
</template>

<script>
import ExperienceDetail from "./components/ExperienceDetail.vue";
import HomeDetail from "./components/HomeDetail.vue";
import ProjectDetail from "./components/ProjectDetail.vue";
import TheHeader from "./components/TheHeader.vue";

export default {
  name: "App",

  components: {
    ExperienceDetail,
    TheHeader,
    HomeDetail,
    ProjectDetail,
  },

  data() {
    return {
      tab: "Home",
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
