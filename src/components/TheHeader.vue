<template>
  <v-navigation-drawer v-model="drawer" temporary>
    <!-- <v-list-item
        prepend-avatar="https://randomuser.me/api/portraits/men/78.jpg"
        title="John Leider"
      ></v-list-item>

      <v-divider></v-divider> -->

    <v-list density="compact" nav>
      <v-list-item
        prepend-icon="mdi-view-dashboard"
        title="Home"
        @click="closeDrawer('Home')"
      ></v-list-item>
      <v-list-item
        prepend-icon="mdi-folder"
        title="Projects"
        @click="closeDrawer('Projects')"
      ></v-list-item>
      <v-list-item
        prepend-icon="mdi-briefcase"
        title="Experience"
        @click="closeDrawer('Experience')"
      ></v-list-item>
    </v-list>
  </v-navigation-drawer>

  <v-app-bar absolute>
    <v-app-bar-nav-icon
      v-if="showNavIcon"
      @click="drawer = !drawer"
    ></v-app-bar-nav-icon>

    <div v-if="showNavItem">
      <div class="d-flex align-center justify-center">
        <v-toolbar-title @click="selectedTab('Home')" class="mx-8 pointer"
          >Gabriel Cacayan</v-toolbar-title
        >
        <v-toolbar-items class="mr-8 pointer" @click="selectedTab('Projects')"
          >Projects</v-toolbar-items
        >
        <v-toolbar-items class="mr-8 pointer" @click="selectedTab('Experience')"
          >Experience</v-toolbar-items
        >
      </div>
    </div>
  </v-app-bar>
</template>

<script>
import { useDisplay } from "vuetify";

export default {
  inject: ["selectedTab"],
  data() {
    return {
      drawer: false,
      responsive: useDisplay().name.value,
    };
  },
  computed: {
    showNavItem() {
      if (
        this.responsive == "xs" ||
        this.responsive == "sm" ||
        this.responsive == "md"
      ) {
        return false;
      } else {
        return true;
      }
    },
    showNavIcon() {
      if (
        this.responsive == "xs" ||
        this.responsive == "sm" ||
        this.responsive == "md"
      ) {
        return true;
      } else {
        return false;
      }
    },
  },
  methods: {
    closeDrawer(tab) {
      this.drawer = false;
      this.selectedTab(tab);
    },
  },
};
</script>

<style></style>
