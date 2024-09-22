<template>
  <section
    id="experience"
    class="py-8 min-h-screen flex flex-col justify-center"
  >
    <div class="bg-gradient-to-t from-primary py-20">
      <Title type="start" class="w-4/5 mx-auto">experience</Title>
    </div>

    <div class="bg-primary text-white text-base lg:text-lg">
      <div
        class="grid grid-cols-1 lg:grid-cols-2 gap-4 lg:gap-8 w-4/5 mx-auto lg:divide-x-4 divide-white"
      >
        <div class="space-y-2 lg:text-end">
          <h1 class="text-lg font-semibold uppercase">Web developer</h1>
          <p>Fil-Global Immigration Services Corp.</p>
          <p>April 2023 - June 2024</p>
        </div>
        <div class="pl-4 pb-12">
          <ul class="list-disc lg:list-inside">
            <li>Main developer for all web applications.</li>
            <li>Migrated projects from old to new servers.</li>
            <li>Recreated legacy websites as new ones.</li>
            <li>Mentored junior developers.</li>
          </ul>
        </div>
      </div>

      <div
        class="grid grid-cols-1 lg:grid-cols-2 gap-4 lg:gap-8 w-4/5 mx-auto lg:divide-x-4 divide-white"
      >
        <div class="space-y-2 lg:text-end">
          <h1 class="text-lg font-semibold uppercase">Software developer</h1>
          <p>Johnsons Berkshire Solutions Inc.</p>
          <p>March 2022 - April 2023</p>
        </div>
        <div class="pl-4 pb-12">
          <ul class="list-disc lg:list-inside">
            <li>Responsible for developing new websites.</li>
            <li>
              Responsible for maintaining existing websites and implementing new
              features.
            </li>
            <li>
              Collaborate closely with senior developers to achieve project
              goals and deliver desired outcomes.
            </li>
            <li>
              Actively participate in code reviews and seek feedback for
              continuous improvement.
            </li>
          </ul>
        </div>
      </div>

      <div
        class="grid grid-cols-1 lg:grid-cols-2 gap-4 lg:gap-8 w-4/5 mx-auto lg:divide-x-4 divide-white"
      >
        <div class="space-y-2 lg:text-end">
          <h1 class="text-lg font-semibold uppercase">
            Software developer intern
          </h1>
          <p>Johnsons Berkshire Solutions Inc.</p>
          <p>July 2021 - March 2022</p>
        </div>
        <div class="pl-4 pb-12">
          <ul class="list-disc lg:list-inside">
            <li>
              Responsible for maintaining existing websites and implementing new
              features.
            </li>
            <li>
              Contribute to team discussions and brainstorming sessions for
              problem-solving and innovation.
            </li>
            <li>
              Assist in troubleshooting and resolving technical issues in web
              applications.
            </li>
          </ul>
        </div>
      </div>
    </div>

    <div class="bg-gradient-to-b from-primary py-20">
      <Title type="end" class="w-4/5 mx-auto">experience</Title>
    </div>
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
