<script>
export default {
  data() {
    return {};
  },

  props: {
    project: Object,
  },
  computed: {
    getAbstract() {
      return this.project.description.text(0, 150) + "[...]";
    },
  },
};
</script>

<template>
  <div class="col col-4">
    <div class="card">
      <div class="card-header my-2">
        <h5 class="card-title">{{ project.title }}</h5>
      </div>
      <div class="card-body">
        <p class="card-text">{{ getAbstract }}</p>
      </div>
      <div class="card-footer">
        <div v-if="project.type">
          {{ project.type.label }}
        </div>
        <div v-else>
          <span class="text-muted">-</span>
        </div>
        <div v-if="project.technology">
          {{ project.technologies.label }}
        </div>
        <div v-else class="text-muted">
          <span>-</span>
        </div>
        <div>
          <router-link
            type="button"
            class="btn btn-sm btn-primary"
            :to="{
              name: 'project-detail',
              params: {
                id: project.id,
              },
            }"
          >
            open
          </router-link>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped></style>
