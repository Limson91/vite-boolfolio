<script>
import axios from 'axios';
import ProjectCard from '/components/ProjectCard.vue';

export default {
  components: {
    ProjectCard
  },

  data() {
    return {
      projects: [],
      BASE_URL: 'http://127.0.0.1:8000/api'
    };
  },

  methods: {
    fetchProjects() {
      axios.get(`${this.BASE_URL}/projects`).then((red) => {
        console.log(res.data.results);
        this.projects = red.data.results;
      });
    }
  },

  created() {
    this.fetchProjects();
  }
}
</script>

<template>
  <!-- <div class="container">
    <h3>Projects List</h3>
  </div>

  <div class="container">
    <section>
      <div v-for="project in projects" :key="project.id" class="card project-card">
        <ProjectCard :project="project" />
      </div>
    </section>
  </div> -->

  <router-view>

  </router-view>
</template>

<style scoped lang="scss">
.container {
  margin-top: 15px;
  text-align: center;
}

.project-card {
  background-color: darkblue;
  border: 1px, solid black;
  color: white;
  padding: 15px;
  margin-bottom: 15px;
}
</style>
