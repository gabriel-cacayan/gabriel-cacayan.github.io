<template>
  <section id="about" class="w-4/5 mx-auto py-8 flex flex-col justify-center">
    <Title>About</Title>

    <p class="text-lg lg:text-xl my-12">
      As a web developer, my focus is on creating engaging and user-friendly
      websites and applications. I have experience working with a range of
      technologies, but I particularly enjoy using Laravel, Vue.js, and
      WordPress, which I find to be powerful and effective tools for building
      high-quality web projects.
    </p>
  </section>
</template>

<script>
import Title from "./Title.vue";

export default {
  components: {
    Title,
  },
};
</script>
