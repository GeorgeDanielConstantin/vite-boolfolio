<script>
import ProjectCard from "./ProjectCard.vue";
export default {
  props: {
    projects: Array,
    title: String,
  },
  components: {
    ProjectCard,
  },
};
</script>

<template>
  <div class="container mt-5">
    <div class="row g-3 d-flex">
      <ProjectCard
        v-for="project in projects"
        :project="project"
        :key="project.id"
        class="d-flex"
      />
    </div>
  </div>
</template>

<style lang="scss" scoped></style>
