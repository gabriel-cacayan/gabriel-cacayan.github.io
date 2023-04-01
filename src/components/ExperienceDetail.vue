<template>
  <v-container class="mb-10">
    <h1 class="text-center my-4">Experience Timeline</h1>
    <v-timeline class="overflow-auto">
      <v-timeline-item
        size="small"
        dot-color="#2962FF"
        v-for="(item, i) in items"
        :key="i"
      >
        <template v-slot:opposite>
          <span>{{ item.year }}</span>
        </template>
        <v-card class="elevation-2 mx-auto">
          <v-card-title class="text-h5">{{ item.title }}</v-card-title>
          <v-card-subtitle>{{ item.company }}</v-card-subtitle>
          <v-card-text>{{ item.description }}</v-card-text>
        </v-card>
      </v-timeline-item>
    </v-timeline>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          color: "pink",
          year: "June 28, 2022",
          title: "Graduation",
          company: "University of Caloocan City",
          description:
            "Studied Bachelor of Science in Information Systems. (2018 - 2022)",
        },
        {
          color: "amber",
          year: "March 26, 2022 - April 14, 2023",
          title: "Software Developer",
          company: "Johnsons Berkshire Solutions Inc.",
          description:
            "Performed software development tasks, assisted in the design and functionality of software applications, and communicated closely with senior software engineers.",
        },
        {
          color: "orange",
          year: "July 19, 2021 - March 20, 2022",
          title: "Software Developer Intern",
          company: "Johnsons Berkshire Solutions Inc.",
          description:
            "Responsible for the maintenance and support of all the delivered projects of the Department.",
        },
      ],
    };
  },
};
</script>

<style></style>
