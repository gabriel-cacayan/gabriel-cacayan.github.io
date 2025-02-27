<template>
  <section
    id="experience"
    class="w-4/5 mx-auto py-8 flex flex-col justify-center"
  >
    <Title>Experience</Title>

    <div class="text-base lg:text-lg my-12">
      <div
        v-for="(job, key) in jobs"
        class="grid grid-cols-1 lg:grid-cols-2 gap-4 lg:gap-8 mx-auto lg:divide-x-4 divide-gray-900"
      >
        <div class="space-y-2 lg:text-end">
          <h1 class="text-lg font-bold uppercase">{{ job.title }}</h1>
          <p>{{ job.company }}</p>
          <p class="font-semibold">{{ job.year }}</p>
        </div>
        <div class="lg:pl-4 pb-12">
          <p>
            {{ job.reponsibility }}
          </p>
        </div>
      </div>
    </div>
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
      jobs: [
        {
          title: "Web developer",
          company: "Fil-Global Immigration Services Corp.",
          year: "April 2023 - Present",
          reponsibility: `As the main developer for all web applications, I have successfully
            migrated projects from old to new servers and recreated legacy
            websites with modern, optimized versions. By building intuitive user
            interfaces, I help the company attract and retain more clients,
            ensuring a seamless and engaging user experience.`,
        },
        {
          title: "Software developer",
          company: "Johnsons Berkshire Solutions Inc.",
          year: "March 2022 - April 2023",
          reponsibility: `I am responsible for developing new websites, maintaining existing
            ones, and implementing new features to enhance functionality. I
            collaborate closely with senior developers to achieve project goals
            and deliver desired outcomes while actively participating in code
            reviews and seeking feedback for continuous improvement.`,
        },
        {
          title: "Software developer intern",
          company: "Johnsons Berkshire Solutions Inc.",
          year: "July 2021 - March 2022",
          reponsibility: `  I am responsible for maintaining existing websites and implementing
            new features while contributing to team discussions and
            brainstorming sessions to drive problem-solving and innovation.
            Additionally, I assist in troubleshooting and resolving technical
            issues in web applications to ensure smooth functionality and user
            experience.`,
        },
      ],
    };
  },
};
</script>
