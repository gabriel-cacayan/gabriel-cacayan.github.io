<script>
export default {
  data() {
    return {
      open: false,
    };
  },
  methods: {
    showDropdown() {
      this.open = !this.open;
    },
    getLinkClass(targetUrl) {
      // Check if the current URL matches the target URL
      if (window.location.hash === targetUrl) {
        // Return the class string when the condition is true
        return "bg-white rounded-full text-primary px-4 py-2";
      } else {
        // Return an empty string or other default class when the condition is false
        return "";
      }
    },
    handleHashChange() {
      this.$forceUpdate(); // Force component re-render
    },
  },

  beforeUnmount() {
    window.removeEventListener("hashchange", this.handleHashChange);
  },
  mounted() {
    window.addEventListener("hashchange", this.handleHashChange);
  },
};
</script>

<template>
  <nav class="bg-primary text-white p-8 w-full uppercase">
    <div
      class="hidden lg:flex items-center justify-around w-3/5 mx-auto font-semibold tracking-widest"
    >
      <a href="#home" :class="getLinkClass('#home')">Home</a>
      <a href="#about" :class="getLinkClass('#about')">About</a>
      <a href="#experience" :class="getLinkClass('#experience')">Experience</a>
      <a href="#skills" :class="getLinkClass('#skills')">Skills</a>
      <a href="#projects" :class="getLinkClass('#projects')">Projects</a>
      <a href="#contact" :class="getLinkClass('#contact')">Contact</a>
    </div>
    <div class="block lg:hidden">
      <div class="flex justify-end">
        <button @click="showDropdown">
          <svg
            class="w-10 h-10 text-white"
            aria-hidden="true"
            xmlns="http://www.w3.org/2000/svg"
            width="24"
            height="24"
            fill="none"
            viewBox="0 0 24 24"
          >
            <path
              stroke="currentColor"
              stroke-linecap="round"
              stroke-width="2"
              d="M5 7h14M5 12h14M5 17h14"
            />
          </svg>
        </button>
      </div>
      <div
        v-if="open"
        class="flex flex-col items-center space-y-4 mt-4 font-semibold tracking-widest"
      >
        <a href="#home" :class="getLinkClass('#home')">Home</a>
        <a href="#about" :class="getLinkClass('#about')">About</a>
        <a href="#experience" :class="getLinkClass('#experience')"
          >Experience</a
        >
        <a href="#skills" :class="getLinkClass('#skills')">Skills</a>
        <a href="#projects" :class="getLinkClass('#projects')">Projects</a>
        <a href="#contact" :class="getLinkClass('#contact')">Contact</a>
      </div>
    </div>
  </nav>
</template>
