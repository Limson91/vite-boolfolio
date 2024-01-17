<script>
export default {
    props: {
        project: {
            type: Object,
            required: true
        }
    }
}
</script>

<template>
    <div class="card project-card">
        <h3>{{ project.title }}</h3>
        <p>{{ project.description }}</p>
    </div>
</template>

<style scoped lang="scss"></style>