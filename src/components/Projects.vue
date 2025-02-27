<template>
  <section id="projects" class="mx-auto py-8 min-h-screen w-4/5">
    <Title class="">Projects</Title>

    <div class="mt-4 lg:mt-0 mb-12">
      <div
        v-for="(project, key) in projects"
        :key="key"
        class="grid grid-cols-1 lg:grid-cols-2 gap-4 lg:min-h-screen justify-center items-center text-center lg:text-left border-b border-gray-500 last:border-b-0"
        :class="project.bgColor"
      >
        <div class="order-last lg:order-first">
          <h1 class="text-3xl lg:text-5xl font-bold mb-4">
            {{ project.name }}
          </h1>
          <p>
            {{ project.description }}
          </p>
          <a
            :href="project.link"
            target="_blank"
            class="my-4 inline-flex items-center px-3 py-2 text-sm font-medium text-center text-white bg-primary rounded-lg hover:bg-white hover:text-primary border hover:border-primary"
          >
            View project
            <svg
              class="rtl:rotate-180 w-3.5 h-3.5 ms-2"
              aria-hidden="true"
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 14 10"
            >
              <path
                stroke="currentColor"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M1 5h12m0 0L9 1m4 4L9 9"
              />
            </svg>
          </a>
        </div>
        <div class="mb-4">
          <img
            :src="project.img"
            :alt="project.name"
            loading="lazy"
            class="rounded-t-lg"
          />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import Title from "./Title.vue";
import trabagoImage from "../assets/trabago_laptop.png";
import vueMovieImage from "../assets/vue_movie_laptop.png";
import zyploImage from "../assets/zyplo_laptop.png";

export default {
  components: {
    Title,
  },
  data() {
    return {
      projects: [
        {
          name: "Zyplo",
          img: zyploImage,
          description:
            "An intuitive and dynamic eCommerce platform built with modern web technologies to provide a seamless shopping experience. The website includes product catalogs, shopping cart, secure payment gateways, and responsive design for optimal performance across devices. With a focus on user experience, the platform integrates advanced filtering, search functionality, and personalized recommendations to enhance the shopping journey.",
          link: "https://zyplo.gabrielcacayan.com",
          bgColor: "bg-white",
        },
        {
          name: "Vue Movie",
          img: vueMovieImage,
          description:
            "Vue Movie is an online database of information related to films, television series, ratings, and reviews. This project is created using Vue.js and an API.",
          link: "https://vue-movie.gabrielcacayan.com/",
          bgColor: "bg-white",
        },
        {
          name: "TrabaGo!",
          img: trabagoImage,
          description:
            "TrabaGo is a web  portal in which job-hunters can register online and apply. This system helps the company or recruiters to manage job openings, interview schedules, find and hire new personnel. The idea is basically to set-up a Job Portal for the Hiring Managers to streamline the process of recruitment. For Applicants to easily apply with all the job openings available.",
          link: "https://trabago.gabrielcacayan.com/",
          bgColor: "bg-white",
        },
      ],
      cardKey: null,
    };
  },
};
</script>
