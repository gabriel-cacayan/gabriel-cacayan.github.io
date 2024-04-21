<template>
  <section id="projects" class="w-4/5 mx-auto py-8 min-h-screen">
    <Title type="start">projects</Title>

    <div class="my-12 grid grid-cols-1 lg:grid-cols-3 gap-8">
      <div v-for="(project, key) in projects" :key="key">
        <div class="bg-white border border-gray-200 rounded-lg shadow">
          <a :href="project.link">
            <img
              :src="project.img"
              :alt="project.name"
              loading="lazy"
              class="rounded-t-lg"
            />
          </a>
          <div class="p-5">
            <a :href="project.link">
              <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900">
                {{ project.name }}
              </h5>
            </a>
            <p
              class="mb-3 font-normal text-gray-700 h-24 overflow-hidden"
              :class="{ '!h-auto': key === cardKey }"
            >
              {{ project.description }}
            </p>
            <div class="flex justify-between items-center">
              <a
                :href="project.link"
                target="_blank"
                class="inline-flex items-center px-3 py-2 text-sm font-medium text-center text-white bg-primary rounded-lg hover:bg-white hover:text-primary border hover:border-primary"
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
              <p
                class="text-primary cursor-pointer"
                :class="{ hidden: project.description.length < 180 }"
                @click="changeHeight(key, project.description)"
              >
                <span v-if="cardKey === null">Read more</span>
                <span v-else>Hide</span>
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>

    <Title type="end" class="mb-12">projects</Title>
  </section>
</template>

<script>
import Title from "./Title.vue";
import trabagoImage from "../assets/trabago.png";
import vueMovieImage from "../assets/vue-movie.png";
import expendicareImage from "../assets/expendicare.png";

export default {
  components: {
    Title,
  },
  data() {
    return {
      projects: [
        {
          name: "TrabaGo!",
          img: trabagoImage,
          description:
            "TrabaGo is a web  portal in which job-hunters can register online and apply. This system helps the company or recruiters to manage job openings, interview schedules, find and hire new personnel. The idea is basically to set-up a Job Portal for the Hiring Managers to streamline the process of recruitment. For Applicants to easily apply with all the job openings available.",
          link: "https://trabago.gabrielcacayan.com/",
        },
        {
          name: "Vue Movie",
          img: vueMovieImage,
          description:
            "Vue Movie is an online database of information related to films, television series, ratings, and reviews. This project is created using Vue.js and an API.",
          link: "https://vue-movie.gabrielcacayan.com/",
        },
        {
          name: "ExpendiCare",
          img: expendicareImage,
          description:
            "An expense tracker to help people reduce household bills. By Tracking your expenses, you can take control of your finances and make better decisions for your future.",
          link: "https://expendicare.gabrielcacayan.com/login",
        },
      ],
      cardKey: null,
    };
  },
  methods: {
    changeHeight(key, description) {
      // console.log(description.length);
      if (this.cardKey === null) {
        this.cardKey = key;
      } else {
        this.cardKey = null;
      }
    },
  },
};
</script>
