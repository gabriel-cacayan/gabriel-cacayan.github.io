<template>
  <section
    id="home"
    class="bg-[#222222] text-white grid grid-cols-1 lg:grid-cols-2 gap-8 p-8 min-h-screen"
  >
    <div class="place-self-center space-y-2">
      <h1 class="text-5xl lg:text-7xl font-bold">Hello!</h1>
      <h1 class="text-5xl lg:text-7xl font-bold">I am Gabriel;</h1>
      <h1 class="text-3xl lg:text-5xl">a web developer;</h1>
    </div>
    <div class="place-self-center">
      <img
        :src="profilePicture"
        alt="Rounded avatar"
        loading="lazy"
        class="w-96 rounded-full"
      />
    </div>
  </section>
</template>

<script>
import profilePicture from "../assets/me.jpg";

export default {
  data() {
    return {
      profilePicture,
    };
  },
};
</script>
