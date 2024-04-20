<template>
  <section
    id="skills"
    class="w-4/5 mx-auto py-8 min-h-screen flex flex-col justify-center"
  >
    <Title type="start">skills</Title>

    <div class="grid grid-cols-3 lg:grid-cols-5 gap-4 lg:gap-8 my-12">
      <div v-for="skill in skills" class="text-center">
        <div
          class="px-4 py-8 border-4 border-primary flex items-center justify-center rounded-xl"
        >
          <img :src="skill.img" alt="html" class="w-auto lg:w-16" />
        </div>
        <p class="mt-4 font-bold">{{ skill.name }}</p>
      </div>
    </div>

    <Title type="end">skills</Title>
  </section>
</template>

<script>
import Title from "./Title.vue";

export default {
  components: {
    Title,
  },
  data() {
    return {
      skills: [
        {
          name: "HTML",
          img: "https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/html/html.png",
        },
        {
          name: "CSS",
          img: "https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/css/css.png",
        },
        {
          name: "Bootstrap",
          img: "https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/bootstrap/bootstrap.png",
        },
        {
          name: "Tailwind CSS",
          img: "https://raw.githubusercontent.com/github/explore/261c2cda92d09ccad6f8b2dc91af32a2a5856989/topics/tailwind/tailwind.png",
        },
        {
          name: "JavaScript",
          img: "https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/javascript/javascript.png",
        },
        {
          name: "Vue.js",
          img: "https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/vue/vue.png",
        },
        {
          name: "PHP",
          img: "https://raw.githubusercontent.com/github/explore/ccc16358ac4530c6a69b1b80c7223cd2744dea83/topics/php/php.png",
        },
        {
          name: "Laravel",
          img: "https://raw.githubusercontent.com/github/explore/56a826d05cf762b2b50ecbe7d492a839b04f3fbf/topics/laravel/laravel.png",
        },
        {
          name: "MySQL",
          img: "https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/mysql/mysql.png",
        },
        {
          name: "WordPress",
          img: "https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/wordpress/wordpress.png",
        },
        {
          name: "Digital Ocean",
          img: "https://upload.wikimedia.org/wikipedia/commons/thumb/f/ff/DigitalOcean_logo.svg/1024px-DigitalOcean_logo.svg.png",
        },
        {
          name: "AWS",
          img: "https://raw.githubusercontent.com/github/explore/fbceb94436312b6dacde68d122a5b9c7d11f9524/topics/aws/aws.png",
        },
        {
          name: "Git",
          img: "https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/git/git.png",
        },
      ],
    };
  },
};
</script>
