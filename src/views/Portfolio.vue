<script>
import ProjectCard from '../components/ProjectCard.vue';

export default {
    components: {
        ProjectCard,
    },

    data() {
        return {
            projects: [],
        };
    },
};
</script>

<template>
    <div>
        <h2>Portfolio</h2>
        <ProjectCard v-for="project in projects" :key="project.id" :project="project" />

        <router-link to="/">Back to Home</router-link>
    </div>
</template>

<style scoped lang="scss"></style>