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
  },
};
</script>

<template>
  <nav class="bg-primary text-white p-8 w-full uppercase">
    <div
      class="hidden lg:flex items-center justify-around w-3/5 mx-auto font-semibold"
    >
      <a href="#">Home</a>
      <a href="#">About</a>
      <a href="#">Experience</a>
      <a href="#">SKills</a>
      <a href="#">Projects</a>
      <a href="#">Education</a>
      <a href="#">Contact</a>
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
      <div v-if="open" class="flex flex-col space-y-2 mt-4">
        <a href="#">Home</a>
        <a href="#">About</a>
        <a href="#">Experience</a>
        <a href="#">SKills</a>
        <a href="#">Projects</a>
        <a href="#">Education</a>
        <a href="#">Contact</a>
      </div>
    </div>
  </nav>
</template>
